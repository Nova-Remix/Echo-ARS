# Editing Roles
What you must do is make sure Echo's role is above the role you're wanting to edit. If it is not above, then this will not work. The only thing you can really do with this is change role colors. No worries, it will be updated soon! I hope. Anyways, let's get into this piece of cake shall we?

# Key List
| Key | Description |
| :---: | :--- |
| **{editrole}** | Tells Echo we will be editing the role! :D |
| **{rolename}** | The role name will be the role you want to edit, not what you want to change the role's name to |
| **{rolecolor}** | The color we want to apply to the role. The key uses HEX Codes (#RRGGBB) |

# Usage
```json
.auto &.test {params}={init}
{editrole:
  {rolename:ROLE}
  {rolecolor:{params}} //Hot Pink
}
I have applied the color {params} to the role ROLE.```
```json
.auto .test={init}
{editrole:
  {rolename:Test}
  {rolecolor:#ff69b4} //Hot Pink
}
I have applied the color Hot Pink to the role Test```
