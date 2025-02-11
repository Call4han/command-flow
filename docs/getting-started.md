## Getting Started

Welcome to the `command-flow` documentation

CommandFlow is a flexible command framework which removes lots of
boilerplate code used in commands

The command framework is divided into two parts. One is the actual
command framework and the other one is the API to allow creation of
a complete command tree based on annotations

### Components of the Command Framework

There are some basic components that you should at least be aware of to use **CommandFlow**
- **Command:** This is the most fundamental component, the **Command**. It contains all the information related to a command, included but not limited to name, aliases, permission, parts, etc.
  Those are created using the `Command.builder(String)` method, which returns an `Command.Builder` instance where you can set all the information of the command.

- **CommandPart:** This is the second most fundamental component, it can be understood as every argument of a **Command**, including things like subcommands, flags, non positional arguments, etc. It can use arguments from the argument list, or provide them using any other means also they can forward the parsing to another part and just act as a modifier. Most of the default parts can be found at the class `Parts`

- **CommandContext**: This is a mutable object which contains the context for the called command including but not limited to the values for every part parsed, the raw arguments list and the raw arguments for every part, the labels and the Command execution path(which path of subcommands was taken).


### Known bugs or misbehaviours
The next list are the known bugs that must be resolved at some point:
- No known bugs at the moment.
