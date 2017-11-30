# User Keys
These keys will grab the ID/Username/Nickname of a user.

# Key List
| Key | Description |
| :---: | :--- |
| **{rawid}** | Grabs the user's ID. Compatible with targeting.|
| **{/rawid}** | ALWAYS prints out the command user's ID. |
| **{/user}** | Prints out user's Username \(Not their nickname\). Compatible with targeting. |
| **{usernick}** | Prints out the user's nickname. Compatible with targeting. |
| **{self}** | Returns the command user's username. |
| **{usericon}** | Grabs the user's profile pciture picture and sends it to the channel. |
| **{nickname}** | Changes the user's nickname |

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

**{/user}**
```ruby
.auto &.test={init}
The user's Username is **{/user}**!
```

**{usernick}**
```ruby
.auto &.test={init}
The user's Nickname is **{usernick}**
```

**{self}**
```ruby
.auto &.test={init}
The user's Username is **{/user}**, and the person who ran the command is **{self}**
```

**{usericon}**
```ruby
.auto .test={init}
{user}'s Profile Picture: {usericon}
```

**{nickname}**
```ruby
.auto .test={init}
{nickname:Hue}
I have changed your nickname to **Hue**
```