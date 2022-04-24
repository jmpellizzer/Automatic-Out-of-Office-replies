# Automatic Out of Office replies for Microsoft Office 365
- This Power Automate flow will automatically activate/deactivate your out of office message for an 8 hours shift
  - Week days:
    - Enabled for 930 mins after End shift hours
  - Weekend:
    - Enabled for 3360 from 1am Your Time Zone on a Saturday     
- It runs every day at the end and at the start of your shift
- For the Weekend, it runs on Saturday at 1am in Your Time zone
  - It gets disabled on Monday, at the beginning of your shift
- Display Name, Job Title and Company name attributes are automatically gathered from your Microsoft Office 365 account 
- Shift Hours and Time zone signature attributes are gather from the variables
- A message to your Microsoft Teams account from Power Automate Bot is sent everytime it runs

## Setup
### Importing the flow to your account
1. [Download](https://github.com/jmpellizzer/Automatic-Out-of-Office-replies/raw/main/Automatic%20Out%20of%20Office%20replies.zip 'Download') the flow
2. Go to [Import](https://emea.flow.microsoft.com/manage/flows/import "Import") under **My flows** to import the flow
3. Click **Upload** then select the downloaded `.zip` file
4. Click **Select during import** to choose existent or create new connections for the required resources
5. If connections are present, choose the desired connection, click **Save** and jump to step 14
6. If there are no connections, click **Create new**
7. Click **New connection**
8. Search for the required resources (Office 365 Outlook, Microsoft Teams and Office 365 Users)   
9. Select the resource and click **Create**
10. Log into your Microsoft Office 365 account
11. Connect the remaining resources (Microsoft Teams and Office 365 Users) by repeating the above procedure from step 4
12. Once connections are created, click **Refresh list** > select the connection > **Save**
13. Repeat the above for all three resources (Office 365 Outlook, Microsoft Teams and Office 365 Users)
14. Click **Import**
15. Go to [My flows](https://us.flow.microsoft.com/manage/environments/Default-4b0911a0-929b-4715-944b-c03745165b3a/flows 'My flows')
16. Select the automation flow *(If no automation is shown, refresh the page)*
17. **Edit** the automation to set your desired signature message, shift hours & time zone

### Signature message Week & Weekend:
1. Expand **Condition** > **Condition Week Days** > **Set up automatic replies week days**
2. Expand **Condition** > **Condition Weekend** > **Set up automatic replies weekend**

### Configuring shift hours and time zones:
#### Adjusting trigger time zone:
1. Go to **My flows** in the left-side pane
2. Select the automation flow and click **Edit**
3. Expand **Recurrence** trigger > **Edit** > **Show advanced options**
4. Select the desired **Time zone**

#### Converting from UTC to your desired time zone:
1. Expand **Convert time zone** task and select the desired **Destination time** zone

#### Setting End, Start (military format) and Time zone shift hours for the signature and other tasks:
1. Expand **Set End shift hours** variable and set the **End** of your shift in the **Value** box
`Example: 17:30`
2. Expand **Set Start shift hours** variable and set the **Start** of your shift in the **Value** box
`Example: 09:00`
3. Expand **Set Time zone** variable and set the **Time Zone** in the **Value** box
`Example: CEST`
4. Click **Save** 

### To turn on/off a Power Automation flow:
1. Select the Power Automation flow under **My Flows**
2. Click the three dots vertically aligned for the desired automation, once selected
3. Click **Turn off**
4. To turn it back on, repeat the steps and select **Turn on** for step 3


## Additional information

- Resources in use
  - Office 365 Outlook Connection
  - Office 365 Users Connection
  - Microsoft Teams Connection
 
