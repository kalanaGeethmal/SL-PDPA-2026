# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a single-file static web application — an interactive reference guide for the Sri Lanka Personal Data Protection Act (PDPA) No. 9 of 2022 and its 2025 amendments. There is no build process, package manager, or external dependencies.

## Running the App

Open `index.html` directly in a browser. No server, build step, or install required.

## Architecture

Everything lives in `index.html` — HTML structure, embedded `<style>` CSS, and inline `<script>` JavaScript. The two PDFs in `Files/` are the official legislative source documents (Act No. 9 of 2022 and Amendment Act No. 22 of 2025).

**UI structure (all in index.html):**
- Tab-based navigation switching content sections into/out of view
- Expandable accordion sections for legal text references
- Interactive compliance checklist with per-item checkbox state (persisted via `localStorage`) and category filtering
- Progress bar calculated from checked items

**Design system (embedded CSS):**
- Dark theme with gold accents (`--ink`, `--gold`, `--cream` CSS variables)
- Fonts loaded from Google Fonts: Playfair Display (headings), DM Mono (metadata/code), DM Sans (body)

## Content Domains

The checklist and reference content covers: lawful bases (Schedules I & II), data subject rights, automated decision-making/profiling, cross-border transfers (S.26), DPO requirements, and breach notification obligations.
