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
| **{split}** | Used with the **{params}** key to split a message into multiple parts |

# Usage
**{msg}**
```ruby
.auto .test={init}
{redirect:ChannelID}
This message was redirected to another channel!
{msg:This message is sent to the channel the command was used in!}
```
**{redirect}**
```ruby
.auto .test={init}
{redirect:CHANNELID} //Replace CHANNELID with the Channel's ID you want to Redirect to
This was redirected to a different channel! WHOOPEE!
```
**{pm}**
```ruby
.auto .test={init}
{pm}
I just slid into your DM's.
```
```ruby
.auto .test={init}
{pm:USERID,ANOTHERID,ETC}
You can PM specific people by using their UserID and separating them with a comma!
```
**{embed}**
```ruby
{embed:
	{title:}
	//Insert the title here
	{type:rich}
	//This is always rich as discord does not have any other types
	{author|name:}
	//Insert the author name (={user}) here
	{author|icon:}
	//This can be used to display a little picture next to the author name
	{author|url:}
	{color:}
	//Insert a colour here (HEX-colors only)
	{thumb|url:}
	//Inserts a small picture in the top right of the embed, can be replaced with {usericon} or related
	{desc:}
	//Your entire description goes here, again {user}, {/user} and related can be used
	{footer|icon:}
	//An icon url goes here ({usericon} or related can also be used) This icon will be displayed at the bottom of the embed
	{footer|text:}
	//Text that should go alongside the {footer|icon:} goes here
}
```
```ruby
.auto .server={init}
{embed:
    {title:Information for {guild|name}}
    {type:rich}
    {author|name:{owner|name}}
    {author|icon:{owner|avatar}}
    {author|url:{owner|avatar}}
    {color:
        {randlist:
             #ff0000,#00ff00,#ffffff,#4286f4,
             #f45642,#262525,#e2d626,#87e226,
             #26e2c0,#2633e2,#8126e2
        }
    }
    {thumb|url:{guild|icon}}
    {desc:
───────────────────────
× ID:                     {guild|id}
× Region:             {guild|region}
× OwnerID:        {owner|id}
× Discord Icon:  [Click to view Guild Icon]({guild|icon})
× Members:       {membercount}
× Channels:        {channelcount}
× Roles:               {rolecount}
───────────────────────
    }
    {footer|icon:https://xtclabs.net/img/favicon-new.png}
    {footer|text: Echo 2.0 A.R.S}
}
```
```ruby
.auto .echo={init}
{embed:
    {type:rich}
        {color:
            {randlist:
                #4286f4,#ff0000,#00ff00,
                ##e8f442,#f49e42,#000000
            }
        }
    {image|url:https://xtclabs.net/img/EchoIcon.jpg}
    {image|width:250}
    {image|height:250}
    {field[0]|name:Echo}
    {field[0]|value:[Echo Official Website](https://proxikal.github.io/Echo/Commands "The Official website for Echo 2.0")}
    {field[0]|inline:true}
    {field[1]|name:Echo Help}
    {field[1]|value:[Echo Documentation](https://github.com/proxikal/Echo "Learn how to use Echo A.R.S Through some Examples.")}
    {field[1]|inline:true}
    {field[2]|name:PHP Webhooks}
    {field[2]|value:[Github Page!](https://github.com/proxikal/discordphp-webhook "Use discord webhooks with ease using DiscordPHP-Webhooks")}
    {field[2]|inline:true}
    {footer|text:Requested by: {/user}.}
    {footer|icon:{usericon}}
}
```
**{greet}**
```ruby
.auto .mygreet={init}
The greet message for your server is **{greet}**
```
**{bye}**
```ruby
.auto .mybye={init}
The bye message for your server is **{bye}**
```
**{alert}**
```ruby
.auto .test={init}
{alert:USERID} //Change USERID to the User's ID you want to alert
This message will send to the channel the command was used in! Echo has its own way of saying who used the command!
```
**{react}**
```ruby
.auto &.test={init}
{react: :x:}
I have reacted to the above message!
```
**{reactbot}**
```ruby
.auto .test={init}
Hey look! I can count to 3 with reactions!
{reactbot: :one: :two: :three:}
```
**{reactme}**
```ruby
.auto .test={init}
{reactme::one:}
I reacted to your message, {user}!
```
**{pin}**
```ruby
.auto .pin={init}
{pin}
Your message was pinned, {self}!
```
**{content}**
```ruby
.auto &.test={init}
**{content}**
//If you type
//.test Testing things
//it will come out as
//.test Testing things
```
**{clean}**
```ruby
.auto &.test={init}
{clean}
**{content}**
//If you type 
//.test Testing things
//it will come out as
//Testing things
```
**{params}**
```ruby
.auto &.test {params}={init}
You said **{params}**!
//It just captures everything you say
//AFTER the trigger
```
**{split}**
```ruby
.auto &.test {params}={init}
{split: }
{/p0} //Captures the first word of your text after the trigger
//It will split every word that is in between spaces
{/p1}
```
```ruby
.auto &.test {params}={init}
{split: - }
//Text - Like - This
//Will come out as
{/p0} //Text
{/p1} //Like
{/p2} //This
```