# Course assistant kit

Everything from the NHH seminar "Building an AI assistant for your course"
(25 September 2026) that you need to build a course assistant of your own in
Sikt KI-assistent: an AI chatbot set up for one course, which students chat
with about concepts, exercises, deadlines and course rules.

## Start here

1. Open [Kursassistent-byggeren](https://ki.sikt.no/B53K) in Sikt and give it
   the link to your course page. It interviews you and writes a first draft of
   the instructions, then walks you through the other settings.
2. Compare the draft with [`examples/instructions.md`](examples/instructions.md),
   the instructions of BED3-Buddy as rewritten for Sikt in September 2026.
   The course responsible has tested them in Sikt; students have not used this version
   yet.
3. Gather your files with [`examples/knowledge-files.md`](examples/knowledge-files.md).
4. Test it the way a student would, then post
   [`examples/note-to-students.md`](examples/note-to-students.md) next to the link.

## What is here

| Folder | What it holds |
|:--|:--|
| `slides/` | The slides. Download the folder and open `index.html` in a browser |
| `examples/` | The instructions of BED3-Buddy, a course assistant for a bachelor finance course, with notes on what the tutor stance and the refusal rules do; an inventory of which course files to upload; and a note to students |
| `builder/` | The instructions and knowledge file of Kursassistent-byggeren itself, and an example of a draft it wrote for BED3 |

The instructions are written for Sikt KI-assistent, but the text works in any
tool that has an instructions field and knowledge files.

Questions: André Wattø Sjuve.
