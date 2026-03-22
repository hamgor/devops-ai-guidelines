# Preface

This book exists because I couldn't hire a project manager.

I'm an engineer. My job is infrastructure, pipelines, and keeping production running. But when our PM left and the headcount wasn't backfilled, I became the person chasing status updates, grooming the backlog, running standups, and writing sprint reports — on top of my actual work. The team kept shipping, but the seams were showing. Tasks slipped through the cracks. Blockers went unnoticed for days. Sprint planning was a guessing game.

I spent weeks looking for a tool that could take the operational weight off my shoulders. Workflow automations were too rigid. Chatbots were too shallow. No-code PM tools solved the wrong problems. Then I found OpenClaw — an AI agent framework that could actually integrate with the tools my team already used: JIRA and Slack. I started building, and within a few weekends, I had a prototype that could read our sprint board, summarize progress, collect async standups, and flag blockers before I noticed them.

It wasn't perfect. The agent hallucinated tasks, misread priorities, and once confidently reported a sprint as on track when we were days behind. But each failure taught me something, and each iteration made the system more reliable. After months of building, evaluating, and refining, the AI PM became something my team actually depended on.

This book is the guide I wish I'd had when I started — the decisions that mattered, the mistakes that were avoidable, and the frameworks that turned a side project into a production system.

## Who This Book Is For

This book is for anyone who has touched project management — whether it's your job title or just your reality — and wants to use AI to do it better. Specifically:

- **Tech leads and engineering managers** who have absorbed project management responsibilities by default. You didn't sign up for sprint planning, backlog grooming, or stakeholder reporting, but the work landed on you and nobody's coming to take it back. You're context-switching between technical decisions and coordination overhead, and it's costing you delivery velocity and focus. This book shows you how to offload the operational mechanics of PM to an AI agent — so you can stay in the technical leadership role you were hired for while keeping your team organized and accountable.

- **Startup founders and CTOs** running teams of 3 to 30 where hiring a full-time PM doesn't make financial or structural sense yet. Coordination can't stay ad hoc — missed handoffs, unclear priorities, and invisible blockers are already slowing you down — but you need a solution that scales with your team, not one that requires a dedicated headcount. This book gives you a way to stand up lightweight, AI-driven PM workflows that grow as your team grows, without the overhead of a traditional PM hire.

- **Project managers and scrum masters** who already have the domain expertise but spend too much of their day on operational mechanics — compiling status reports, chasing updates across Slack threads, manually tracking blockers, and synthesizing sprint data into stakeholder narratives. An AI PM agent doesn't replace your judgment; it removes the busywork that prevents you from exercising it. This book shows you how to build an AI assistant that handles the repetitive, time-consuming parts of your role so you can focus on the higher-order work: strategic prioritization, team dynamics, risk management, and stakeholder alignment. For PMs managing multiple squads or projects simultaneously, the patterns in this book offer a path to scale your effectiveness without scaling your hours.

- **Anyone curious about AI agents in practice** — not the marketing slides, not the demo videos, but a real system integrated into real team tools handling real work. If you've been following the AI agent space and want to see what it looks like to actually build, ship, and maintain one in a production team environment, this book is a concrete, end-to-end case study.

You don't need prior experience with AI, machine learning, or natural language processing. You do need working familiarity with JIRA (or similar task trackers), Slack (or similar communication tools), and enough comfort with code to follow along with configuration and integration examples. This is not a book for passive readers — you'll get the most out of it by building alongside each chapter.

## What You'll Build

By the end of this book, you will have built a working AI project manager powered by OpenClaw that:

- **Connects to JIRA** to read, create, update, and transition issues across your team's boards and sprints.
- **Lives in Slack** as a bot your team interacts with naturally — answering questions, collecting standups, and pushing updates.
- **Automates sprint rituals** including status summarization, standup collection, blocker detection, and progress reporting.
- **Supports task management** with intelligent routing, workload awareness, and priority-based suggestions.
- **Evaluates its own performance** through structured metrics, automated pipelines, and feedback loops that improve the system over time.
- **Runs in production** with proper security boundaries, reliability patterns, and monitoring.

The system is modular. You can adopt the pieces that fit your team's needs and skip the rest. Every component is built incrementally — starting from a minimal prototype and growing based on real usage.

## How This Book Is Organized

The book follows the natural arc of building an AI PM from scratch, organized into three phases:

**Chapters 1–4: Problem, Tools, and First Build.**
Chapter 1 establishes why teams struggle without PMs and why AI agents are a viable solution. Chapter 2 introduces OpenClaw and the technology stack. Chapters 3 and 4 are hands-on: setting up the environment, wiring integrations, and shipping a working prototype.

**Chapters 5–10: Understanding, Patterns, and Evaluation.**
Chapter 5 examines how AI agents fail and how to debug them. Chapter 6 tears down real PM workflows to develop judgment about what AI should handle. Chapter 7 codifies the patterns that work (and the ones that don't). Chapters 8, 9, and 10 build a complete evaluation and feedback system — from defining metrics to closing the production learning loop.

**Chapters 11–14: Strategy, Adoption, and Production.**
Chapter 11 addresses the strategic dimensions of AI PM adoption. Chapter 12 covers the human side — getting teams to trust and use the system. Chapter 13 is production engineering: security, reliability, and scale. Chapter 14 offers an honest retrospective and practical guidance for readers starting their own implementation.

Each chapter is designed to be read in sequence, but experienced practitioners can skip directly to the chapters most relevant to their stage.

## Conventions Used in This Book

The following typographical conventions are used throughout:

- *Italic* is used for new terms and emphasis.
- `Constant width` is used for code, configuration files, commands, environment variables, and tool names.
- **Constant width bold** is used for commands or text that the reader should type literally.
- Code blocks contain complete, runnable examples wherever possible. Abbreviated examples are clearly marked.

## How to Use the Code Examples

All code examples, agent configurations, and prompt templates referenced in this book are available in the companion repository. The examples are designed to work with OpenClaw, JIRA Cloud, and Slack — the specific versions and compatibility notes are documented in Chapter 3.

You are free to use the code in your own projects without requesting permission. Adapting the examples for your team's specific workflow is expected and encouraged.
