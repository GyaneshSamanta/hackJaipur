<div align="center">
  <img src="repository-assets/cover.png" width="80%" alt="HackJaipur" />

# MoodWiz

**Be kind to your mind — a privacy-first mental wellness web app built at HackJaipur 2020.**

[![Hackathon](https://img.shields.io/badge/Built%20at-HackJaipur%202020-ff6f00.svg)](https://devfolio.co/hackjaipur/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://lbesson.mit-license.org/)
[![Deploy](https://img.shields.io/badge/Deployed-Azure-0078d4.svg)](#)

</div>

---

## About

|        |                                                                                            |
| ------ | ------------------------------------------------------------------------------------------ |
| Who    | Team **codeBlooded** from SRM Institute of Science and Technology, Kattankulathur.          |
| What   | A web app for self-discovery, mood support, and connecting with mental health professionals. |
| When   | June 2020 — built across one weekend at **HackJaipur** (MLH).                              |
| Where  | Browser-first; deployed on Azure App Service. A Kotlin WebView wrapper ships an Android build. |
| Why    | India has ~4,000 mental health professionals for 1.3B people. Tech can raise the line.      |

## The Story

The numbers are the entire reason this exists. The WHO estimates **7.5% of India** lives with some form of mental disorder, the treatment gap is **over 70%**, and the country has fewer than 4,000 mental health professionals to meet that demand. On top of the supply problem, stigma keeps people from even acknowledging there's something to treat.

We built **MoodWiz** as the lowest-friction front door we could imagine: no account, no data collection, no cloud-stored conversation history. Open the page and pick a path. **Discover** is the soft entry — read explainers, watch professional-recorded videos, hear calming music, or sketch on a digital canvas that saves nothing. **Connect** is for when reading isn't enough — a video-call room (Agora.io) for sessions with counselors, a DialogFlow chatbot that assesses mood and tells jokes, motivational speeches, and a printable habit tracker.

Our design principles were deliberate: **cloud-first, mobile-first, minimalist, reusable.** The reusable part matters — the same shell can be rebadged for any awareness campaign with a similar shape (helpline + content + connect).

We won the hackathon's mental-health-aid problem statement, and just as importantly we ended the weekend with something we'd actually recommend to a friend.

## Gallery

<div align="center">
  <img src="repository-assets/1.png" width="80%" alt="Landing" />
  <img src="repository-assets/2.png" width="80%" alt="Guide" />
  <img src="repository-assets/3.png" width="80%" alt="Sketch" />
  <img src="repository-assets/4.png" width="80%" alt="Video call" />
  <img src="repository-assets/5.png" width="80%" alt="Listen" />
</div>

---

## Tech Stack

- **Frontend:** HTML, CSS, JavaScript
- **Hosting:** Microsoft Azure App Service (auto-deployed via GitHub Actions)
- **Realtime:** Agora.io for video calls
- **Conversational AI:** Google Cloud DialogFlow
- **Forms / Surveys:** Collect.chat
- **Auth/Backend (selective):** Firebase
- **Mobile:** Kotlin WebView wrapper (`Android/`)

## Repo Structure

```
hackJaipur/
├── index.html               # Main landing
├── login.html               # Optional sign-in flow
├── style.css / script.js    # Top-level styling + behavior
├── Discover/                # Read / Watch / Listen modules
├── Canvas/                  # Sketchboard
├── Connect/                 # Connect hub
├── Videocall/               # Agora.io video session room
├── Chatbot/                 # DialogFlow integration
├── NavDocs/                 # Navigation pages / static docs
├── Android/                 # Kotlin WebView wrapper
├── assets/ + media/         # Images, audio, video
└── repository-assets/       # README screenshots
```

## Getting Started

```bash
git clone https://github.com/GyaneshSamanta/hackJaipur.git
cd hackJaipur
# Open index.html in any modern browser. An internet connection is required
# for DialogFlow, Agora.io, and other third-party integrations to function.
```

For local serving with hot-reload, any static server works:

```bash
npx serve .
```

## Contributing

PRs welcome — particularly anything that hardens accessibility (this is a mental-health tool; that audience deserves a polished experience). Open an issue first for content additions to the *Discover* sections so we can vet sources.

## License

[MIT](https://lbesson.mit-license.org/).

## Credits

Team **codeBlooded** — SRM Institute of Science and Technology:

- [Aaishika S Bhattacharya](https://github.com/aaishikasb) — Team Lead
- [Souharda Biswas](https://github.com/TheSouharda)
- [Akash Ramjyothi](https://github.com/akash-ramjyothi)
- [Gyanesh Samanta](https://github.com/GyaneshSamanta)

Resources: WHO mental health statistics, [Indian suicide data](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6902359/), and the counselors who reviewed our flow.
