# User Keys

These keys will grab the ID/Username/Nickname of a user.

# Key List

| Key | Description |
| :---: | :--- |
| **{rawid}** | Grabs the user's ID. Compatible with targeting \(@mentions\) |
| **{/rawid}** | ALWAYS prints out the command user's ID. |
| **{/user}** | Prints out user's Username \(Not their nickname\). Compatible with targeting \(@mentions\). |
| **{usernick}** | Prints out the user's nickname. Compatible with targeting \(@mentions\). |
| **{self}** | Returns the command user's username. |

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



