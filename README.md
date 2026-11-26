# 320+ Study Room — 2027 UTME

A free, local-first study website for the two UTME tracks. It has the 91-day schedule, topic checklists, original CBT-style practice, progress tracking, and an optional on-device AI tutor.

## Cost and privacy

- No API key, account, paid model call, or server-side AI is used.
- Lessons, quizzes, tutor chat, and progress are kept in the browser's local storage. They do not sync between learners or devices in this version.
- Each browser downloads the selected model the first time the tutor is loaded. The Lite model uses about 945 MB of estimated memory; the Standard model uses about 1.6 GB. The first download uses internet data. A compatible WebGPU browser is required.
- The AI model is small and can make mistakes. Verify syllabus and admission details with JAMB's official IBASS.
- A public site host is not configured in this folder. Publishing requires choosing a static host; this app does not call a paid service.

## Run locally

The tutor requires a secure site address (HTTPS) or localhost. Do not open `index.html` directly from a `file://` address.

If Python is available, run its built-in static server from this folder:

```powershell
py -m http.server 8000
```

Then open `http://localhost:8000`. The model library and model files download the first time the tutor is loaded.

## Study calendar

- November 30, 2026 through February 28, 2027, inclusive.
- Daily two-hour session: 9:00–11:00 p.m. Africa/Lagos.
- First hour: shared Use of English and Government.
- Second hour: each learner's separate subjects.

The schedule uses broad topic sequences based on JAMB's current public syllabus pages. Recheck the 2027 syllabus and prescribed literature list in IBASS when JAMB updates them. The example questions included here are original practice questions, not copied or verified past questions.

## Tutor technology

The tutor uses [WebLLM](https://github.com/mlc-ai/web-llm), which runs model inference in the browser using WebGPU. See [WebLLM's setup guide](https://github.com/mlc-ai/web-llm/blob/main/docs/user/get_started.rst) and its [model memory estimates](https://webllm.mlc.ai/models/).

