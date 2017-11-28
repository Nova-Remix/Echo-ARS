# Sleep Keys
Sleep keys are something a lot of people enjoy to use for many reasons. Some reasons could be for deleting messages, others can be for making games and whatnot.

## Key List
`{sleep:SLEEPFOR}`

`{sleep}{time:SLEEPFOR}{/sleep}`

You **MUST** change `SLEEPFOR` to the amount of **Seconds**(s), **Minutes**(m), or **Hours**(h) that you want the command to wait for BEFORE it posts the message and/or does the command.


## Usage
**{sleep:SLEEPFOR}**
```ruby
.auto .test={init}
{sleep:3s}
{del}
The sleep key worked!
```

**{sleep}{time:SLEEPFOR}{/sleep}**
```ruby
.auto .test={init}
{del}
The message was deleted and this message was sent first!
{sleep}
{time:3s}
This message was sent 3 seconds later!
{/sleep}
```

# Note
`{sleep:3s}` will sleep your ENTIRE command! If you only want certain things to wait before being triggered, I suggest linking to other rules. If you just want to sleep a message you want sent to the channel, then the `{sleep}{time:3s}` key can be useful for you.