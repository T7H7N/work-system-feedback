# First sweep: accepted items missing from an export

Window closes Sunday, January 5, 2031. Two readers split the three paths below. The first read Elm and Reed; the second read Moss. Their returns accounted for every assigned path exactly once.

| Record | Evidence | Classification |
|---|---|---|
| [Elm](notes/elm.md) | A successful run omitted ash. Adding a final line break restored it. | Direct |
| [Moss](notes/moss.md) | A separate run omitted sage. The same single input change restored it. | Direct |
| [Reed](notes/reed.md) | Forwarded Elm's account and performed no run. | Relay only |

**3 records, 2 direct sessions, 1 relay.** The two direct accounts used different batches and show the same end-of-file condition. Group them under one signal. A hypothetical missing item rejected before export would need different evidence and is excluded.

Decision: ask the export maintainer to handle the final accepted item when input ends. Check both saved batches with and without a final line break. Keep the signal open until the repaired output has also been used.
