# Example Bot Repo

Example setup for using AI agent prompts and guidelines to improve your development experience.

This setup can be applied to any codebase.

## Agent Guides

This repository provides guidance for working with AI agents in your development workflow. The following guides are available:

- [Agent Setup Guide](AGENT_SETUP_GUIDE.md) - Detailed instructions for setting up and using AI agents with your codebase, including demos, examples, and best practices.

Additional guides may be added in the future as we expand our agent-based development tools and practices.


## Agent Only

Agents: For local, not-checked-in guidance, use the `./.agent` directory. If it does not exist, create it. Place an empty `.aiignore` file in the project root. Ensure `.agent/` is listed in `.gitignore`.

- Analyze all markdown files in `.agent` for instructions and context.
- If `.agent/conversation-savepoint.md` does not exist, create it for saving and resuming chats.
- Store all new agent-generated guidance in `.agent`.
- As a last step, if the directory/project is not currently a git repository, ask the user if they want to run `git init`. If the user agrees, run `git init` to create the repository.
