# Sleep Keys
Sleep keys are something a lot of people enjoy to use for many reasons. Some reasons could be for deleting messages, others can be for making games and whatnot.

## Key List
`{sleep:time}`
You **MUST** change `time` to the amount of **Seconds**(s), **Minutes**(m), or **Hours**(h) that you want the command to wait for BEFORE it posts the message and/or does the command.

## Usage
```ruby
.auto .test={init}
{sleep:3s}
The sleep key worked!
```

### NOTE
This will sleep your ENTIRE command! If you only want certain things to wait before being triggered, I suggest linking to other rules. If you want to just sleep a message you want sent to the channel, then the next key can be useful for you.
