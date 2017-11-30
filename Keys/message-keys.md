# Message Keys
The message keys will include:
* Redirecting Messages
* Embeds
* Reactions
* Messaging certain channels (or users)
* etc...

# Key List
| Key | Description |
| :---: | :--- |
| **{msg}** | Sends a message to the channel that the command was used in, even if there was a redirect in the command |
| **{redirect}** | Redirects a message to the channel (using Channel ID's). **NOTE:** Some keys are bugged when using redirects |
| **{pm}** | DM's the User that used the command, the mentioned person, or you can DM specific user's with their User ID's |
| **{embed}** | Sends a sexy embed. Absolutely wonderful. |
| **{greet}** | Shows the Greet Message for the server |
| **{bye}** | Shows the Bye Message for the server |
| **{alert}** | Alerts someone if the trigger was used |
| **{react}** | Echo will react to the last message |
| **{reactbot}** | Echo will react to its own message (A MESSAGE MUST BE SENT) |
| **{reactme}** | Echo will react to the current message |
| **{pin}** | Echo will pin the message to the channel |
| **{content}** | Grabs the content of the message |
| **{clean}** | (Used when using {content}) Gets rid of the trigger from the message it is collecting the content from |
| **{params}** | Works just like {content}, except the trigger is already removed from the message it collects |