# agenda-notifications

## SETUP INSTRUCTIONS

1. You'll need to be connected to a Slack Workspace (aka, have a Slack account). If you don't have one, get one know, it's pretty easy.
2. You'll need to create a Slack Webhook URL. If you don't have one follow the instructions below



## AGENDA NOTIFICATIONS SETUP


#### I) Setting Up User Properties
1. Open this [https://script.google.com/d/1JhJC2Ku_bBfxa0C1rgN5JCBSKW7oAZa9GGL1zuOsRtagAel2rJ7-vnFC/edit](Google App Script)
1. Go to File > Project Properties > User Properties
2. Click Add Row
   - Fill name with: CALENDAR_IDS
   - Press on value column (there's no indication of it) and type your desired calendar ids
   - Make sure the ids are comma separated:
   - eg: home@gmail.com, work@gmail.com
3. Click Add Row
   - Fill name with: SLACK_WEBHOOK_URL
   - Press on the value column and paste your slack Webhook Url (if you don't have one or know how to create one, follow the instructions below)
   
#### II) Testing it out ----------------
   - Press on the scripts.gs file (on the left sidebar)
   - Press on the "Select Function" Dropdown on the top toolbar > Select the function "sendEventsForToday"
   - Now press the ▸ button next to the functions selector. 
   - If everything went well you will have received a Slack Notification. If not, review the User properties step

#### III) Setting up daily triggers
- Go to the menu Edit > Current Project's Triggers
- Add a new trigger. Set is as:  time-driven / Day Timer / 7a-8m (or whatever time works best for you)
- You're set!

reach out to me on twitter at @bernatfortet

   
## HOW TO CREATE A SLACK WEBHOOK URL
_You need to be logged in to a slack workspace (aka, account) __do it on your browser___

1. Go to https://api.slack.com/apps
2. Click on Create New App
3. Give it a name. I recommended: "Agenda"
4. Select your workspace. I recommend that you create a personal workspace to keep it isolated from other stuff
5. Click Create App
6. Under "Add features and functionality" click "Incoming Webhooks"
7. The page navigate to the "Incoming Webhooks" page. Now mark "Activate Incoming Webhooks" to On (by pressing on the switch button at the top right)
8. A new section will appear below titled "Webhook URLs for Your Workspace"
9. Click on the button "Add New Webhook to Workspace"
10. Select which channel you want the agenda to be posted
11. A new entry will be created. Under "Webhook Url", you'll se a url. Copy it, this is your slack webhook URL
12. Continue with your AGENDA NOTIFICATIONS SETUP
