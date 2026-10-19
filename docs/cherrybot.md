# The Cherrybot

## Setup

Here are some basic steps on how to first get started with the bot. 
If anything ever doesn't work, you should probably check if you have everything done here. 
I generally recommend you to check the documentation if anything ever breaks. If this doesn't fix it, the root is something
that most definitely but perchance occasionally possibly may have been my fault. Oops.


Before anything else, the most important command:  

- type `%report [text]` to have a message sent to me directly  
Whether you have a problem, want to suggest something, whatever. The text will be given to me via bot logs and I will read it ASAP. 

### Setting up an admin role

- this can only be done by the server owner
- there can only be one role capable of cherrybot-privileges
- please make sure only trusted members have this role
- type `%admin_add @[some_role]`
- type `%adminrole` to see the current admin role

### Setting up a welcome channel

- this assigns a specific channel from your server where a welcome message will be sent
- this can only be done by someone with the local cherrybot admin role
- use `%welcome_add [mention-channel]` to set a new channel or replacing the old one
- use `%welcome_remove` to remove the local channel assignment
- use `%welcome_see` to see your local channel assignment)

### Reaction-role messages

Work in progress.

### Using the to-do feature

There is a server-stored to-do list connected to each cherrybot user. The list is created upon first using a to-do related command.

- use `%todo see` to view your to-do list content
- use `%todo add [task]` to add [task] to your to-do list
- use `%todo remove [index]` to remove the [index]-th task from your to-do list
- use `%todo` to quick view an explanation for the three commands

### WolframAlpha Plugin

Work in progress.

### Admin utilities

- use `createrole [hex] [role name]` to create a role called [role name] with color [hex]

### Fun commands

Work in progress. 

### Cherrybot Troubleshooting

- use `%stats` to see the amount of servers the bot is employed in + total user count
- use `%ping` to see the bot latency; useful for testing bot activity / downtime
- use `%uptime` to see time amount of the current bot instance. please report if you notice an oddly low time amount

### Passive bot functions

- the cherrybot sends a welcome message whenever someone joins the server, given that a welcome channel was set up by an admin
