#Mention Keys
Mention keys will mention anything (a user, a channel, a role, etc) and/or will either require/disallow mentions for a command. They can come in handy if people are spamming commands and don't know who Echo is responding to.

#Key List
`{user}` - Mentions the user that triggers the command OR the person that you mention when using the command.
`{here}` - Does the @here mention
`{everyone}` - Mentions @everyone
`{mention}` - Requires a mention in order to use the command
`{-mentions}` - Prevents keys from directing to mentioned user.

#Usage
**{user}**
```ruby
.auto .test={init}
This will mention the person who uses the command, {user}!
```
```ruby
.auto &.test={init}
This will work if you mention a user or don't mention anyone at all, {user}!
```

**{here}**
```ruby
.auto .test={init}
This is just a test, {here}!
```

**{everyone}**
```ruby
.auto .test={init}
Sorry to mention {everyone}, but this is just a test!
```

**{mention}**
```ruby
.auto &.test={init}
{mention}
This command will not work unless you do .test @user!
```
```ruby
.auto &.test={init}
{mention:This message will send if there was no mention found in the command!}
And this message will send if there was a mention found!
```

**{-mentions}**
```ruby
.auto &.test={init}
{-mentions}
Even if there was a mention found in the command, {user} will ping the person who ran it!
```