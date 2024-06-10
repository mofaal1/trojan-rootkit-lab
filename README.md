---

## Project Showcase: Trojan and Rootkit Analysis

### Objective:
Analyzed the impact of a Trojan and a rootkit on a Windows machine using Task Manager, netstat, and File Explorer. Reported observations based on process lists, open ports, and file system changes at different points in time.

### Skills Learned:
- Malware analysis
- System monitoring
- Network port analysis
- File system inspection
- Using Task Manager, netstat, and File Explorer tools

### Tools Used:
- Windows VM
- Task Manager
- Netstat
- File Explorer

### Steps and Observations:

#### Initial Observations:

1. **Presence of "beast" in the Process List:**
   - Checked the Task Manager to see if "beast" was listed among running processes to identify malicious processes and understand the presence and impact of malware.
     
     ![Picture1](https://github.com/mofaal1/trojan-rootkit-lab/assets/137732122/f557a619-4394-4142-98e8-094be44e6e4d)

   - **Explanation:** The screenshot confirms the presence of "beast" in the Task Manager's process list.

2. **Open Ports on the Victim Computer:**
   - Used netstat to list open ports on the victim machine, as malware often opens network ports to communicate with external servers or attackers.
     
     ![Picture2](https://github.com/mofaal1/trojan-rootkit-lab/assets/137732122/a166fb8b-e080-4821-815a-123cf543afe2)

   - **Explanation:** The netstat output shows the open ports, focusing on entries starting with TCP and the specified IP address.

#### Remote Desktop and File System Observations:

3. **Victim’s Desktop in the Remote Desktop Window:**
   
   - Accessed the victim’s desktop via Remote Desktop to verify remote access and confirm whether the attacker can control the victim's machine.
     
     ![Picture3](https://github.com/mofaal1/trojan-rootkit-lab/assets/137732122/a9eee83f-e235-489b-9341-cd48da06a6ef)

   - **Explanation:** The screenshot shows the victim’s desktop as seen in the Remote Desktop window.

5. **Contents of the C: Drive on the Victim Machine:**
   
   - Browsed the C: drive on the victim machine using File Explorer to inspect the file system and identify any files or folders created by the malware.
  
       <img width="500" alt="Picture4" src="https://github.com/mofaal1/trojan-rootkit-lab/assets/137732122/ee6bb712-9155-4425-b96a-f6cbd1491cdc">

   - **Explanation:** The screenshot shows the contents of the C: drive, confirming access to the victim's file system.

6. **Success of Uploading Cartoon.jpg:**
   
   - Uploaded a file named Cartoon.jpg to the victim machine to demonstrate file upload capability, showing the level of control an attacker has over the victim machine.
     
      <img width="500" alt="Picture5" src="https://github.com/mofaal1/trojan-rootkit-lab/assets/137732122/6213a920-9fa2-41a3-aeba-92c0c9d231c1">

   - **Explanation:** The screenshot shows Cartoon.jpg in the Windows Explorer, indicating a successful upload.

8. **Chat Window:**
   
   - Opened the chat window used during the attack to document communication methods used by the attacker and understand the interaction between the attacker and the victim.
     
      ![Picture6](https://github.com/mofaal1/trojan-rootkit-lab/assets/137732122/fd2071f9-5157-4b61-8163-9f54f690211c)

   - **Explanation:** The screenshot captures the chat window, documenting the interaction.

#### Subsequent Observations:

7. **Presence of "beast" in the Process List:**
   
   - Checked the Task Manager again to see if "beast" was still listed among running processes to verify the persistence of the malware process and understand if it can evade termination.

     <img width="500" alt="picture7" src="https://github.com/mofaal1/trojan-rootkit-lab/assets/137732122/a0edfce7-5a80-412a-b426-7ba0ce8934dc">

   - **Explanation:** The screenshot confirms the continued presence of "beast" in the Task Manager's process list.

9. **New Open Ports on the Victim Computer:**
    
   - Used netstat to list new open ports on the victim machine to identify new ports that have opened since the initial check, revealing further malicious activity.

     <img width="500" alt="Picture8" src="https://github.com/mofaal1/trojan-rootkit-lab/assets/137732122/bbb98538-d367-40f7-aa3b-161ebc8a19c7">

   - **Explanation:** The netstat output shows additional open ports, indicating changes in the network status.

#### Task Manager and File System Analysis:

9. **"beast.exe" in Task Manager’s Process List:**
   - Checked Task Manager for the presence of beast.exe to confirm the presence of the specific executable, aiding in identifying and analyzing the malware.
   
     <img width="500" alt="Picture9" src="https://github.com/mofaal1/trojan-rootkit-lab/assets/137732122/30f6cdb1-6338-45be-a821-f891d2de9d44">

   - **Explanation:** The screenshot shows beast.exe running in the Task Manager.

10. **Open Ports for the Beast Trojan:**
    - Used netstat to identify ports opened by Beast Trojan, as knowing which ports the Trojan opens can help in understanding its communication mechanisms.
      
      <img width="500" alt="Picture10" src="https://github.com/mofaal1/trojan-rootkit-lab/assets/137732122/b5fd6c1d-ac26-4088-a5e8-034b2453361f">

    - **Explanation:** The netstat output shows the open ports associated with the Beast Trojan.

11. **Continued Presence of beast.exe in Task Manager:**
    - Rechecked Task Manager to see if beast.exe is still present to verify the persistence of the malware process over time, indicating its resilience and potential evasion techniques.

      <img width="500" alt="Picture11" src="https://github.com/mofaal1/trojan-rootkit-lab/assets/137732122/38a8ee7a-e71e-4583-ac35-8bbb4a58e7fa">

    - **Explanation:** The screenshot confirms that beast.exe remains active in the process list.

13. **Visibility of Previously Identified Open Ports:**
    - Used netstat to check the visibility of previously identified ports to determine whether the ports remain open or have been closed, indicating changes in the malware's behavior.

      <img width="500" alt="Picture12" src="https://github.com/mofaal1/trojan-rootkit-lab/assets/137732122/41818456-4f97-48ba-a885-a978ec32f48c">

    - **Explanation:** The netstat output indicates that the ports associated with the Beast Trojan are no longer open.

14. **C:\beast Folder:**
    - Checked for the presence of the C:\beast folder to identify files and directories created by malware, aiding in its analysis and cleanup.
      
      <img width="500" alt="Picture11" src="https://github.com/mofaal1/trojan-rootkit-lab/assets/137732122/38a8ee7a-e71e-4583-ac35-8bbb4a58e7fa">

    - **Explanation:** The screenshot shows the absence of the C:\beast folder in the file system.

15. **F:\Hackish\hxdef100 Subfolder:**
    - Checked for the presence of the \hxdef100 subfolder inside F:\Hackish to verify the presence of specific subfolders, helping in understanding the malware's installation and propagation.

      <img width="500" alt="Picture15" src="https://github.com/mofaal1/trojan-rootkit-lab/assets/137732122/66509dc8-fad1-4280-9073-602d6f38b3c0">
      

    - **Explanation:** The screenshot shows the \hxdef100 subfolder, indicating that the folder is present in the specified directory.

16. **Ports Connected to the Attacker Machine:**
    - Used netstat to identify ports connected to the attacker machine to understand which ports are used for communication with the attacker, aiding in analyzing the attack's command and control structure.
    
      <img width="500" alt="Picture10" src="https://github.com/mofaal1/trojan-rootkit-lab/assets/137732122/b5fd6c1d-ac26-4088-a5e8-034b2453361f">

    - **Explanation:** The netstat output shows the ports connected to the attacker machine, indicating active connections.

    - **Conclusion:** The hxdef100 rootkit alters port connections and visibility, making it harder to detect the malicious activity.

#### Final Observations:

16. **Presence of "beast" in Task Manager:**
    - Checked Task Manager for the "beast" process one last time to ensure the malware process remains active throughout the analysis, aiding in understanding its persistence.
    
      <img width="500" alt="Picture14" src="https://github.com/mofaal1/trojan-rootkit-lab/assets/137732122/17491b2d-f1fa-496b-8f34-7204b7a4b8c4">

    
    - **Explanation:** The screenshot shows the "beast" process in the Task Manager.

17. **Visibility of Previously Identified Ports:**
    - Used netstat to check the visibility of the ports identified earlier to confirm the presence or absence of these ports over time, indicating the malware's behavior regarding network communication.
    
      <img width="500" alt="Picture13" src="https://github.com/mofaal1/trojan-rootkit-lab/assets/137732122/ee53ee36-635f-4ed8-a5c4-92098671aa19">
    
    
    - **Explanation:** The netstat output confirms the visibility of the previously identified ports.

18. **Presence of C:\beast Folder:**
    - Checked for the presence of the C:\beast folder one last time to ensure the folder is present or absent, aiding in verifying the malware's impact on the file system.

      <img width="500" alt="C- beast Folder" src="https://github.com/mofaal1/trojan-rootkit-lab/assets/137732122/51ae50d6-910c-493f-89e0-fe8592289bbb">

    - **Explanation:** The screenshot shows the C:\beast folder in the file system.

19. **Presence of \hxdef100 Subfolder inside F:\Hackish:**
    - Checked for the presence of the \hxdef100 subfolder one last time to verify the presence of specific
