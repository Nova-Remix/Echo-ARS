# Sleep Keys

Sleep keys are something a lot of people enjoy to use for many reasons. Some reasons could be for deleting messages, others can be for making games and whatnot.

## Key List

| Key | Description |
| :---: | :--- |
| **{sleep}** | Sleeps the entire command for x amount of [time](README.md) |
| **{time}** | Sends a message after x amount of [time](README.md) while the rest of the command takes effect immediately. |

## Usage

**{sleep}**

```ruby
.auto .test={init}
{sleep:3s}
{del}
The sleep key worked!
```

**{time}**

```ruby
.auto .test={init}
{del}
The message was deleted and this message was sent first!
{sleep}
{time:3s}
This message was sent 3 seconds later!
{/sleep}
```



