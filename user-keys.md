#User Keys
These keys will grab the ID/Username/Nickname of a user.

#Key List
**{rawid}** - Grabs the user's ID, either the command user (if no mention is found) or the mentioned user (if there was a mention).
**{/rawid}** - This will ALWAYS print out the command user's ID, even if there was a mention found.
**{/user}** - Prints out the user's username (NOT THEIR NICKNAME)
**{usernick}** - Prints out the user's nickname.
**{self}** - Returns the command user's username.

#Usage
**{rawid}**
```ruby
.auto &.test={init}
{user}'s ID is **{rawid}**
```

**{/rawid}**
```ruby
.auto .test={init}
The command user's ID is **{/rawid}**!
```