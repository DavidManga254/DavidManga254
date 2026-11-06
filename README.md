<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,100:2563eb&height=190&section=header&text=David%20Manga&fontSize=52&fontColor=ffffff&fontAlignY=38&desc=Full%20stack%20developer%20%C2%B7%20Nairobi%2C%20Kenya&descSize=18&descAlignY=60" width="100%" alt="David Manga, full stack developer, Nairobi, Kenya" />

<a href="https://github.com/DavidManga254">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1400&color=2563EB&center=true&vCenter=true&width=640&lines=React+and+TypeScript+on+the+front;Go+and+Java+on+the+back;Building+retrieval+and+LLM+features+into+real+products;I+write+code+I+can+test+and+explain" alt="Typing animation of what I work on" />
</a>

</div>

## About

I build web, mobile and desktop apps, from the interface down to the database. Most of my time goes into React and TypeScript on the front, with Go, Java, Node and PHP behind it. Lately I've been spending a lot of it on backend systems (streaming, queues, anomaly detection) and on making LLMs useful in real products.

I like work where I can check whether it's right: tests, screenshots, metrics, a diff that's either zero or isn't. Several of the projects below came out of that.

Based in Nairobi, Kenya.

## What I work with

<div align="center">

**Front end**

<img src="https://skillicons.dev/icons?i=react,ts,js,nextjs,vue,nuxt,tailwind,html,css,vite,storybook" alt="React, TypeScript, JavaScript, Next.js, Vue, Nuxt, Tailwind, HTML, CSS, Vite, Storybook" />

**Back end and data**

<img src="https://skillicons.dev/icons?i=go,java,spring,nodejs,nestjs,php,laravel,python,postgres,mysql,sqlite,prisma" alt="Go, Java, Spring, Node, NestJS, PHP, Laravel, Python, PostgreSQL, MySQL, SQLite, Prisma" />

**Mobile, desktop and tooling**

<img src="https://skillicons.dev/icons?i=electron,firebase,docker,git,github,playwright,jest" alt="Electron, Firebase, Docker, Git, GitHub, Playwright, Jest" />

</div>

React Native and Wails (Go) fill the mobile and desktop gaps: I've used React Native with Firebase Cloud Messaging, and Wails for a Go desktop app.

## Featured projects

| Project | What it is | Stack |
|---|---|---|
| [**Hala**](https://github.com/DavidManga254/Hala-Voting-System) | Blockchain voting system on Algorand. Each vote is a transaction to a candidate account, with an encrypted voter ID in the note to block double voting. **3rd place at the Algorand competition in Kenya, 2023.** Built with a teammate. | React, Express, Algorand SDK |
| [**VRT-system**](https://github.com/DavidManga254/VRT-system) | Visual regression pipeline. Pulls design frames from pencil.dev as baselines, screenshots each Storybook story with Playwright, diffs them pixel by pixel, and hands differences to Claude Code over MCP to fix. | Playwright, Storybook, React, Node, MCP |
| [**Stream-server**](https://github.com/DavidManga254/Stream-server) | Video streaming server. Upload, background FFmpeg transcoding to 360p/480p/720p, adaptive bitrate HLS delivery. A DB poller feeds a worker thread pool. | Java, FFmpeg, HLS, Docker |
| [**chat-bot-schedular**](https://github.com/DavidManga254/chat-bot-schedular) | Type a sentence, get a Google Calendar event. An LLM function call turns the text into a structured event (time, attendees, recurrence, reminders). | NestJS, OpenAI, Prisma, Next.js |
| [**Green-Harvest**](https://github.com/DavidManga254/Green-Harvest) | Farm produce marketplace with a customer app, a farmer dashboard, payments, subscriptions, chat and maps. | Laravel, React, TypeScript, Paystack |
| [**clipsy**](https://github.com/DavidManga254/clipsy) | Desktop clipboard manager that finds other devices on the LAN with UDP and connects over TCP. Early stage. | Go, Wails, React, SQLite |

More: [instaApp](https://github.com/DavidManga254/instaApp), a React Native chat app on Firebase Cloud Messaging, and [Echo](https://github.com/DavidManga254/Echo), a RAWG.io clone on Laravel and React.

## AI and retrieval (RAG)

I'm working through a five-phase RAG curriculum and building the labs in Python as I go. It follows the structure of DeepLearning.AI's RAG course: how RAG works, search foundations, vector databases, generation, and running it in production.

**What I've built so far**

- **Retrieval from scratch.** A keyword retriever, then BM25 written by hand and used to rank documents, so I know what the parameters do instead of just calling a library.
- **Semantic search** with sentence-transformers embeddings over the same passages.
- **Chunking and context windows.** I split articles into chunks and widen each hit with its neighbours. My first version sent near-duplicate passages to the model: on 25 test queries, 23 had two identical passages. Merging overlapping windows from the same article brought that to 0 of 25 and raised distinct articles per question from 3 to 5, with the source article still found in every query that had one.
- **Failure tests.** Scripts for the cases where retrieval breaks: synonyms with no shared words, questions the documents can't answer, and queries with zero keyword overlap. Each logs what was retrieved and what the model said.
- **Data.** The BBC News set (2,225 articles) plus a set of short invented stories.
- **Vector database.** Started on Weaviate (collections, import, queries) in Python.

**Where it's going**

Hybrid search with rank fusion, cross-encoder reranking, retrieval metrics (precision@k, recall@k, MRR), then evaluation with Ragas, request tracing, prompt-injection defences and cost tracking. After that, agents and tool use: function calling, MCP and multi-step loops.

**Already in real code**

- LLM function calling to turn free text into validated, structured data ([chat-bot-schedular](https://github.com/DavidManga254/chat-bot-schedular)).
- Claude Code reading a design tool over MCP as part of an automated fix loop ([VRT-system](https://github.com/DavidManga254/VRT-system)).

**Next application**

I'm applying this to a log monitoring backend I'm building in Java: Spring Boot, PostgreSQL, a disk-backed ingest queue, per-service baselines with z-score anomaly detection, incident grouping, and Slack and Discord alerts. The plan is retrieval over logs and incidents so an engineer can ask what changed. That repo is private for now.

## Backend and systems

- **Queues and workers:** DB-polled job queues feeding thread pools (Stream-server), disk-backed ingest buffering, leases so two workers don't send the same alert.
- **Networking:** UDP discovery and TCP handshakes in Go (clipsy), HLS streaming, WebSockets and FCM push in React Native chat apps.
- **APIs and auth:** NestJS and Laravel APIs with role-separated middleware, Google OAuth, signed httpOnly cookies, encrypted token storage.
- **Data:** PostgreSQL with Prisma and Flyway, MySQL with Laravel migrations, SQLite in desktop apps.

## Stats

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=DavidManga254&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" alt="GitHub stats" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=DavidManga254&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" alt="Most used languages" />

</div>

## Get in touch

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-DavidManga254-0f172a?style=for-the-badge&logo=github&logoColor=white)](https://github.com/DavidManga254)
<a href="https://www.linkedin.com/in/david-manga-313419234/"><img src="https://raw.githubusercontent.com/DavidManga254/DavidManga254/main/assets/linkedin.webp" height="40" alt="LinkedIn" /></a>
</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2563eb,100:0f172a&height=90&section=footer" width="100%" alt="" />
