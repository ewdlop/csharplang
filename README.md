# C# Language Design

[![Join the chat at https://gitter.im/dotnet/csharplang](https://badges.gitter.im/dotnet/csharplang.svg)](https://gitter.im/dotnet/csharplang?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge) [![Chat on Discord](https://discordapp.com/api/guilds/143867839282020352/widget.png)](https://aka.ms/dotnet-discord-csharp)

Welcome to the official repo for C# language design. This is where new C# language features are developed, adopted and specified.

C# is designed by the C# Language Design Team (LDT) in close coordination with the [Roslyn](https://github.com/dotnet/roslyn) project, which implements the language.

You can find:

- Active C# language feature proposals in the [proposals folder](proposals)
- Notes from C# language design meetings in the [meetings folder](meetings)
- Summary of the [language version history here](Language-Version-History.md).

If you discover bugs or deficiencies in the above, please leave an issue to raise them, or even better: a pull request to fix them.

For *new feature proposals*, however, please raise them for [discussion](https://github.com/dotnet/csharplang/labels/Discussion), and *only* submit a proposal as an issue or pull request if invited to do so by a member of the Language Design Team (a "champion").

The complete design process is described [here](Design-Process.md). A shorter overview is below.

## Discussions

Debate pertaining to language features takes place in the form of [Discussions](https://github.com/dotnet/csharplang/discussions) in this repo.

If you want to suggest a feature, discuss current design notes or proposals, etc., please [open a new Discussion topic](https://github.com/dotnet/csharplang/discussions/new).

Discussions that are short and stay on topic are much more likely to be read. If you leave comment number fifty, chances are that only a few people will read it. To make discussions easier to navigate and benefit from, please observe a few rules of thumb:

- Discussion should be relevant to C# language design. If they are not, they will be summarily closed.
- Choose a descriptive topic that clearly communicates the scope of discussion.
- Stick to the topic of the discussion. If a comment is tangential, or goes into detail on a subtopic, start a new discussion and link back.
- Is your comment useful for others to read, or can it be adequately expressed with an emoji reaction to an existing comment?

Language proposals which prevent specific syntax from occurring can be achieved with a [Roslyn analyzer](https://docs.microsoft.com/visualstudio/extensibility/getting-started-with-roslyn-analyzers). Proposals that only make existing syntax optionally illegal will be rejected by the language design committee to prevent increased language complexity.

## Proposals

When a member of the C# LDM finds that a proposal merits consideration by the broader team, they can [Champion](https://github.com/dotnet/csharplang/issues?q=is%3Aopen+is%3Aissue+label%3A%22Proposal+champion%22) it, which means that they will bring it to the C# Language Design Meeting. Proposals are always discussed in linked discussions, not in the champion issue. We didn't always follow this policy, so many champion issues will have discussion on them; we now lock issues to prevent new discussion from occurring on them. Each champion issue will have a discussion link on it.

## Design Process

[Proposals](proposals) evolve as a result of decisions in [Language Design Meetings](meetings), which are informed by [discussions](https://github.com/dotnet/csharplang/discussions), experiments, and offline design work.

In many cases it will be necessary to implement and share a prototype of a feature in order to land on the right design, and ultimately decide whether to adopt the feature. Prototypes help discover both implementation and usability issues of a feature. A prototype should be implemented in a fork of the [Roslyn repo](https://github.com/dotnet/roslyn) and meet the following bar:

- Parsing (if applicable) should be resilient to experimentation: typing should not cause crashes.
- Include minimal tests demonstrating the feature at work end-to-end.
- Include minimal IDE support (keyword coloring, formatting, completion).

Once approved, a feature should be fully implemented in [Roslyn](https://github.com/dotnet/roslyn), and fully specified in the [language specification](spec), whereupon the proposal is moved into the appropriate folder for a completed feature, e.g. [C# 7.1 proposals](proposals/csharp-7.1).

**DISCLAIMER**: An active proposal is under active consideration for inclusion into a future version of the C# programming language but is not in any way guaranteed to ultimately be included in the next or any version of the language. A proposal may be postponed or rejected at any time during any phase of the above process based on feedback from the design team, community, code reviewers, or testing.

### Milestones

We have a few different milestones for issues on the repo:
* [Working Set](https://github.com/dotnet/csharplang/milestone/19) is the set of championed proposals that are currently being actively worked on. Not everything in this milestone will make the next version of C#, but it will get design time during the upcoming release.
* [Backlog](https://github.com/dotnet/csharplang/milestone/10) is the set of championed proposals that have been triaged, but are not being actively worked on. While discussion and ideas from the community are welcomed on these proposals, the cost of the design work and implementation review on these features are too high for us to consider community implementation until we are ready for it.
* [Any Time](https://github.com/dotnet/csharplang/milestone/14) is the set of championed proposals that have been triaged, but are not being actively worked on and are open to community implementation. Issues in this can be in one of 2 states: needs approved specification, and needs implementation. Those that need a specification still need to be presented during LDM for approval of the spec, but we are willing to take the time to do so at our earliest convenience.
* [Likely Never](https://github.com/dotnet/csharplang/milestone/13) is the set of proposals that the LDM has rejected from the language. Without strong need or community feedback, these proposals will not be considered in the future.
* Numbered milestones are the set of features that have been implemented for that particular language version. For closed milestones, these are the set of things that shipped with that release. For open milestones, features can be potentially pulled later if we discover compatibility or other issues as we near release.

## Language Design Meetings

Language Design Meetings (LDMs) are held by the LDT and occasional invited guests, and are documented in Design Meeting Notes in the [meetings](meetings) folder, organized in folders by year. The lifetime of a design meeting note is described in [meetings/README.md](meetings/README.md). LDMs are where decisions about future C# versions are made, including which proposals to work on, how to evolve the proposals, and whether and when to adopt them.

## Language Specification

The current ECMA-334 specification can be found in markdown form on the [C# Language Standard](https://github.com/dotnet/csharpstandard/) repository.

## Implementation

The reference implementation of the C# language can be found in the [Roslyn repository](https://github.com/dotnet/roslyn). This repository also tracks the [implementation status for language features](https://github.com/dotnet/roslyn/blob/main/docs/Language%20Feature%20Status.md). Until recently, that was also where language design artifacts were tracked. Please allow a little time as we move over active proposals.

#2632

#3038

## Anonymous type aliasing

#8928
