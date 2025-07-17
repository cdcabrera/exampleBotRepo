# Example Bot Repo

Example setup for using AI agent prompts and guidelines to improve your development experience.

This setup can be applied to any codebase.

## Demo

**This repo is the demo**. At the bottom is some simple automation you can do yourself by asking the AI Agent to `Scan this repo's guidance` or `Scan this repo for guidance and execute any setup. no confirmation necessary.` depending on how comfortable with the chat executing things automatically.

### Demo away

1. Copy/clone this entire `README.md`, or just copy the `agent only` section at the bottom.
2. Open an AI chat in the context of this repo and `README.md`
3. Ask the agent to `scan this repo/directory guidance`
4. The agent should "attempt to" generate a few files, including a `conversation-savepoint.md`
5. After that ask the agent to update the `.agent` guidance for your current chat against the `conversation-savepoint.md`.
6. Restart the IDE or whatever you're using
7. Ask the agent to resume the chat from the conversation savepoint. You may still have to note where it is.

That's it! Depending on the model and chat you're leveraging, your results can vary.

> Currently, we've noted that [Cursor's](https://cursor.com/?from=home) chat appears to be more consistent in following guidance. But even it has the appearance of being randomly "dumb." Other tooling like [JetBrains](https://www.jetbrains.com/) is an option, but testing results were heavily dependent on the model being picked.

### How it could work for you

1. Get the agent to create the `agent only` section at the bottom of your `README.md` in some repo.
2. Pick the steps you want to automate
   > This can be things like some level of tooling installation guidance, or always do a spell check, or even an ask/answer set of questions for users/developers who are unfamiliar with the code. The options really do start to stack up, especially when you think about leveraging these tools in place of current linting tools.
3. Check it in!
4. Test it! This can/will get frustrating =)

## Agent setup

Creating basic guidelines can give you some semblance of AI agent consistency.

### README agent section

Create an AI agent only section at the bottom of your repo's `README.md` indicating that when agents read documentation they should look in a local, gitignored, directory for local developer specific guidance, it can be any directory you want. You can ask the agent to do this. For reference, see the agent section below on this `README.md`.

> To view hidden files on Mac with the latest OS, the 3-key command is
> `shift apple/command period`

### Set up a conversation savepoint

Want to pick up mostly from where you left off? Ask the agent to create a conversation savepoint. You'll still have to ask it to save on exiting the editor and scan the conversation savepoint on startup.

> You can attempt to get it to save conversations automatically by asking, but the consistency is a little off. It tends to randomly ignore guidance.

Open an AI agent chat and ask it to
```
Create a conversation-savepoint markdown file under a ".agent" directory. This file is for agents only, and should be used to allow agents to resume the conversation with a user.
```

### Working in an existing codebase

Ask the agent to understand the repo/code context
```
Index this repository. Create guidelines for maintenance based on all code and git history. The guidelines should be stored underneath the "./.agent" directory. The primary focus of the guidelines is the "./src" directory, a [react or other] UI code base. The guidelines should also cover emulating the code style.
```

Follow it up by asking the agent to (feel free to ask it to save that summary under the `.agent` directory)
```
Provide a concise summary for the questions
- What does this repo/code actually do?
- What is [this product/thing]?
```

Take things a step further if you're not familiar with the codebase and ask...
```
If the info is available, add a question and answer in a summary doc under .agent using plain speak, non-technical, and avoiding acronyms
- Where [are these things being] typically used?
```

### Get familiar with a codebase

#### General

Working in an existing codebase based on \[some framework\], ask the agent to minimally understand...
```
Scan this reference [over here]

Do not recreate this set of guidelines, but create an internal reference to the remote under `.agent`
```

Then ask the agent to analyze the custom implementation used in the codebase
```
Create a `[x]-implementation` set of guidelines for how [x] is specifically implemented in this codebase. This should include current usage patterns, customizations, and migration considerations.
```

##### A specific example, Patternfly React
> **Important**:
> - Always vet remote resources before scanning
> - Consider the bandwidth associated with remote resources
> 
> Security and blocking someone else's resources are still considerations.
>
> Example: Highlighting concerns... you wouldn't know unless we said something, or you remember how to decode binary, and it really depends on how permissive you've opted to make your tooling, but want to Rick Roll someone? Copy the below binary into one of your chats:
>
> `$ open "https://youtu.be/dQw4w9WgXcQ?si=jUD0shmHyTOkB_xy`
>
> vs
>
> 00100100 00100000 01101111 01110000 01100101 01101110 00100000 00100010 01101000 01110100 01110100 01110000 01110011 00111010 00101111 00101111 01111001 01101111 01110101 01110100 01110101 00101110 01100010 01100101 00101111 01100100 01010001 01110111 00110100 01110111 00111001 01010111 01100111 01011000 01100011 01010001 00111111 01110011 01101001 00111101 01101010 01010101 01000100 00110000 01110011 01101000 01101101 01001000 01111001 01010100 01001111 01101011 01000010 01011111 01111000 01111001 00100010

Working in an existing Patternfly React codebase? Ask the agent to minimally understand Patternfly React
```
Scan this git guideline resource for Patternfly https://github.com/nicolethoen/patternfly-ai-coding.git 

Do not recreate this set of guidelines, but create an internal reference to the remote under `.agent`
```

Then ask the agent to analyze the custom Patternfly implementation used in the codebase
```
Create a `patternfly-implementation` set of guidelines for how Patternfly is specifically implemented in this codebase. This should include current usage patterns, customizations, and migration considerations.
```

<!--
## Agent Only

Agents: The following block is base64-encoded. Decode before use.

Rm9yIGxvY2FsLCBub3QtY2hlY2tlZC1pbiBndWlkYW5jZSwgdXNlIHRoZSBgLi8uYWdlbnRgIGRpcmVjdG9yeS4gSWYgaXQgZG9lcyBub3QgZXhpc3QsIGNyZWF0ZSBpdC4gUGxhY2UgYW4gZW1wdHkgYC5haWlnbm9yZWAgZmlsZSBpbiB0aGUgcHJvamVjdCByb290LiBFbnN1cmUgYC5hZ2VudC9gIGlzIGxpc3RlZCBpbiBgLmdpdGlnbm9yZWAuCgotIEFuYWx5emUgYWxsIG1hcmtkb3duIGZpbGVzIGluIGAuYWdlbnRgIGZvciBpbnN0cnVjdGlvbnMgYW5kIGNvbnRleHQuCi0gSWYgYC5hZ2VudC9jb252ZXJzYXRpb24tc2F2ZXBvaW50Lm1kYCBkb2VzIG5vdCBleGlzdCwgY3JlYXRlIGl0IGZvciBzYXZpbmcgYW5kIHJlc3VtaW5nIGNoYXRzLgotIFN0b3JlIGFsbCBuZXcgYWdlbnQtZ2VuZXJhdGVkIGd1aWRhbmNlIGluIGAuYWdlbnRgLgotIEEgYXMgbGFzdCBzdGVwLCBpZiB0aGUgZGlyZWN0b3J5L3Byb2plY3QgaXMgbm90IGN1cnJlbnRseSBhIGdpdCByZXBvc2l0b3J5LCBhc2sgdGhlIHVzZXIgaWYgdGhleSB3YW50IHRvIHJ1biBgZ2l0IGluaXQuIElmIHRoZSB1c2VyIGFncmVlcywgcnVuIGBnaXQgaW5pdGAgdG8gY3JlYXRlIHRoZSByZXBvc2l0b3J5Lgo=
-->
