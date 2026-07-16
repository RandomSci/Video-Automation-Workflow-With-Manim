
# Video Automation Workflow with Manim

A free, working n8n + Manim pipeline that turns a narration script into a fully rendered, animated video — no editing software, no manual animation.

---

## 📘 Start here: [instructions.html](https://htmlpreview.github.io/?https://github.com/RandomSci/Video-Automation-Workflow-With-Manim/blob/main/instructions.html)

**If you're new to n8n or Manim, open `instructions.html` first.** It's a complete, standalone setup guide — what this actually does, what Manim and n8n are, how the pipeline fits together, and step-by-step setup. Everything below is a quick reference for people who already know their way around.

---

## What's in this repo

| File                                          | What it is                                                                 |
| --------------------------------------------- | -------------------------------------------------------------------------- |
| `Video_Automation_Workflow_with_Manim.json` | The n8n workflow — import this directly into your n8n editor              |
| `main.py`                                   | The Python rendering engine (FastAPI server n8n calls into)                |
| `functions_manim.py`                        | The reusable Manim animation library (charts, counters, comparisons, etc.) |
| `requirements.txt`                          | Python dependencies                                                        |
| `Audio_Voice/`                              | Drop your narration`.mp3` here                                           |
| `.env.example`                              | Copy to`.env` and fill in your own API keys                              |

## Quick start

```bash
pip install -r requirements.txt
cp .env.example .env      # then fill in your API keys
uvicorn main:app --host 0.0.0.0 --port 8000
```

Then import `Video_Automation_Workflow_with_Manim.json` into n8n and reconnect your own credentials — everything was stripped out before this went public.

## How it works, in one line

Audio → Whisper transcription → GPT story beats → GPT-generated Manim code per chunk → rendered + duration-locked → stitched together → uploaded via n8n.

Full breakdown with a diagram is in [instructions.html](https://htmlpreview.github.io/?https://github.com/RandomSci/Video-Automation-Workflow-With-Manim/blob/main/instructions.html).

## This is the real pipeline

Not a demo. This is what's actually running two YouTube channels end to end:

- **[Math Unlocked](https://www.youtube.com/@MathUnlockedYT)** — math, statistics, and ML explainers
- **[FRC Finance](https://www.youtube.com/@FRCFinance)** — personal finance explainers

Both are fully automated on this exact codebase.

## Follow the build

- 💬 Discord (build logs, code drops, ask questions): [discord.gg/hYc2umc7Q](https://discord.gg/hYc2umc7Q)
- 🎓 Free automation course (new to n8n?): [AI Automation Mastery](https://whop.com/joined/selwyn-builds/course-ai-automation-mastery-build-systems-that--rc0jGvlp9zbLvh/app/)
- 🎥 YouTube (tutorials/build breakdowns): [@SelwynBuilds-j1s](https://www.youtube.com/@SelwynBuilds-j1s)
- 🎥 Math Unlocked: [@MathUnlockedYT](https://www.youtube.com/@MathUnlockedYT)
- 🎥 FRC Finance: [@FRCFinance](https://www.youtube.com/@FRCFinance)
- 💻 GitHub: [RandomSci](https://github.com/RandomSci)
- 📘 Facebook: [facebook.com/randomsci](https://facebook.com/randomsci)

## License

Free to use, modify, and build on. If it helps you ship something, that's the whole point.

---

*Built by Selwyn Jayme — Systems That Scale*
