# Robotics Engineering Curriculum

The Robotics Engineering Curriculum is the source-of-truth content repository for a long-term robotics engineering programme.

This repository contains the educational content only. The website is a separate application that reads curriculum data and renders it as an interactive learning platform.

## Purpose

This curriculum is designed to support 5-10 years of structured learning across software, embedded systems, electronics, mechanical engineering, robotics, AI, computer vision, and humanoid robotics.

It is not a website codebase, LMS implementation, or task tracker. It is a content system for a complete engineering programme.

## Repository Structure

```text
robotics-engineering-curriculum/
  README.md
  docs/
  curriculum/
    phase-1/
      module-1/
        week-1/
          mission-0.md
          mission-1.md
  projects/
  skills/
  hardware/
  resources/
  templates/
  images/
```

## Curriculum Hierarchy

The curriculum is organised as:

```text
Curriculum
  Phase
    Module
      Week
        Mission
```

Each mission is stored as an independent Markdown document. Weekly projects, skills, hardware pages, and resources are stored separately so they can be reused across the programme.

## How The Website Consumes This Repository

The website should treat this repository as a content source.

Current integration stage:

- The website still renders from local TypeScript seed data.
- The app now has a curriculum source boundary so the UI does not need to know whether content came from TypeScript, Markdown, a Git checkout, or an API.
- Future work can replace the seed loader with a Markdown loader that reads this repository.

Target integration:

1. Clone or fetch this repository.
2. Parse Markdown files and front matter.
3. Convert content into the website curriculum schema.
4. Render the same UI from parsed curriculum data.

## Writing Standards

Every mission should be:

- Independent enough to be reviewed by itself.
- Connected to a weekly project.
- Clear about prerequisites.
- Clear about why the learning matters to robotics.
- Written in professional engineering language.
- Structured enough to be parsed by software later.

## Markdown Conventions

- Use kebab-case filenames.
- Use one mission per file.
- Keep headings stable and predictable.
- Use relative links for local curriculum references.
- Put reusable concepts in `skills/`, not repeated long explanations inside every mission.
- Put reusable hardware explanations in `hardware/`.
- Put project build briefs in `projects/`.

## Naming Conventions

Mission files:

```text
mission-0.md
mission-1.md
mission-2.md
```

Project files:

```text
reaction-time-analyser.md
traffic-light-controller.md
weather-station.md
```

Skill files:

```text
gpio.md
adc.md
state-machines.md
queues.md
```

Hardware files:

```text
raspberry-pico-2-wh.md
raspberry-pi-zero.md
button.md
ldr.md
```

## Repository Standards

Every project must include:

- GitHub repository
- README
- Circuit diagram
- Wiring photos
- Source code
- Demo video
- Lessons learned
- Future improvements

Every mission must include:

- Title
- Mission number
- Estimated time
- Difficulty
- Mission objective
- Why this matters
- Theory
- Coding
- Hardware
- Challenge
- Reflection
- Engineering notebook
- Success criteria
- Stretch goal
- Resources
- GitHub repository
- Related project
- Related skills
- Related hardware
- Prerequisites

## Status

This repository is currently a scaffold. The full curriculum will be written manually over time.
