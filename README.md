# Phase III ⏩ GUI Exploration & Disk Space Troubleshooting (Splunk Server Issue) — Part 1

## 📝 My goal in this phase was to explore the Splunk GUI, locate key menus, and troubleshoot a disk space issue that was preventing indexing. Originally, I planned to focus solely on GUI exploration, but the server paused indexing due to low disk space. The mission was to attempt restoring indexing and understanding the problem.

<img width="1250" height="290" alt="GqhVhVm" src="https://github.com/user-attachments/assets/f67ebf69-8c85-43d6-ade0-7ffeae1e9013" />

## ⏩ Notes
## 📝 I noticed that Splunk had stopped indexing because the available disk space was only 4GB, below the required 5GB. This blocked data flow and prevented safe indexing. 

<img width="518" height="68" alt="ppNPj0c" src="https://github.com/user-attachments/assets/3c0bc5fd-9bb9-4555-b488-906ee93119c8" />

## 📝 I checked the server’s disk usage to confirm the problem.  

<img width="802" height="219" alt="XpXsZC7" src="https://github.com/user-attachments/assets/761aaab0-71b5-4b09-a5e2-3244dc0ffb33" />

## 📝 I attempted to free space by:  
- Removing temporary dispatch files. 🧹  
- Clearing system temporary files and caches. 🗑️  
- Moving large log files to a backup folder. 📂

<img width="804" height="91" alt="z4HGs9h" src="https://github.com/user-attachments/assets/fee223a4-1801-4f70-b594-2b56e426f6b3" />

<img width="511" height="71" alt="CFq5hrz" src="https://github.com/user-attachments/assets/7501e5fd-864b-410a-97f7-40f5fa485b3c" />

<img width="619" height="217" alt="hP1hTri" src="https://github.com/user-attachments/assets/57b6d637-8a87-428c-b4d1-f0b5eb647d48" />

## 📝 After performing these steps, I verified the available disk space, but indexing **still did not fully resume**. It became clear that the underlying issue was the VM disk size itself, which needed to be expanded before Splunk could function properly.  

## 📝 This phase highlighted that sometimes troubleshooting at the file level is not enough, and infrastructure adjustments are necessary to resolve persistent operational issues. 💻

## ⏩ Next Steps — Part 2

📝 Resize the VM disk to provide sufficient space for Splunk indexing.  
📝 Verify that the new disk space exceeds the 5GB minimum requirement.  
📝 Restart Splunk and confirm that indexing resumes successfully.  
📝 Continue GUI exploration once the server is stable.  
📝 Note: Fixing the issue this way is not ideal in production — temporary cleanup is safer, but underlying VM sizing must be addressed for long-term stability. 🚀


## ⏩ Summary
📌 This was a partial troubleshooting mission:  
📝 I identified the disk space issue on the Splunk server.  
📝 I applied safe cleanup steps to free space.  
📝 Indexing did not fully resume because the VM’s disk size was insufficient.  
📝 Part 2 will involve resizing the VM to provide enough storage for Splunk, after which indexing and GUI exploration can continue. 🚀
