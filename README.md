- 👋 Hi, I’m @Clar17y
- 👀 I’m interested in learning how to work with AI tools and expand my coding knowledge
- 🌱 I’m currently starting with Python and Cursor but will try new things when I can!

My first project is creating an application to help my Grassroots football team.

# ⚽️ Personal Projects - Grassroots Football Tools

## 🟢 Project 1: Pitch Allocation System

A pitch allocation system designed to help grassroots clubs allocate teams to pitches each week — inspired by my son's club where the fixture secretary used pen and paper.

**Development Steps:**
1. Build a Python application to allocate teams across available pitches.
2. Add user-defined constraints (e.g. specific teams, pitch availability).
3. Develop a simple UI in Python.
4. Convert the application into a mobile-friendly website usable by club members.

---

## 🟡 Project 2: Football Events Management System (Spreadsheet Edition)

Started as a personal effort to gain insight into my son's team’s performance by tracking match data in a spreadsheet. The goal was to ask AI questions like:
- Who was the most improved player?
- What interesting stats can you share about the team?
- What do the game notes say about our progress?

**Problems Encountered:**
- Data formatting issues made it hard for AI (ChatGPT) to analyse effectively.
- I manually restructured the spreadsheet into a clearer format that resembled a relational database.

**Evolution:**
- Created a PostgreSQL database mirroring the spreadsheet structure.
- Focused on a central `Events` table, e.g.:

| match_id | time               | period_number | kind  | team_id | player_id | player_name | performance | goal_for | goal_against | notes                                                        |
|----------|--------------------|----------------|-------|---------|-----------|--------------|-------------|-----------|---------------|--------------------------------------------------------------|
| 1        | 15/09/2024 11:07:12 | 1              | goal  | 1       | 8         | Player1      | Solid (+1)  | 1         | 0             | Scored from a corner                                          |
| 1        | 15/09/2024 11:07:12 | 1              | assist| 1       | 3         | Player2      | Solid (+1)  | 0         | 0             | Scored from a corner                                          |
| 1        | 15/09/2024 11:07:44 | 1              | goal  | 2       |           |              |             | 0         | 1             | Right winger caused problems and a lucky toe poke goal       |

> Design went from allowing multiple players per row (e.g. goal scorer + assister) to two separate rows, hence some duplication

**Next Idea:**
Build a live match-tracking app to log these events in real time during games instead of retroactively from video.

**Shoutout:** [pitchfeed.co.uk](https://www.pitchfeed.co.uk) – they beat me to it and even trialled with our club via my wife. Their app focuses on live updates for families; mine’s focused on personal stats and analysis.

---

## 🔵 Project 3: Football Events Management System

Same foundation as Project 2, but now accelerated using [Atlassian Rovodev](https://www.atlassian.com/rovodev) (Claude 4 Sonnet under the hood). Code generation is vastly faster, even though I’m still learning TypeScript and React.
I've since moved on to Codex CLI tool which is now running ChatGPT 5 Codex model and am very impressed with the ability of it.

This phase is about scaling the application, exploring how far AI-assisted development can take a hobbyist project, and maintaining control over quality and direction as complexity grows.
Now includes co-authored commits from Claude using Claude Code on web and Opus 4.5. Using 4.5 Opus as much as possible through Kiro / AntiGravity and Claude Code interface. Codex 5.2 XHigh is also pretty good using Codex CLI!
Will be looking soon to productionise what I have an get it hosted in AWS!

## 🟠 Project 4: Football Video Analysis

With the success I've had using Codex CLI tool, is it possible to create my own software that will take the footage I've captured of the grassroots football team and analyse it with AI? e.g. can I get the events from the 3rd project created automatically by analysing it with software that I train using my data and autopopulate the events.

Update: More time consuming than beneficial... got it working but the amount of time needed to train the model would make this not worth the time. Also, as the camera pans and the players move in and out of the shot it would be very difficult for the model to track each player - how does it know who the player who came into the frame is? How do you attribute stats to them if they're never identified before going out of frame again? etc. Parked this for now.

## 🟣 Project 5: Savvy Hampers Inventory Manager

Mobile-first inventory, costing, and margin tracking for a hamper / kit business (built for an Etsy seller).

### Features

- Lot-based inventory with expiry dates and FIFO allocation
- Barcode scanning (camera or handheld scanner input) for fast stock entry
- Hamper definitions with category-based requirements and real-time "can make" availability
- Sales recording with automatic stock consumption and margin calculation (including Etsy fees)
- Business expenses tracking (packaging, ads, postage, etc.)
- Analytics dashboards plus low-stock / expiring alerts
- Optional Etsy integration to sync listing inventory (real mode or mock mode for dev)
- Historical import from spreadsheets (sales + expenses)

### Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React + Vite + TypeScript + TailwindCSS |
| Backend | Express + TypeScript |
| Database | PostgreSQL |
| ORM | Prisma |
| Auth | Supabase (magic links) |
| Barcode | html5-qrcode |
