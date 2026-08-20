# Câte Drone? 🇷🇴

An interactive map and open database documenting **drone-related incidents in Romania**, built from official statements and verified public sources.

The goal is simple: make it easy to understand **where, when, and what happened** without digging through dozens of press releases and news articles.

> **Status:** Early development

## 🗺️ What is Câte Drone?

**Câte Drone?** (`cate-drone.ro`) is a public, interactive visualization of drone incidents connected to Romania.

Instead of presenting incidents as isolated news stories, the project aims to collect them into a structured dataset and display them geographically.

Each incident can include information such as:

* 📍 Location and coordinates
* 📅 Date and time
* 🚁 Incident type
* 🧩 Drone or debris information, when known
* 🏛️ Official statements
* 📰 Relevant public sources
* 🔗 Links to original sources
* ✅ Verification / confidence status

## 🎯 Goals

The project is designed around a few principles:

* **Accessible** — no account or login required
* **Source-driven** — incidents should be traceable to their original sources
* **Interactive** — explore incidents directly on a map
* **Transparent** — distinguish confirmed information from uncertain or incomplete reports
* **Automatable** — eventually detect and extract new incidents from trusted sources automatically
* **Expandable** — start with Romania, with the possibility of covering other regions in the future

## 💡 Planned Features

### Interactive Map

Explore incidents geographically instead of scrolling through a traditional database.

The map will focus on areas where incidents actually occurred rather than forcing a full-country view when the available data is concentrated in specific regions.

### Incident Details

Selecting an incident will provide its known details, sources, timeline, and verification status.

### Filters & Exploration

Potential filters include:

* date
* county / region
* incident type
* drone status
* source type
* verification status

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

* **Next.js**
* **TypeScript**
* **Leaflet / OpenStreetMap**
* Database and backend architecture — TBD
* AI-assisted data extraction — planned

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
