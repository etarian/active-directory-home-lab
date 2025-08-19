# Active Directory Home Lab – Setup Summary

This repository outlines a simplified home lab setup using VirtualBox, Windows Server 2019, and Active Directory, thanks to Josh Madakor’s tutorial. I plan on building this myself a few more time to get used to the process.
<img width="1358" height="805" alt="Screen Shot 2025-08-18 at 4 05 37 PM" src="https://github.com/user-attachments/assets/6dd0dded-cc11-4041-9b81-ffa6d28d263d" />

1. Installed Software and created VM
   - Oracle VirtualBox
   - Windows Server 2019 and Windows 10 ISOs
   - Create VM (`DC`) with two network adapters (NAT + Internal)
<img width="1266" height="769" alt="Screen Shot 2025-08-19 at 3 08 46 PM" src="https://github.com/user-attachments/assets/03080f82-04a3-4b8f-bb77-96933a5064fd" />

2. Server Configuration and AD Setup
   - Static IP setup and adapter renaming
   - Install AD DS, promote to domain (`mydomain.com`)
   - Create new admin OU and user, log in with new admin
<img width="752" height="769" alt="Screen Shot 2025-08-19 at 3 30 51 PM" src="https://github.com/user-attachments/assets/8ca91124-94db-41bb-8b11-d17b6b7fdedd" />
<img width="638" height="771" alt="Screen Shot 2025-08-19 at 3 28 47 PM" src="https://github.com/user-attachments/assets/64abfdfc-bf15-44d4-8afa-0049e41a10d3" />

3. **Network Services**
   - Configure NAT using Routing & Remote Access
   - Install and configure DHCP server (172.16.0.100–200 scope)

4. **Automate User Creation**
   - Run PowerShell script to create `_USERS` OU and bulk users (username: first initial + lastname, default password)
<img width="1343" height="699" alt="Screen Shot 2025-08-19 at 3 40 05 PM" src="https://github.com/user-attachments/assets/9df92a6e-c67a-44d2-8326-9e5da822390b" />

5. **Client VM Setup**
   - Create Windows 10 VM (`Client1`), attach to Internal Network
   - Join to domain and test login with domain user
<img width="1343" height="672" alt="Screen Shot 2025-08-19 at 3 53 35 PM" src="https://github.com/user-attachments/assets/e6b6aa85-3c56-4c27-ab89-a079b2ec0bf7" />

