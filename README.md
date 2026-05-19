\# ReviseFlow — Spaced Revision Scheduler for Students



ReviseFlow is a completely local, browser‑based study planner that combines \*\*spaced repetition\*\* with your \*\*real‑world class schedule\*\*.  

It ensures you never miss a revision, automatically respects your weekly timetable, and helps you prepare for exams—all with a modern dark UI.



\---



\## ✨ Features



\### 📅 Calendar‑Aware Scheduling

\- Import your weekly class schedule from a simple Google Calendar `.ics` export.

\- The app maps each subject to the actual days it occurs in your timetable.

\- Lessons are automatically scheduled only on days the subject appears—no more useless “study Maths on Sunday” reminders.



\### 🔁 Smart Spaced Repetition (SM‑2)

\- Dynamic interval calculation based on your recall quality.

\- Supports four feedback levels: \*\*Easy\*\*, \*\*Medium\*\*, \*\*Hard\*\*, \*\*Forgotten\*\*.

\- Ease factor adapts over time.

\- Intervals grow from 1 day to over a year as you master material.



\### 🧱 Block‑Based Repetition (NEW)

\- For structured curricula, use \*\*calendar block repetition\*\*.

\- Instead of fixed‑day intervals, a lesson can repeat \*\*every X blocks\*\* of the subject (e.g., every 3rd Maths lesson).

\- Ideal for courses where content is divided into numbered sessions.



\### 📚 Subjects \& Sections

\- Create subjects with custom icons and colors.

\- Organise lessons into \*\*sections\*\* (e.g., “Algebra”, “Grammar”).

\- Each lesson tracks its difficulty, mastery, status, and revision history.



\### 📊 Memory Health Analytics

\- Visualise your overall retention, subject breakdowns, and weakest lessons.

\- 30‑day activity heatmap and revision trend chart.

\- Identify what you’re about to forget before it’s too late.



\### 🎯 Exam Preparation Mode

\- Add upcoming exams with a date.

\- Mark critical lessons that need extra attention.

\- See a countdown and a weakness list for each exam.



\### 🔍 Powerful Search

\- Search across all lessons by name, subject, status, or tags.

\- Filter by overdue, critical, or specific subjects.



\### 🔥 Streak Tracking

\- Tracks your daily study streak automatically.

\- Longest streak recorded.



\### 💾 Data Ownership

\- All data stored in your browser’s `localStorage`.

\- Export / import your full database as a JSON file.

\- No servers, no accounts, full privacy.



\### 🌙 Modern Dark UI

\- Built with Tailwind CSS and React.

\- Fully responsive sidebar, modals, and calendar.

\- Smooth animations and a distraction‑free experience.



\---



\## 🧠 How It Works



\### Spaced Repetition (SM‑2)

When you review a lesson, you rate your recall:

\- \*\*Easy\*\* → interval jumps to the next tier, ease factor increases.

\- \*\*Medium\*\* → moves to the next interval tier but stays near the current length.

\- \*\*Hard\*\* → interval shrinks slightly, ease factor drops.

\- \*\*Forgotten\*\* → resets to 1 day, ease factor decreases significantly.



The app also \*\*snaps the next revision date to a valid calendar day\*\* for that subject, so you only review when the subject actually appears.



\### Calendar Blocks

After importing your weekly schedule, the app builds a sorted list of all future dates when each subject is taught (e.g., every Monday, Wednesday, Friday).  

\- If a spaced‑repetition calculation lands on a day the subject isn’t taught, it automatically moves forward to the next available day.

\- \*\*Block repetition\*\* uses this list to schedule reviews every N blocks (e.g., 3rd occurrence after today).



\### Block Repetition Detail

\- A lesson with `blockReview = true` and `blockInterval = 3` will appear on the 3rd, 6th, 9th, etc. occurrence of the subject, starting from the next block after the lesson’s start date.

\- All future block occurrences (up to one year) are shown on the calendar view.

\- Useful when you want to review a topic only every 3rd lesson, regardless of calendar days.



\---



\## 🚀 Getting Started



\### Prerequisites

\- A modern web browser (Chrome, Firefox, Edge, Safari).

\- No installation required—just open the `index.html` file.
- Pc APP version / and an ANDROID version too ! 



\### Running the App

