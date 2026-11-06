<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,100:2563eb&height=190&section=header&text=David%20Manga&fontSize=52&fontColor=ffffff&fontAlignY=38&desc=Full%20stack%20developer%20%C2%B7%20Nairobi%2C%20Kenya&descSize=18&descAlignY=60" width="100%" alt="David Manga, full stack developer, Nairobi, Kenya" />

<a href="https://github.com/DavidManga254">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1400&color=2563EB&center=true&vCenter=true&width=900&lines=React+and+TypeScript+on+the+front;Go+and+Java+on+the+back;Building+retrieval+and+LLM+features+into+real+products;I+write+code+I+can+test+and+explain" alt="Typing animation of what I work on" />
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

## AI and retrieval

I'm working through a RAG curriculum in Python, building each lab as I go.

- **Built:** BM25 from scratch, semantic search with embeddings, chunking with context merging, and failure tests for synonyms, unanswerable questions and zero keyword overlap. Started on Weaviate.
- **Next:** hybrid search and reranking, Ragas evaluation, then agents and tool use.
- **In real code:** LLM function calling in [chat-bot-schedular](https://github.com/DavidManga254/chat-bot-schedular), and Claude Code over MCP in [VRT-system](https://github.com/DavidManga254/VRT-system).
- **Applying it to:** a log monitoring backend in Java (private for now).

## Backend and systems

- **Queues and workers:** DB-polled job queues feeding thread pools (Stream-server), disk-backed ingest buffering, leases so two workers don't send the same alert.
- **Networking:** UDP discovery and TCP handshakes in Go (clipsy), HLS streaming, WebSockets and FCM push in React Native chat apps.
- **APIs and auth:** NestJS and Laravel APIs with role-separated middleware, Google OAuth, signed httpOnly cookies, encrypted token storage.
- **Data:** PostgreSQL with Prisma and Flyway, MySQL with Laravel migrations, SQLite in desktop apps.

## Get in touch

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-DavidManga254-0f172a?style=for-the-badge&logo=github&logoColor=white)](https://github.com/DavidManga254)
<a href="https://www.linkedin.com/in/david-manga-313419234/"><img src="https://raw.githubusercontent.com/DavidManga254/DavidManga254/main/assets/linkedin.webp" height="40" alt="LinkedIn" /></a>
</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2563eb,100:0f172a&height=90&section=footer" width="100%" alt="" />
