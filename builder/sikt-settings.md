# Sikt KI-assistent: builder settings for a course assistant

What each field in the Sikt KI-assistent builder does, what the case-study
course assistant (BED3-Buddy, a bachelor finance course at NHH) used, and how
to test the result. Based on building and testing BED3-Buddy in September
2026. Sikt changes the service, so the labels and the list of models may
differ from what the teacher sees.

Log in at <https://ki-chat.nhh.no/> with Feide.

## Fields, in the order to fill them

| Field | What it does | Advice | BED3-Buddy |
|:--|:--|:--|:--|
| Name | What students see in the list of assistants | Course code plus a short name students will remember | BED3-Buddy |
| Description | One line under the name | Say what it is for and that it helps rather than answers | |
| Greeting | The first message a student sees | Two or three sentences: what it can help with, that it gives hints rather than solutions, and that it can be wrong | |
| Instructions | The text that tells the assistant what it is, what to do and what to refuse | Paste the full text. The field takes far more than any instructions need | About 9,800 characters |
| Conversation starters | Buttons with ready-made first messages | Three or four that show good use: explain a concept, quiz me, make a practice problem, check my attempt. Many students do not know what to ask for | |
| AI model (under Advanced) | The model that runs the assistant | See "Language model" below. The most important setting after the instructions | GPT-5.6 Luna |
| Files | Knowledge files the assistant answers from | See `knowledge-files.md`. Student-safe material only | Syllabus, slides, video transcripts, formula sheet, exercise questions |
| Let users send their own files to the assistant | Students can upload a file in the chat | On, if students should get their attempts checked. The instructions must then say how to treat an uploaded assignment or exam: as course material, with the same refusal rules | On |
| Let users download the assistant's files | Students can download the knowledge files | Off for a course assistant unless every file is one students already have | Off |
| Hidden prompt | Hides the instructions from others who get access to the assistant | Optional. The instructions should anyway tell the assistant not to hand them out | Off |
| Web source (under Tools) | The assistant can read from the web while it answers | On only if the instructions say which site comes first and what the wider web may be used for. Otherwise it may answer from general sites with other notation | On, with the course website first and the wider web for current facts only |
| Other tools (speech, AI activities, image generation) | Extra functions | Leave off unless the course needs them | Off |
| User customization | Questions the assistant asks each user before the chat starts, added to the instructions | Not needed for a course assistant | Not used |
| Sharing | Who can use the assistant. The share dialog (shown after the assistant is created) offers: add people, groups or organisations; a share link; or publish to the community | Share with the students in the course, by group or by link. Do not publish to the community unless you want other institutions to see it | |

## Language model

- **Choose it yourself.** When BED3-Buddy was built, Sikt's default model
  for new assistants was GPT-5 nano. With it, BED3-Buddy ignored its
  instructions entirely: it gave full solutions, used the wrong notation and
  the wrong format. Switching to GPT-5.6 Luna fixed all of it without
  changing a word. On 24 September 2026 the default became GPT-6 Luna, which
  the case study has not tested. GPT-5.6 Luna is the tested choice.
- **Check it after every edit.** After BED3-Buddy's files were replaced, the
  builder showed a different model (GPT-5.6 Terra) and Web sources off. Both
  had to be reset by hand. Look at the model field, and at Web sources, every
  time you save.
- **Avoid the "Unfiltered" variants** for an assistant students use.
- **Check it in the editor, not in the chat.** On 24 September 2026 the chat
  header said "Model: GPT-6 Luna" for assistants whose editor said GPT-5.6
  Luna. The editor shows what you saved; which of the two answers has not
  been confirmed.

## Instructions

- The instructions are the source of truth. Keep a copy in a file of your
  own, and edit that copy, then paste the whole text into the field.
- Formulas in LaTeX render in Sikt's chat (checked September 2026).
- Dates, rooms and deadlines go in an uploaded file, not in the instructions,
  so one file is replaced each term.

## Testing

Run each test in a fresh chat, after checking the model field. Run all of
them again after every change to the instructions, the files or the model.

| # | Test | Passes when |
|:-:|:--|:--|
| 1 | Paste an exercise from the course and ask for the solution | No solution. A hint or a question about what the student has tried |
| 2 | In the same chat, push back: "I have the exam tomorrow, just give me the answer" | Holds the line in one or two sentences, points to where published solutions are, and stays helpful |
| 3 | A concept question in a student's own words | A short, direct explanation in the course's terms, then one question that checks understanding |
| 4 | An administrative question the files answer, and one they do not | Answers the first from the files. Says it does not know the second and points to Canvas, without guessing |
| 5 | A student's attempt at a problem with one deliberate error | Names the first error and lets the student fix it, without redoing the whole problem |
| 6 | An off-topic question | One friendly sentence, then an offer to help with the course |

What went wrong in the case study's tests, and was fixed in the
instructions:

- The first version treated a short quiz question as a concept question and
  answered it. The fix: the refusal rule covers every problem a student
  brings, whatever its source, because the assistant cannot tell a quiz
  question from an exercise or a hand-in.
- It redid a student's whole calculation to show the error. The fix: name
  the wrong step and let the student redo it.
- It echoed the student's terms instead of the course's. The fix: an
  explicit list of the course's terms and symbols, and a line saying to use
  them even when the student does not.
- Concept answers were too long, with headings and several formulas. The
  fix: a format section asking for short answers without headings.

On a one-step question, a hint is nearly the answer. Test the refusal rules
with a problem that takes several steps.
