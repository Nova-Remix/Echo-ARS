# JavaScript
Yes, that's right. Donators can now use JavaScript for the servers that they own. WOOT WOOT! The JS is quite limited, meaning there are things you cannot do. An example of this would be trying to use **setTimeout** and **setInterval**. They will not work since Proxy will not allow it. Don't worry, it's still fun as ever!

# Base Command
This is the base command to tell Echo we will be using JS:
```js
#js >>
//Code Here
>>```

# Built-in Variables
| Function Name | Description |
| :---: | :--- |
| **Params** | If you are using {params} key this will carry the data to JS |
| **RawUserID** | Always the command User's ID |
| **UserID** | The User's ID. Compatible with targeting |
| **UserImage** | The User's Profile Picture. Compatible with targeting |
| **Usernick** | The User's Nickname. Compatible with targeting |
| **Username** | The User's Username. Compatible with targeting |
| **RawUsername** | Always's the command User's Username |
| **ServerMembers** | A JSON Object of all the Server Members |
| **ServerRoles** | A JSON Object of all the Server Roles |
| **ServerChannels** | A JSON Object of all Server Channels |
| **ServerOwnerID** | The server owners ID |
| **ChannelID** | The current channels ID |
| **ChannelTopic** | The current channels Topic |
| **ChannelName** | The current channels name |
| **ChannelType** | The current channels type |

# Database Usage
This is how we can use Databases inside of JS. Say we had a database called **Quotes** and had my UserID as a variable. This is what we would do to print out the data within the variable:
```js
.auto .quote={init}
#js >> //Calling the JS
use Quotes; //Grabbing the Database
//resp is the message that gets sent to the channel
resp = Quote[RawUserID]; //DBname[Variable]
>>```
TADA! As simple as that. Now, if we had a variable that looked similar to **USERID-quotes**, then it would be slightly different.
```js
.auto .quote={init}
#js >> //Calling the JS
use Quotes; //Database Name
resp = Quotes[RawUserID + "-quotes"]; //DB[UserID + "Variable"]
>>```
