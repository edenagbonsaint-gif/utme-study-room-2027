# 320+ Study Room — 2027 UTME

A free UTME study website for the two tracks. It has a flexible 91-day plan, topic checklists, original CBT-style practice, progress tracking, an on-device AI tutor, and a temporary direct chat room for study partners.

## Cost and privacy

- The AI tutor uses no API key, account, paid model call, or server-side AI.
- Tutor chat, quizzes, and progress are kept in the browser's local storage. They do not sync between learners or devices.
- Partner chat uses the free PeerJS Cloud signaling service to connect two browsers, then sends messages directly over an encrypted peer connection. It does not save chat history. The invite code lets someone join the room, so share it only with your study partner. Keep the room open on both devices; some networks may block direct peer connections.
- Each browser downloads the selected model the first time the tutor is loaded. The Lite model uses about 945 MB of estimated memory; the Standard model uses about 1.6 GB. The first download uses internet data. A compatible WebGPU browser is required.
- The AI model is small and can make mistakes. Verify syllabus and admission details with JAMB's official IBASS.
- The public version is hosted on GitHub Pages from the public repository. No paid hosting or AI service is used.

## Run locally

The tutor requires a secure site address (HTTPS) or localhost. Do not open `index.html` directly from a `file://` address.

If Python is available, run its built-in static server from this folder:

```powershell
py -m http.server 8000
```

Then open `http://localhost:8000`. The model library and model files download the first time the tutor is loaded.

## Study calendar

- November 30, 2026 through February 28, 2027, inclusive.
- Choose a one-hour or two-hour session and set its start time from the dashboard; the default is 9:00 p.m. Africa/Lagos.
- One-hour sessions rotate through shared subjects and the selected learner's track subjects.
- Two-hour sessions split the shared first hour into 30 minutes each for English and Government, then use the second hour for one track subject.
- The schedule changes the plan display but does not send notifications.

The schedule uses broad topic sequences based on JAMB's current public syllabus pages. Recheck the 2027 syllabus and prescribed literature list in IBASS when JAMB updates them. The example questions included here are original practice questions, not copied or verified past questions.

## Tutor technology

The tutor uses [WebLLM](https://github.com/mlc-ai/web-llm), which runs model inference in the browser using WebGPU. See [WebLLM's setup guide](https://github.com/mlc-ai/web-llm/blob/main/docs/user/get_started.rst) and its [model memory estimates](https://webllm.mlc.ai/models/). Partner chat uses [PeerJS](https://peerjs.com/); its [FAQ](https://peerjs.com/client/faq) explains the free signaling service and direct data connection.

