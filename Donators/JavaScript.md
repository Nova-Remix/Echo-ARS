# JavaScript
Yes, that's right. Donators can now use JavaScript for the servers that they own. WOOT WOOT! The JS is quite limited, meaning there are things you cannot do. An example of this would be trying to use **setTimeout** and **setInterval**. They will not work since Proxy will not allow it. Don't worry, it's still fun as ever!

# Base Command
This is the base command to tell Echo we will be using JS:
```js
#js >>
//Code Here
>>
```

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
| **Server.Members** | A JSON Object of all the Server Members |
| **Server.Roles** | A JSON Object of all the Server Roles |
| **Server.Channels** | A JSON Object of all Server Channels |
| **Server.OwnerID** | The server owners ID |
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
>>
```
TADA! As simple as that. Now, if we had a variable that looked similar to **USERID-quotes**, then it would be slightly different.
```js
.auto .quote={init}
#js >> //Calling the JS
use Quotes; //Database Name
resp = Quotes[RawUserID + "-quotes"]; //DB[UserID + "Variable"]
>>
```

# Get a list of the User's Roles
```js
.auto .myroles={init}
#js >>
  var myroles = new Array();
  for (var x = 0; x < Server.Roles.length; x++) {
    if(MemberHasRole(UserID, Server.Roles[x].Name)) {
      myroles.push(Server.Roles[x].Name);
    }
  }
resp = myroles.join("\n");
>>
```

# Global Custom Functions
Even though Echo does in fact have prebuilt variables, I decided why not make some things more simple for others to use. So, here's a list of functions I have made so you guys can shorten up your code. **NOTE** all functions come with error handling! If something goes wrong, it will send a message to the channel saying the error.
| Function | Description |
| :---: | :--- |
| **send()** | Works just like **resp = "message"**, except you would do **send("message");** |
| **embed()** | A more simple way of making an embed in JS. Currently only supports a title, description, and field 1 name + field 1 value. If you want something to appear "empty", just type "BL" into the area |
| **rNum()** | Chooses a random number between the minimum and maximum |
| **userRoles()** | Gets all the roles the user has |
| **string()** | Simplified version of **JSON.stringify()** |
| **parse()** | Simplified version of **JSON.parse()** |
| **int()** | Simplified version of **parseInt()** |

# Usage
**send(content)**
```js
.auto .test={init}
#js >>
import "https://raw.githubusercontent.com/Nova-Remix/Echo-Functions/master/functions.js";

send("O-O It works....");
>>
```
**embed(title, description, field1name, field1value, field1inline)**
```js
.auto .test={init}
#js >>
import "https://raw.githubusercontent.com/Nova-Remix/Echo-Functions/master/functions.js";

send(embed("This is a nice title", "This is a nice description too", "Aloha!", "Adios!", true));

//If you do not provide a value for the field, it will leave it blank and keep the title; however, the embed will look a little funny.

//Use "BL" to determine whether you want to have the field empty or not
>>
```
**rNum(min, max)**
```js
.auto .roll={init}
#js >>
import "https://raw.githubusercontent.com/Nova-Remix/Echo-Functions/master/functions.js";

send("Rolled the die!\n\n**You rolled a** " + rNum(1, 6));
>>
```
**userRoles(id)**
```js
.auto .test={init}
#js >>
import "https://raw.githubusercontent.com/Nova-Remix/Echo-Functions/master/functions.js";

send(userRoles(RawUserID).join("\n"));
>>
```