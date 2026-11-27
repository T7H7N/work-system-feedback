# work-system-feedback · Session notes and sweeps

English | [한국어](README.ko.md)

Use this method to improve the rules, tools, and procedures that several people or sessions use to do their work. A worker describes friction in their own words in a **session note**. At regular intervals, a **sweep** reads every note in the window, counts independent observations, and gives the owner evidence for a repair. The next sweep checks whether the change was used and whether the failure recurred. The same task can also produce a **fragment** for a person who needs the result in a weekly report.

```text
Work performed
  |-- Result someone can use -> fragment -> weekly report -> reader's decision
  |
  +-- Friction someone saw -> session note -> sweep all eligible notes
                                                |
                                  count independent observations
                                                |
                                  owner changes a shared rule,
                                  tool, or procedure if warranted
                                                |
                                   check use and recurrence
                                       in the next sweep
```

## Choose what to write

| At the end of a task | Write |
|---|---|
| A result someone needs for a decision or weekly report | A fragment. Include the evidence and any limit on the result. |
| A misleading signal, failed attempt, or surprising constraint that another worker might encounter | A session note in your own words. Describe the input, action, and visible result in the order they happened. |
| A usable result and a trap worth investigating | Both. The fragment can say the export was delivered; the note can explain how the export first appeared complete with a row missing. |
| Routine activity with neither kind of information | Skip both. An urgent fault goes directly to the person who can act on it. |

Write a session note before reading another worker's account or a predecessor's note. Use your own evidence. If you learned of an event secondhand, name its source and say which parts you could check yourself. This makes it possible to tell how many workers actually saw a problem. There is deliberately no sentence template for session notes.

## Try both paths with one export

The example uses fictional workers, files, and dates. All inputs can be inspected as plain text.

1. **Write for the weekly reader.** On Friday, Elm restored a missing row and checked the exported IDs. The [fragment](examples/fragment.md) says which batch the reader can use and which repair is still open. Assemble fragments by the date the work happened, even if written up the following Monday. Keep each author's fragment separate; append new evidence to that author's own note. A person checks the evidence and edits the [weekly note](examples/weekly.md).
2. **Read the whole sweep window.** Freeze a list of eligible note files and their content fingerprints. Divide the list among readers. Each reader reports which files were read, cites the observation, and names unreadable files. A changed fingerprint reopens that file for inspection without creating a new occurrence. Keep fragments, weekly notes, and sweep reports out of the incident count.
3. **Count witnesses.** Elm and Moss each ran a different input and compared the bytes at the end of the input with the missing output row. Reed passed along Elm's observation without running an export. The [first sweep](examples/sweep-first.md) therefore has **3 records, 2 direct sessions, 1 relay**. Two mentions by Elm still count as one direct session for that signal. Merge differently named reports only if their evidence supports the same failure. Keep an uncertain match separate.
4. **Make a decision and check what happened.** The sweep owner records the evidence, decision, owner, and the condition for checking again. Here, two independent observations justify fixing the missing final row. The [next sweep](examples/sweep-next.md) checks the repair against both original input conditions and asks, **"Was the result actually used?"** A successful check is follow-up evidence; it adds no failure occurrence. The [ledger](examples/ledger.md) retains the original counts and the reason for closure.

You can adopt either path on its own. Start with [capture](docs/capture.md), [weekly assembly](docs/assemble.md), or [running a sweep](docs/sweep.md). The [fragment form](templates/fragment.md), [reader return](templates/sweep-return.md), and [signal ledger](templates/signal-ledger.md) are the only forms.

## Prior work

| Project | Practice relevant here |
|---|---|
| [hex/claude-sessions](https://raw.githubusercontent.com/hex/claude-sessions/1bffb839754748f7201ff08678d6ad0549c2115c/docs/session-layout.md) | Each contributor keeps an append-only narrative notebook. Its resume workflow rereads the notebook; here the writer first records their own observation. |
| [cathrynlavery/worklog](https://raw.githubusercontent.com/cathrynlavery/worklog/22c5e0c352772916a0e21498dd7d802d746ade9d/README.md) | Session checkpoints with evidence supply daily and weekly reports. Here a worker can record friction even when it adds nothing to the weekly report. |
| [twisted/towncrier](https://raw.githubusercontent.com/twisted/towncrier/bbb4eef8394940eddeba4f934a907e4ea4cbf2ce/README.rst) | Small fragments carry changes that matter to the eventual reader and are assembled later. Its output is a release note. |
| [tang-t21/weekly-report](https://raw.githubusercontent.com/tang-t21/weekly-report/ea0b0810485949311e4394f20f9a49ec7478e3af/README.md) | Session history and pull requests can supply a weekly report retrospectively. Here contributors select fragments while the evidence is at hand. |
| [weak-fox/agent-retrospective](https://raw.githubusercontent.com/weak-fox/agent-retrospective/54365e745470a81333efef5221e058bcd5a60ca4/README.md) | We adopt its practice of fingerprinting inputs to find previously seen files that changed after the last pass. |
| [pskoett/self-improving-agent](https://raw.githubusercontent.com/pskoett/self-improving-agent/e958afb5bf697c7d22898f9bba53406e2e3261bd/self-improving-agent/SKILL.md) | Both methods use recurrence when deciding whether to change guidance. This project tracks distinct tasks when promoting lessons to agent guidance. Our ledger counts firsthand sessions and names the owner of the shared tool, rule, or procedure that needs attention. |
| [netresearch/retro-skill](https://raw.githubusercontent.com/netresearch/retro-skill/751ff48dd788d17c9e081f7bcd540c6992ae87bf/README.md) | Both methods can direct a finding to the owner of a shared project rule or tool. We adopt its question about later use. Our starting evidence is the set of firsthand and relayed notes in a fixed window, including material a worker would leave out of a weekly report. |

## Related projects

[session-lineage](https://github.com/T7H7N/session-lineage) describes how a successor picks up unfinished work.

[blind-review-policy](https://github.com/T7H7N/blind-review-policy) describes how to review a fixed candidate and decide what to do with the findings.
