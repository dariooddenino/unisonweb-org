---
title: Three-minute quickstart guide
description: This short guide will have you downloading and installing Unison and running your first program.
---

# Three-minute quickstart guide

This short guide will have you downloading and installing Unison and running your first program. There isn't much exposition here and the focus is on getting you up and running as quickly as possible. 🏎

More in-depth guides follow this one.

If you have any trouble with the process, or have ideas about how to improve this document, [come talk to us in the #alphatesting Slack channel][slack]! This document is also [on GitHub][on-github].

[slack]: /slack
[on-github]: https://github.com/unisonweb/docsite/edit/gh-pages/_includes/quickstart.markdown
[guide]: /docs/tour
[roadmap]: /docs/roadmap

## Step 1: Install Unison

If you haven't already, please join the [#alphatesting channel on Slack][slack]. Once you're logged in, [this Slack post](https://unisonlanguage.slack.com/files/TLL09QC85/FMT7TDDDY?origin_team=TLL09QC85) gives the (very brief and simple) install instructions.

When Unison is further along and ready for more general availability we'll just include those instructions here. For now, given the many rough edges that exist, we are really hoping that if you are trying out Unison you'll come talk to us, ask questions, and report bugs!

## Step 2: Create your Unison codebase

Run `ucm init` to initialize a Unison codebase in `$HOME/.unison`. This is where Unison will store function definitions, types, namespaces, and so on. 

## Step 3: Fetch the base libraries and run your first program

Launch `ucm` again, then from the `.>` prompt, do:

```ucm
pull https://github.com/unisonweb/base:.releases._M1j base
```

You'll see some output from `git` in the background, and once that's done you'll see a big list of definitions that the `pull` added. Press `q` to exit the list of definitions.

Open a new file, `scratch.u` in the same directory where you launched `ucm`, then add the following _watch expression_ (a line starting with `>`) to the top, then save the file. This expression multiplies every element in a list by `10`, using the `List.map` function:

```unison
---
title: scratch.u
---
> List.map (x -> x * 10) [1,2,3,4,5,6]
```

## What next?

* Come [say hello in Slack][slack], tell us what you thought about this guide, and ask questions. 👋
* A [more leisurely tour][guide] of the Unison language and the `ucm` command line tool. (25 minutes)