# Delete Keys AND Clear Keys
Delete keys are something a lot of people enjoy to use for many reasons. One reason could be for deleting messages to keep a channel clean.

# Key List
| Key | Description |
| :---: | :--- |
| **{del}** | Deletes the user's message either instantly or after **x** time. |
| **{delme}** | Deletes the bots message either instantly or after **x** time. |
| **{del*}** | Echo will **NOT** delete bot master's messages. |
| **{delauto}** | Deletes the entire command from the A.R.S file after being triggered. |
| **{clear}** | Clears either 5 messages or **x** amount of messages in the channel. |
| **{tclear}** | Clears either 5 or **x** amount of messages from the user who used the command \(or whomever was mentioned\) |

# Usage
**{del}**
```ruby
.auto .test={init}
{del}
Your message was deleted!
```
```ruby
.auto .test={init}
{del:5s}
Your message will be deleted after 5 seconds!
```

**{delme}**
```ruby
.auto .test={init}
{delme}
My message will be deleted immediately.
```
```ruby
.auto .test={init}
{delme:5s}
My message will be deleted after 5 seconds!
```

**{del*}**
```ruby
.auto .test={init}
{del*}
Your message will be deleted, unless you're a Bot Commander. ;)
```

**{delauto}**
```ruby
.auto .test={init}
{delauto}
This rule will work once. Try to use the trigger again. :)
```

**{clear}**
```ruby
.auto .test={init}
{clear}
I have cleared 5 messages from the channel!
```
```ruby
.auto .test={initunit}
{clear:6}
I have cleared 6 messages from the channel!
```

**{tclear}**
```ruby
.auto .test={init}
{tclear:5}
I have cleared 5 of your messages!
```
