# Age of Command

> *A real-time strategy game where the enemy thinks — plans, adapts, and fights back.*
---

## Overview

**Age of Command** is a Unity-based real-time strategy game built around a single design ambition: making the AI opponent feel genuinely intelligent. Rather than scripted responses or stat-inflated cheating, the enemy commander reasons about the battlefield, forms plans, and executes them with coordinated units — all in real time.

The project serves as both a playable RTS and a technical showcase of applied game AI, combining two complementary paradigms into a unified decision-making architecture.

---

## Core Features

### 🧠 Hybrid AI Architecture

The AI brain is built on two layered systems that work in concert:

- **GOAP (Goal-Oriented Action Planning)** handles *long-term strategic thinking*. The AI defines high-level goals — secure a resource point, destroy the enemy base, establish a defensive perimeter — and dynamically constructs action sequences to achieve them based on the current world state. Plans are re-evaluated as conditions change.

- **Behavior Trees** handle *short-term and tactical execution*. Once a strategic directive is issued, individual units and squads follow structured behavioral logic: patrol, engage, retreat, regroup, flank. The tree reacts fluidly to immediate threats without disrupting the broader plan.

This separation of concerns means the AI can *think big and act smart* simultaneously.

---

### 🪖 Formation Movement & Squad Cohesion

Units don't just move — they move *together*. The squad system supports dynamic formation assignments (line, wedge, column, surround).

### ⚙️ Escalade Auto-Management

The AI manages its own economy and unit production autonomously. *Escalade* refers to the AI's ability to:

- Monitor resource income and expenditure
- Prioritize tech progression or unit count based on strategic context
- Self-regulate production queues without player input
- Adapt its build strategy in response to scouting information

This system frees the GOAP planner to focus on strategic objectives rather than micromanaging base logistics.

---

### 🌫️ Fog of War

Full fog-of-war implementation creates genuine information asymmetry:

- Units reveal vision in a dynamic radius around them.  
- Enemy positions, movements, and structures are hidden outside explored areas
- The AI operates under the same fog constraints as the player — it scouts, remembers last-known positions, and acts on incomplete information
- Memory decay mechanics ensure the AI doesn't have perfect recall of stale intelligence

---

## Built With

- **Engine**: Unity
- **Language**: C#
- **AI Paradigms**: GOAP · Behavior Trees
- **Pathfinding**: NavMesh + custom formation steering
- **Fog of War**: Compute shader-based visibility grid

---

## Status

🚧 **In active development** — core AI architecture implemented, gameplay systems in progress.

---
