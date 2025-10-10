# Optimized Internals

## Overview

This project comprises a listener thread implementation based on primitive locks and multi-threading techniques. It
was created primarily to serve as source material for the development of an AI prompt. The prompt,
[Tom (Principal Developer)](https://github.com/SebGSX/Prompt-Engineering/blob/main/prompt-engineering/pull-request-review.md),
required a sufficiently complex codebase to exercise the AI's ability to review pull requests. See the
[Repo README](https://github.com/SebGSX/Prompt-Engineering/blob/main/README.md) for more information.

## Maintenance

To update the dotnet tools, run the following commands:

```shell
dotnet tool update --local dotnet-stryker
dotnet tool update --local dotnet-coverage
dotnet tool update --local microsoft.coyote.cli
```

All other dependencies are managed by the project's `dotnet` configuration and the NuGet package manager.
