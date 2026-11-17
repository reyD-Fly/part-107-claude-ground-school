# Part 107 Claude Ground School

A free, open-source study tool that transforms your Claude Project into a full Part 107 Ground School. It runs a 90-minute study session six days a week, logs your study for you, and retests the questions you missed before. At the end of the course, it gives you full 60-question mock tests.

Created by **Luis Cadiz**.

---

## What is in this repository

| File or folder | What it is |
| --- | --- |
| `system-prompt.md` | Master Ground Instructor instructions to paste in your Claude Project. |
| `tracker-template.md` | A blank Part 107 Study Tracker for all 17 lessons, 2 mock tests, a study session log, and a missed questions log. |
| [Knowledge Base release](https://github.com/reyD-Fly/part-107-claude-ground-school/releases/tag/knowledge-base-v1) | The public-domain FAA PDFs the instructor uses to teach the sessions. You upload these to your Claude Project. They are attached to a release because they are too large to be stored in the repository itself. |
| `knowledge-base/` | Notes on the reference FAA documents and where to get them. |
| `LICENSE` | Creative Commons Attribution-NonCommercial 4.0 (CC BY-NC 4.0). |

## How the study system works

- **Schedule:** Each session runs 90 minutes, Monday through Saturday. There are no classes on Sundays.
- **Each session has three phases:**
    1. **Recall and remediation (0–10 min):** First, all missed questions from prior sessions are shown to the student again. If a student misses the same concept more than once, the instructor gives a step-by-step, whiteboard-style visual outline of the key points of that concept.
    2. **Concepts (10–50 min):** Written study information with original graphics. For each concept, students also get one YouTube video found by search, with the title and channel checked.
    3. **Quiz (50–90 min):** 20 questions: 14 on the current lesson and 6 review questions from earlier lessons. Students must score 90% (18/20) or higher to pass the lesson. If they do not pass, they repeat the lesson in the next session.
- **Real-world scenarios:** Airspace, chart, and weather questions are all set in the context of your own drone and your own local airport, and they use current METAR/TAF reports.
- **Finish line:** After all 17 lessons, you take full 60-question mock tests. When you score 85% or higher on two consecutive mock tests, you are ready to book the real test.

---

## Required prerequisites

### 1. A Claude account with Projects

You need a Claude account with Projects. Turn on web search in your chat settings. The instructor uses it for live weather reports, current charts, and video links.

### 2. Two study guides (purchase them yourself)

The instructor uses two commercial study guides only as a guide to arrange the lessons in the correct order and to set the correct pace. The books are copyrighted and are not included in this repository. If you want to use the study guides, you must purchase them yourself and take your own notes.

| Name in the prompt | Book | Author | Amazon |
| --- | --- | --- | --- |
| Kindle Study Guide 1 | *Drone FAA 107 License Study Guide: Everything You Need to Know to Pass Your 107 Test the First Time* (2018) | Damon Darnall | [Paperback (ISBN-10 1727096533)](https://www.amazon.com/dp/1727096533) · [Kindle (ASIN B07GC5HH8L)](https://www.amazon.com/dp/B07GC5HH8L) |
| Kindle Study Guide 2 | *Remote Pilot FAA Part 107 Study Guide in Full-Color: The Complete UAG Test Prep with Full Practice Exams & Bonus Questions* (2025) | Bolton Prep | [Kindle (ASIN B0FWZZVC2N)](https://www.amazon.com/dp/B0FWZZVC2N) |

The tracker lists the matching chapter and section numbers for each lesson. The system still works without the books, because all teaching content comes from the FAA documents.

### 3. A printed copy of the testing supplement figures (recommended)

Chart lessons ask you to work on paper. Print these pages from the FAA Airman Knowledge Testing Supplement (FAA-CT-8080-2H): **Figures 20–26, Figures 69–71, and Legend 1.**

---

## Deployment guide

Follow these four steps in order.

### Step 1. Create a Project

1. Open [Claude](https://claude.ai/).
2. Go to **Projects** and create a new Project.
3. Name it **Part 107 Ground School**.

### Step 2. Set the custom instructions

1. Open `system-prompt.md` in this repository.
2. Copy the WHOLE document and DO NOT ALTER it in any way. You do not need to fill in the bracketed placeholders, like `[Your Name]`. Claude fills them in for you during setup (Step 4).
3. In your Project, open the instructions box. The box has the title "Set project instructions" at the top. Paste the text and then click "Save instructions".

### Step 3. Upload the knowledge files

1. Open the [Knowledge Base release](https://github.com/reyD-Fly/part-107-claude-ground-school/releases/tag/knowledge-base-v1).
2. Under **Assets**, download every PDF.
3. In your Project, upload all of the PDFs to the Project knowledge (the Project's files area).

**The Airman Knowledge Testing Supplement for Sport Pilot, Recreational Pilot, Remote Pilot, and Private Pilot (FAA-CT-8080-2H) comes in 12 separate PDFs instead of one large PDF. The full document is too large to upload to a Claude Project as one file. Upload all 12 parts so the instructor can see all the figures.**

### Step 4. Initialize the tracker

1. Open `tracker-template.md` and copy all of its text. Do not fill anything in.
2. Start a new chat inside your Project. Paste the tracker text, then type:
    
    ```
    Here is my blank study tracker. Acknowledge these rules, and I will say 'start' when I am ready for Lesson 1.
    ```
    
3. Next, Claude will ask for some basic setup information: your name, your drone, your airport or local airspace, and the time of day you want your daily study sessions to start. Claude will use this information to complete your tracker and to set up all of the flight scenarios. Save the updated tracker it gives you. Claude may also ask to set up a scheduled task: a nightly reminder to create your FAA Tracking Number (FTN) and book your test. You can click 'Schedule' to set up the reminder or 'Cancel' if you do not need it.
4. When you are ready to study, type **start**.

---

## Tips for using it day to day

- **Keep the tracker current.** At the end of each session, ask Claude to provide a current copy of the tracker and save it to your records. When a chat gets long, start a new chat and paste the current tracker at the start.
- **Verify, do not assume.** Claude checks altitudes, frequencies, and weather against official sources, but you are the pilot. Always confirm airspace with the official [FAA UAS Facility Maps](https://www.faa.gov/uas/commercial_operators/uas_facility_maps) and current sectional charts before you fly.
- **Set a deadline.** Create an FAA Tracking Number (FTN) in [IACRA](https://iacra.faa.gov) and schedule your knowledge test with PSI. Set a fixed test date to keep yourself on track.

## Sources for the knowledge base

All PDFs in the Knowledge Base release are U.S. government works in the public domain. You can also download them directly from the FAA:

- [Remote Pilot – Small Unmanned Aircraft Systems Study Guide (FAA-G-8082-22)](https://www.faa.gov/sites/faa.gov/files/uas/resources/policy_library/remote_pilot_study_guide.pdf)
- [Airman Knowledge Testing Supplement for Sport Pilot, Recreational Pilot, Remote Pilot, and Private Pilot (FAA-CT-8080-2H)](https://www.faa.gov/sites/faa.gov/files/training_testing/testing/supplements/sport_rec_private_akts.pdf) · [FAA testing supplements page](https://www.faa.gov/training_testing/testing/supplements)

## Contact

- **Questions or problems with the study system:** Open an [Issue](https://github.com/reyD-Fly/part-107-claude-ground-school/issues) here on GitHub. Other students can see the answer too.
- **Email:** dewdrop.26stories@icloud.com
- **Instructors and professionals:** Connect with me on [LinkedIn](https://www.linkedin.com/in/luiscadiz).

## Disclaimer

This project is not affiliated with or endorsed by the FAA, PSI, Anthropic, or the authors of the study guides listed above. The instructor is an AI tutor. It is not perfect and can make mistakes. Be sure to check important facts against the official FAA sources.

This project is a study aid for the knowledge test. It is not flight instruction, and it does not replace official FAA sources. You are responsible for following 14 CFR Part 107 and getting any required authorization before you fly. Never use a lesson scenario as a real flight plan without checking official sources first.

## License

The instructions, tracker, and documentation in this repository are released under the [Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/) license. You are free to share and adapt the material for noncommercial purposes, provided you give proper credit to Luis Cadiz and link back to this repository. You may not sell the material or use it in a paid product or course. The FAA documents in the Knowledge Base release are in the public domain.
