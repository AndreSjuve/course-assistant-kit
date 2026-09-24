# Knowledge file inventory

A knowledge file is a document the teacher uploads so the course assistant
can answer from it. The assistant is not trained on these files; it looks up
the relevant passage each time a student asks. This inventory lists the kinds
of files worth uploading, one rule for each, and marks the kinds the
case-study assistant (BED3 at NHH) used. No actual course files are included.

**The one rule that covers everything:** never upload what you would not put
on the course page.

## Inventory

| Kind of file | Rule | Case study |
|:--|:--|:-:|
| Syllabus, schedule, course description, course rules | Upload the current version and replace it whenever it changes. This is what makes "when is the deadline?" answerable. | ✓ |
| Lecture slides and lecture notes | Student editions only. Never the instructor edition with notes, solutions or grading remarks. | ✓ |
| Video transcripts | Merge into one file per lecture so the file count stays low. Strip timestamps. | ✓ |
| Formula sheet | Upload the same PDF the students get, so the assistant uses the course's notation. | ✓ |
| **Exercise sets, without solutions** | **Upload the questions. Never upload a solution key, a model answer or a rubric.** Store solutions somewhere the assistant cannot see. | ✓ |
| Practice exams and past exams | Questions only, and only if the course publishes them. Same rule as exercise sets. | |
| Case material | Student editions only. Instructor notes and solution proposals stay out. | |
| Textbook chapters, licensed articles, database exports | Do not upload. Copyright and licence terms apply. Refer students to the library and the reading list instead. | |
| Co-lecturers' or third parties' material | Only with the author's explicit agreement for this use. Course ownership does not cover it. | ✓ (with agreement) |
| Anything containing student data | Never: no names, grades, submissions, emails or feedback on individual work. | |
| Anything from the assessment side | Never: exam drafts, solution proposals, grading maps. If a student could not read it on the course page, it does not go in. | |

## Where the files go

For Sikt KI-assistent, from Sikt's privacy statement (June 2026): the models
run on Microsoft Azure in Sweden, all processing takes place within the EEA,
inputs and outputs are not used to train language models (and this cannot be
switched on in the service's current design), and when a staff member uses
the service on behalf of NHH, NHH is normally the data controller. Sources with links
are in `docs/research-platforms.md`, section 1.

## Practical advice

- **Keep a list.** A short file recording what was uploaded, from where, and
  who checked it as student-safe. Without it you will not remember what the
  assistant knows, and you cannot rebuild it when the platform changes.
- **Fewer, larger files.** Merge per lecture or per topic rather than
  uploading fifty small files.
- **Use what students already get.** The built PDF of the slides, the formula
  sheet as distributed, the schedule page as published. No special editions.
- **Replace, do not add.** When the schedule changes, delete the old file and
  upload the new one, or the assistant will quote both.
- **Test the retrieval.** After uploading, ask three administrative questions
  whose answers are in the files and one whose answer is not. The assistant
  should answer the three and say it does not know the fourth.
