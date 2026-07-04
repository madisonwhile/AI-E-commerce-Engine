# AI E-Commerce Production Engine

A multi-agent AI production engine that transforms a simple creative brief into production-ready creative assets for e-commerce brands.

The system analyses a brand's identity, product photography, moodboards and campaign references before generating multiple prompt types, including catalogue photography, website imagery and cinematic banner video prompts—all while maintaining consistent creative direction.

This project explores how AI can automate creative preparation—not creativity itself.

---

## The Problem

Creating consistent AI-generated marketing imagery is difficult.

Most workflows rely on manually writing prompts for every product, requiring repeated descriptions of the same garments, lighting, composition and brand identity. The process is slow, difficult to scale and often produces inconsistent results across campaigns.

My previous workflow solved this problem for a single brand using manually written prompt guides, but it wasn't flexible enough for real-world client work.

I wanted to design a system capable of understanding entirely new brands from a creative brief alone.

---

## The Solution

Instead of building one large prompt, I designed a modular multi-agent architecture.

Each agent performs a specialised task before passing structured information to the next stage, allowing the system to gradually build an understanding of the brand before generating production-ready prompts.

The engine analyses:

- Brand identity
- Target audience
- Creative goals
- Product photography
- Moodboards
- Existing campaign imagery

The final output is a structured set of production-ready prompts including:

Catalogue product photography
Website and lifestyle imagery
Cinematic banner video concepts

allowing brands to generate consistent creative assets across multiple marketing channels from a single creative brief.
---

## Core Features

- Multi-agent workflow architecture
- Learns new brands from structured creative briefs
- Product understanding using uploaded product photography
- Moodboard and campaign reference analysis
- Brand identity extraction
- Catalogue image prompt generation
- Website lifestyle image prompt generation
- Banner video prompt generation
- Multiple prompt variations per product
- Reusable architecture designed for any brand or industry

---

## Architecture Overview

Creative Brief
        │
        ▼
Brand Analysis Agent
        │
        ▼
Product Analysis Agent
        │
        ▼
Prompt Generation Agent
        │
        ▼
   Output Agent
        │
        ▼
Production Ready Prompts

Each stage has a single responsibility, making the workflow easier to improve, debug and extend than relying on one large prompt.

---

## One of the Biggest Design Decisions

Early versions attempted to describe products entirely through text.

Despite increasingly detailed prompts, product accuracy remained inconsistent.

After extensive experimentation, I redesigned the workflow so uploaded product photography became the primary visual reference. Instead of repeatedly describing garments, the generated prompts focus on:

- atmosphere
- lighting
- composition
- styling
- camera direction
- brand identity

This significantly improved consistency while giving the image model more creative freedom.

---

## Current Limitations

Version 1 intentionally stops after prompt generation.

The original architecture included an additional agent responsible for automatically sending prompts to Higgsfield for image generation.

Due to API credit limitations, this stage was temporarily removed and prompts are currently pasted into Higgsfield manually.

The architecture has been designed so automatic generation can be reintroduced in a future release.

---

## Technologies

- Python
- Claude
- Multi-Agent Architecture
- Prompt Engineering
- Generative AI
- Higgsfield
- Nano Banana Pro

---

## Repository Structure

README.md

Architecture.md

Prompt Design.md

Lessons Learned.md

Roadmap.md

Assets/

---

## Future Roadmap

- Build a modern web application frontend
- User authentication and client workspaces
- Automated Higgsfield integration
- Campaign project management
- Brand knowledge libraries

---

## Why I Built This

This project wasn't about generating images.

It was about exploring how AI systems can understand creative intent.

One of the biggest lessons from building this engine was realising that better outputs rarely come from writing longer prompts—they come from designing better systems.

That idea has become a recurring theme throughout my work and continues to shape the creative tools I build today.
