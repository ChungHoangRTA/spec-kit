# Qwen CLI Support

Spec Kit now supports Qwen CLI as an AI coding agent for Spec-Driven Development.

## Installation

To use Qwen CLI with Spec Kit, you'll need to install the Qwen CLI tool first:

```bash
npm install -g @qwen-code/qwen-code
```

For more information on installing Qwen CLI, visit the [Qwen Code GitHub repository](https://github.com/QwenLM/qwen-code).

## Usage

When initializing a new Spec Kit project, you can select Qwen CLI as your AI assistant:

```bash
specify init <project_name> --ai qwen
# Or in the current directory:
specify init --here --ai qwen
```

You can also skip the AI tool check if you want to initialize a project without having Qwen CLI installed:

```bash
specify init <project_name> --ai qwen --ignore-agent-tools
```

## Commands

Qwen CLI uses the same commands as Gemini CLI. Once your project is set up with Qwen CLI support, you can use the following commands in your Qwen CLI session:

- `/specify` - Create a new feature specification and branch
- `/plan` - Generate an implementation plan for your feature
- `/tasks` - Break down the plan into executable tasks

These commands work the same way as with other AI assistants, following the Spec-Driven Development methodology.

## Packaging

Qwen CLI templates are packaged based on the Gemini CLI templates, ensuring consistent functionality across both platforms. When a new release is created, the packaging workflow automatically generates a Qwen-compatible package by adapting the Gemini templates.

## Agent Context File

When using Qwen CLI, Spec Kit will generate a `QWEN.md` file in your project root that provides context about your project's technologies, structure, and commands. This file is automatically updated as you add new features to your project.