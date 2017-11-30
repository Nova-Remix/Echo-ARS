# Creating a Custom Command
To create a command, all you must do is type in **.auto** then the trigger.

# What is a Trigger?
A trigger is what the user must say in order for the command to active. For instance, if I wanted to have people type **.echo** to activate the command, I would do:
```ruby
.auto .echo={init}```
After that, I would simply put in what I would want the command to do.

# When to use &
As most people already know, you can also do **.auto &.echo** as a trigger. DON'T WORRY, the user won't have to type **&.echo** to trigger the command. The **&** is used when you want the command to be triggered WHEREVER in the message the trigger is found. Sounds confusing, but it's quite simple. For an example, I can type in **Type in .echo to use the command**. The command would trigger since **.echo** was found in the command.

You will also use **&** if you use the **{params}** key in your trigger. Well, it's required to use **&**. If you didn't, Echo will automatically add it for you.