# Câte Drone? 🇷🇴

An interactive map and open database documenting **drone-related incidents in Romania**, built from official statements and verified public sources.

The goal is simple: make it easy to understand **where, when, and what happened** without digging through dozens of press releases and news articles.

> **Status:** Early development

## 🗺️ What is Câte Drone?

**Câte Drone?** (`cate-drone.ro`) is a public, interactive visualization of drone incidents connected to Romania.

Instead of presenting incidents as isolated news stories, the project aims to collect them into a structured dataset and display them geographically.

Each incident can include information such as:

- 📍 Location and coordinates
- 📅 Date and time
- 🚁 Incident type
- 🧩 Drone or debris information, when known
- 🏛️ Official statements
- 📰 Relevant public sources
- 🔗 Links to original sources
- ✅ Verification / confidence status

## 🎯 Goals

The project is designed around a few principles:

- **Accessible** — no account or login required
- **Source-driven** — incidents should be traceable to their original sources
- **Interactive** — explore incidents directly on a map
- **Transparent** — distinguish confirmed information from uncertain or incomplete reports
- **Automatable** — eventually detect and extract new incidents from trusted sources automatically
- **Expandable** — start with Romania, with the possibility of covering other regions in the future

## 💡 Planned Features

### Interactive Map

Explore incidents geographically instead of scrolling through a traditional database.

The map will focus on areas where incidents actually occurred rather than forcing a full-country view when the available data is concentrated in specific regions.

### Incident Details

Selecting an incident will provide its known details, sources, timeline, and verification status.

### Filters & Exploration

Potential filters include:

- date
- county / region
- incident type
- drone status
- source type
- verification status

### Automated Data Collection

A future ingestion pipeline may monitor trusted sources such as official Romanian institutions and public statements.

AI-assisted extraction could transform unstructured announcements into structured incident candidates containing:

```text
date
location
coordinates
incident type
description
source
confidence
```

Candidates can then be validated before becoming part of the public dataset.

## 🧱 Architecture

The architecture is still being designed.

The project will initially focus on a lightweight web application and interactive map, with data ingestion and automation added incrementally.

Initial direction:

```text
Trusted Sources
      ↓
Data Collection
      ↓
Extraction / Normalization
      ↓
Incident Database
      ↓
API / Application
      ↓
Interactive Map
```

## 🛠️ Tech Stack

Initial technologies under consideration:

- **Next.js**
- **TypeScript**
- **Leaflet / OpenStreetMap**
- Database and backend architecture — TBD
- AI-assisted data extraction — planned

The stack will evolve as the data model and ingestion requirements become clearer.

## 📊 Data Philosophy

The project should never present uncertain information as established fact.

Every incident should preserve its provenance:

```text
Incident
├── What happened?
├── Where?
├── When?
├── Who reported it?
├── What is officially confirmed?
├── What remains uncertain?
└── Where can the original source be found?
```

This makes the project both a visualization and a traceable historical dataset.

## 🌍 Future Direction

Romania is the starting point.

If the data collection and verification pipeline proves reliable, the same architecture could eventually support incidents across multiple countries and provide a broader view of drone activity geographically and over time.

---

**cate-drone.ro** — turning scattered reports into structured, explorable data.

This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
