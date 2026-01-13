## 13.01.2026 - released v2.4 solution package
- now contains v3 nudging logic
- removed premium connector to Entra
- built solely on standard connectors now

### Admin experience
- added counter to message send action
- flow status message now contains sent messages count <br><br>
<img width="222" height="118" alt="image" src="https://github.com/user-attachments/assets/64da8dad-1959-4a18-a8fd-63d9b12d4047" /><br><br>

### Solution variables & architecture
- added connection entra_connect --> uses standard connector
- simplified flow layout for 
- removed connections
 - excel_connect
 - sharepoint_connect
 - pre-authorized entra connection


## 12.01.2026 - released v2.31 solution package
- quick fix to get solution functional again, viable was missing

### Solution variables & architecture
- added environment variable group_id --> string --> contains nudge group id

## 12.01.2026 - released v2.3
### User experience
- nudges now as formatted Adaptive cards
- nudges contain button to hand over directly to agent within M365 Copilot WebApp <br><br>
<img width="222" height="118" alt="image" src="https://github.com/user-attachments/assets/52a32d18-23d2-4b05-8af5-143871fa0afd" /><br>

### Admin experience
- added flow success nudge in Teams Chat <br>
<img width="222" height="118" alt="image" src="https://github.com/user-attachments/assets/5d62dca2-1a2f-40ba-9148-f27e5cad5243" /> <br>
- added proactive nudges for possibly unwanted flow events --> directing on issue resolution <br>
<img width="222" height="118" alt="image" src="https://github.com/user-attachments/assets/53de0f6c-d8e0-41df-aacd-05210b41cdf6" /><br>
<img width="222" height="118" alt="image" src="https://github.com/user-attachments/assets/e6445932-febc-4788-bf2c-d056c1c99e16" /><br>
- added testmode nudge in Teams Chat to check basic functionality <br>
<img width="222" height="163" alt="image" src="https://github.com/user-attachments/assets/3c610280-7147-4de6-acfa-6ba951c5e881" /><br>

### Agent Code
- reworked source for better performance and increased reliability
- now yaml based syntax for perfect interpretion by Copilot
- reworked sample prompts for better readability
- added de/en language switch to respect browser / system preferences
- fixed some minor issues

### Solution variables & architecture
- added environment variables to 
  - centralize administration
  - setting most variables during solution import
  - improve failure resistance
  - improve flow logic
- added environment variables:
  - admin_user --> string --> contains admin mailaddress to send status nudges in Teams Chat
  - testmode_enabled --> boolean --> exit logic in flow to prevent unwanted nudging during setup
  - nudging_enabled --> boolean --> exit logic in flow to prevent unwanted nudging
  - nudge_group_id --> text --> contains Entra ID group id where all nudge receipients are in
  - campaign_start_date --> string --> exit logic in flow to prevent unwanted nudging outside campaign timeframe
  - campaign_end_date --> string --> exit logic in flow to prevent unwanted nudging outside campaign timeframe
  - agent_app_id --> string --> needed for nudging funtionality
  - agent_title_id --> string --> needed for URL construction to handover conversation from Teams Chat to M365 Copilot WebApp

### Solution Flow
- defined exit criteria on set variables
  - testmode_enabled == true: only testnudge to admin || false: nudges delivered to everyone
  - nudging_enabled == true: nudges will be sent in Teams Chats || false: no nudges are sent (except admin info)
  - [today] >= campaign_start_date AND <= campaign_end_date: nudges will be send // else: info nudge to admin
