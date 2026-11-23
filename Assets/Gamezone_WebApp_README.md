<h1 align="center">GameZone 🎮</h1>

<p align="center">
A gaming news and discovery portal with <b>Jarvis</b>, an AI support chatbot that talks like a friend and turns visitors into leads.
</p>

<p align="center">
  <a href="https://gamingarena-alpha.vercel.app/">Live Demo</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js" />
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" alt="Tailwind CSS" />
  <img src="https://img.shields.io/badge/OpenAI_GPT--4o-412991?style=for-the-badge&logo=openai&logoColor=white" alt="GPT-4o" />
  <img src="https://img.shields.io/badge/MCP-444444?style=for-the-badge" alt="MCP" />
  <img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Vercel" />
</p>

<p align="center">
  <img src="assets/jarvis-home.png" alt="GameZone homepage with the Jarvis chat open" width="90%">
</p>

---

## Overview

GameZone is a dark-themed gaming portal covering news, featured AAA games, reviews, esports, videos, and community pages. A chat widget called **Jarvis** sits on every page. It is powered by GPT-4o with an MCP backend and answers questions about games, reviews, release dates, news, and esports in a simple, friendly tone. While chatting, Jarvis asks for the visitor's name, phone number, and email so interested visitors become leads for the parent website.

## Jarvis in Action

<table>
  <tr>
    <td width="33%" valign="top" align="center">
      <img src="assets/jarvis-search-games.png" alt="Jarvis searching games" width="100%">
      <br><sub><b>1. Search.</b> Jarvis shows "Searching games" while it looks up the best-rated title.</sub>
    </td>
    <td width="33%" valign="top" align="center">
      <img src="assets/jarvis-game-details.png" alt="Jarvis reading game details" width="100%">
      <br><sub><b>2. Details.</b> It shows "Reading game details", then answers with a link to the game page.</sub>
    </td>
    <td width="33%" valign="top" align="center">
      <img src="assets/jarvis-lead-capture.png" alt="Jarvis asking for the visitor's name" width="100%">
      <br><sub><b>3. Lead capture.</b> After helping, Jarvis asks "what should I call you?" to start collecting contact details.</sub>
    </td>
  </tr>
</table>

## Features

- **Homepage:** a hero carousel for featured stories, latest news, featured games with scores, and upcoming releases with a wishlist button
- **News:** latest news and patch notes
- **Games:** full game library, top-rated list, and a release calendar
- **Reviews:** game reviews and hardware reviews
- **Esports:** tournaments, match schedule, and team rankings
- **Videos:** trailers and gameplay
- **Community:** forums and leaderboards
- **Jarvis support chat:** a floating chat widget with plain, easy language, live tool-status messages, and links to game pages
- **Lead capture:** collects name, phone number, and email inside the conversation

## Meet Jarvis

Jarvis is a floating chat widget on every page, marked "GameZone support · Online". It answers questions about games, reviews, release dates, news, and esports in simple, friendly language, with bold highlights, bullet points, and links to the relevant game pages.

1. A visitor asks a question in the chat.
2. Jarvis calls MCP tools to get the data it needs, shown in the chat as "Searching games" and "Reading game details".
3. GPT-4o writes a short, friendly answer with a link to the game page.
4. Once the visitor is engaged, Jarvis asks what to call them, then their phone number and email.
5. The details are validated and saved through an MCP tool to TODO: storage (database / sheet / CRM).
6. The visitor can reset the conversation at any time with the refresh button.

## Architecture

<p align="center">
  <img src="assets/architecture.png" alt="GameZone architecture: visitor to Next.js frontend to API routes to GPT-4o, with an MCP server for game data and lead storage" width="95%">
</p>

<!-- TODO: list your MCP tools. Visible in the UI so far: search games, read game details. Add the lead-saving tool name. -->

## Tech Stack

| Layer | Tools |
|---|---|
| Frontend | Next.js, React, Tailwind CSS |
| AI | OpenAI GPT-4o |
| Backend | Next.js API routes, MCP |
| Deployment | Vercel |

## Getting Started

```bash
git clone https://github.com/Sanchal-01/Gamezone_WebApp.git
cd Gamezone_WebApp
npm install
```

Create a `.env.local` file in the project root:

```
OPENAI_API_KEY=your_key_here
# TODO: add any other variables (lead storage, MCP server URL, etc.)
```

Run the app:

```bash
npm run dev
```

Open `http://localhost:3000`.

## Privacy and Data Handling

Jarvis collects a visitor's name, phone number, and email only to follow up on their interest. The chat tells visitors why their details are requested before it asks for them. API keys stay on the server and are never exposed to the browser.

<!-- TODO: add retention period and how a visitor can request deletion -->

## Sample Content Notice

Articles, scores, esports data, upcoming release dates, and the site statistics are sample content for demonstration. Game titles are trademarks of their respective owners. Photos are from Unsplash.

## Roadmap

- [ ] TODO: planned features

## License

Released under the MIT License.
