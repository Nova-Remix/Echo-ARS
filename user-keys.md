# User Keys

These keys will grab the ID/Username/Nickname of a user.

# Key List

| Key | Description |
| :---: | :--- |
| **{rawid}** | Grabs the user's ID, either the command user \(if no mention is found\) or the mentioned user \(if a mention is found\). |
| **{/rawid}** | This will ALWAYS print out the command user's ID, even if there was a mention found. |
| **{/user}** | Prints out user's Username \(Not their nickname\). Compatible with targeting \(@mentions\). |
| **{usernick}** | Prints out the user's nickname. Compatible with targeting \(@mentions\). |
| **{self}** | Returns the command user's username. Doesnt Doesn't matter if there was a mention found in the command or not. |

# Usage

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