1\. Download the folder / it has the android app - pc app - web app at one place !

2\. Double‑click to open it in your browser if you choose the html version. same as app version . and install the ANDROID version

3\. (Optional) For a better experience, serve it with a local server (e.g., `npx serve .`) if you choose html.



\### First Steps

1\. \*\*Create a Subject\*\* – Click the “+” in the sidebar, choose a name, icon, and color.

2\. \*\*Add a Lesson\*\* – Inside the subject, click “+ Add Lesson”. Fill in title, section, difficulty, etc.

3\. \*\*Set Up Your Weekly Schedule\*\* – Go to \*\*Settings\*\* → \*\*Weekly Schedule (Manual)\*\*, upload a `.txt` file (see format below).

4\. \*\*Start Studying\*\* – On the dashboard, click “Study Now” on today’s lessons. After studying, rate your recall.



\---



\## 📘 Detailed Usage



\### Subjects

\- Each subject has an icon, a colour, and a list of sections.

\- You can edit or delete subjects from the sidebar or the subject page.



\### Lessons

\- \*\*Status\*\* automatically moves between `new`, `learning`, `stable`, and `mastered` based on review history.

\- \*\*Manual Override\*\*: When adding/editing a lesson, you can set a specific “Next Revision Date” to bypass automatic scheduling.

\- \*\*Sections\*\* help organise material; you can filter the lesson list by section.



\### Rating Your Recall

When a lesson is due, click “Review Now” to open the rating panel:

\- \*\*Easy\*\* 😊 → You remembered everything effortlessly.

\- \*\*Medium\*\* 🤔 → You recalled most, but with some effort.

\- \*\*Hard\*\* 😰 → You struggled significantly.

\- \*\*Forgotten\*\* 😞 → You couldn’t remember; reset the learning.



\### Calendar Integration



\#### Option 1: Manual Weekly Schedule (Recommended)

Create a `.txt` file like this:

MONDAY



Science



Geography



Philosophy

...

TUESDAY



Maths



Science

...



text



Each day name must be spelled exactly in uppercase (MONDAY, TUESDAY, …).  

Subjects are listed with a dash (`-`) or simply the name.  

\*\*Upload\*\* this file in Settings → Weekly Schedule.



\*\*Important\*\*: In the same section, set a \*\*keyword\*\* for each subject that exactly matches the name in the file (case‑insensitive). Then \*\*re‑upload\*\* the `.txt` file to generate the calendar blocks.



\#### Option 2: Google Calendar `.ics` Import

\- Export your Google Calendar as an `.ics` file.

\- Import it in Settings → Alternative: Import .ics File.

\- The app matches events whose \*\*summary\*\* exactly equals your subject’s keyword.



> \*\*Note\*\*: Time‑zone corrections are applied so that imported dates always reflect your local day.



\### Block‑Based Repetition

When adding/editing a lesson:

\- Check \*\*“Use calendar block repetition”\*\*.

\- Enter \*\*“Show every X blocks”\*\* (e.g., 4).

\- The lesson will then be scheduled only every 4th time the subject occurs.



\### Exam Mode

\- In \*\*Exam Mode\*\*, add an exam with a name and date.

\- Mark lessons as “critical” by clicking the star next to them.

\- The dashboard shows a countdown and a list of your weakest lessons for each active exam.



\### Settings

\- Configure default spaced‑repetition intervals and ease factor.

\- Import/export your entire database as JSON.

\- Reset all data in the Danger Zone.



\---



\## 💾 Backup \& Restore

Your data lives in your browser’s `localStorage`.  

To avoid losing it:

\- Regularly \*\*export a JSON backup\*\* (Settings → Backup \& Restore).

\- You can later re‑import that file to restore everything.



\---



\## 🛠️ Technical Stack

\- \*\*React 18\*\* (via CDN, with Babel for JSX)

\- \*\*Tailwind CSS\*\* (CDN)

\- \*\*Recharts\*\* (lazy‑loaded for analytics)

\- Vanilla JavaScript for the SM‑2 algorithm and ICS parsing

\- No build step, no server needed—just a single HTML file.



\---



\## 📝 License

This project is provided for personal educational use. Feel free to modify and share.



\---



\*\*Happy revising! 🎓\*\*  

\*ReviseFlow – because your memory deserves a real schedule.\*

