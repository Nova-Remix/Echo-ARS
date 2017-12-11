# Does Echo have features regarding music or voice channels?
No, Echo does not have features regarding music or voice channels. The only feature that will be regarding anything with Voice Channels is the Channel Permissions key for Donators. We would love to see Echo with those features; however, this is not the end of the world. There are a lot of good music/audio bots out there.
# How can I let Echo react to other Bots?
You can't, the reason being because we had to take safety precautions Echo. This feature will not be added, so please do not complain and/or ask about it.
# Why does the {joined} key return NaN in some cases?
Discord doesn't always send the correct data therefore causing Echo to replace **{joined}** with NaN instead of the Join Date.
# I forgot Echo's prefix! How do I change it?
By default Echo's prefix will be **.** In case you change it or if you forget it, you can type **@Echo#2101 what is your prefix?** and Echo will tell you the prefix for your server.
# Why does Echo show the trigger when I use {params}?
The trigger with **{params}** is case-sensitive. If you have your command as
```ruby
.auto &.test {params}={init}
You said **{params}**!
```
and you trigger it by typing
```css
.Test Hello There!
```
then Echo will end up adding **.Test** into the **{params}** since you used a capital letter instead of a lowercase letter.
# Am I allowed to use Everything Triggers?
For those who don't know what Everything Triggers are, they are triggers that will be triggered either **every single message** sent or even **most messages** sent. Everything Triggers are ABSOLUTELY forbidden from being used with Echo due to the lag it would cause for everyone else using the bot AND Echo would possibly get banned from Discord due to flooding their API. If anyone is found using an Everything Trigger, they will be **ARS Banned** (Meaning they can no longer create custom commands).
# How do I get access to the Donator Content?
In order for you to be able to use any of this content, you must [donate](https://www.patreon.com/echobot) to the Patreon. All money goes towards paying for hosting Echo on a better VPS. None of it will be used for personal advantages.
# How do I edit a command that already exists?
To edit a command that already exists, all you would need to do is type
```js
.auto <The EXACT trigger that already exists>={init}<Edited Code>
```
# How do I delete a command?
In order to delete a command, all you would need to do is type
```js
.delauto <The EXACT trigger>
```
Want to delete multiple commands at once? Type in
```js
.delauto <Trigger1> .. <Trigger2> .. <Trigger3> .. Etc
```