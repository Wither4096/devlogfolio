---
date: 2026-11-18T02:57:31+03:00
title: "yshell"
description: "shell built on a whim, because why not"
tags: ["project"]
summary: "simple UNIX system shell"
---

## Project Info

- **Status:** Complete
- **Tech:** C with POSIX APIs
- **Repo:** [GitHub](https://github.com/wither4096/whyshell)

## Overview
A simple UNIX shell made in C made over the course of a single afternoon. Designed to be simple, readable, and easy to understand for anyone with basic C knowledge

## Goals

- Learn UNIX/POSIX systems programming in C
- Learn basic tokenization and parsing techniques
- Learn `fork()`,`execvp()` process workflow
- Minimal as to be built in as little time as possible

## Design

- Single source file
- Manually memory managed
- Tokenizing command input using strtok()
- Creating child processes with fork()
- Executing external programs using execvp()

## Implementation

- Written in POSIX C
- Tokenizing arguments using `strtok()`
- Child process creation and handling with POSIX methods

## Features

- Built in commands (exit, cd)
- Running external programs with POSIX `execvp()`

## Limitations

- No scripting.
- No environment variable expansion.
- No quoting or escaping.

## What I Learned

- Dealing with arguments in programming
- Creating child processes, handling them, and managing errors
- Basic tokenization and parsing
