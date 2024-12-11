# Learning Claude MCP

Dec 2024
[Steve Chambers](https://viewyonder.com)

Docs and code to learn and explore Claude MCP.

## Introduction

This is a live working set of documents and code to learn and explore Claude MCP. The code is written in Python and uses the Claude MCP library.

I did this work while also learning Zed as my new IDE. Zed is also configured with Claude Sonnet as the AI assistant (inline and chat).

## Table of Contents

- [Using Zed and Claude AI Assistant](#using-zed-and-claude-ai-assistant)
- [Building a CLI Host App with Claude MCP](#building-a-cli-host-app-with-claude-mcp)

## Using Zed and Claude AI Assistant

Ok, so this is not specific to Claude MCP -- though there is an MCP Protocol piece -- but I'm learning Zed at the same time (two birds with one stone, ay? 😜 ).

Call me old fashioned but I read the [Zed Assistant Documentation](https://zed.dev/docs/assistant/assistant) first. It's like a pre-warm routine for my brain... Here's the main things I'm doing with Zed and AI, with links to offical Zed docs if you need more juice...

1. [Assistant (chat) panel](#assistant-chat-panel).
2. [Inline assistant](#inline-assistant).
3. [Configure the AI assistant](#configure-the-ai-assistant).
4. [Using previous contexts](#using-previous-contexts).
5. [Using slash commands](#using-slash-commands).
6. [Using the prompt library](#using-the-prompt-library).
7. [MCP Context Servers](#mcp-context-servers).

### Configure the AI assistant
[Zed Docs -> Configure the AI assistant](https://zed.dev/docs/assistant/configuration).

By default, you are using the [Zed AI](https://zed.dev/blog/zed-ai) Free Plan which is limited to 1000 requests per month. They are adding a usage plan for "power users" -- is that people who code while on a stairmaster? -- the backend LLM is Anthropic Claude (Dec 2024).

```
  "assistant": {
    "default_model": {
      "provider": "zed.dev",
      "model": "claude-3-5-sonnet-latest"
    },
    "version": "2"
  },
```

You can add your own LLM back-end by just adding a different Assistane model and API key to your Zed settings.json configuration.

```
 "assistant": {
    "default_model": {
      "provider": "anthropic",
      "model": "claude-3-5-sonnet-latest"
    },
    "anthropic": {
      "api_key": "sk-ant-0000000000000"
    },
    "version": "2"
  },
```

Check what your current config is by running `assistant: show configuration`.

### Assistant chat panel
[Zed Docs -> Assistant (chat) panel](https://zed.dev/docs/assistant/assistant-panel).

### Inline assistant
[Zed Docs -> Inline assistant](https://zed.dev/docs/assistant/inline-assistant).

### Using previous contexts
[Zed Docs -> Using previous contexts](https://zed.dev/docs/assistant/contexts).

### Using slash commands
[Zed Docs -> Using slash commands](https://zed.dev/docs/assistant/commands).

### Using the prompt library
[Zed Docs -> Prompt library](https://zed.dev/docs/assistant/prompting).

### MCP Context Servers
[Zed Docs -> MCP Context Servers](https://zed.dev/docs/assistant/context-servers).

## Building a CLI Host App with Claude MCP
