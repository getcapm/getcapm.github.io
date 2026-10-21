<style>
.md-content .md-typeset h1 { display: none; }
</style>

<div align="center">
    <img src="assets/logo-dark.png"/>
</div>

<p align="center">
    <em>Code Analysis Package Manager</em>
</p>

## Introduction

CAPM is a package manager for all tools related code analysis. It provides a
single command to [find](/packages/),
[run](/getting-started/#running-a-package), and
[configure](getting-started/#package-configuration) your code analysis tools. 

For example, running the [tokei](https://github.com/XAMPPRocky/tokei) code
counter is as simple as: `capm run tokei`:

![Tokei example](example.gif)

## Why

Code analysis should be easy and one of the first things to set up for a
software project, not an afterthought.

Static analysis tools give insight into code metrics such as volume,
complexity, and duplication. CAPM makes running these tools from the
[CLI](/getting-started/#running-a-package), and [GitHub
Actions](/getting-started/#running-in-github-actions), straightforward.

## How

CAPM wraps static analysis tools in a small Docker image, called packages. It
also provides a CLI command and GitHub Action to run these packages. 
