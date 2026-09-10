# Focus Flow

A single-file Pomodoro-style focus timer that runs entirely in the browser.

Set focus and break lengths, start the timer, and each completed focus
session plants something new in your garden for the day. Progress
(sessions, streaks, and today's garden) is saved to `localStorage`, so it
persists between visits without any backend.

## Features

- Focus / Short Break / Long Break modes with a circular progress ring
- Configurable focus, short break, and long break durations
- Automatically cycles to a long break after every 4 focus sessions
- A daily "garden" that grows a new plant per completed focus session
- Tracks today's session count, total sessions, and best streak
- A short audio chime when a session ends

## Usage

Open [`index.html`](index.html) directly in any modern browser — no build
step, server, or dependencies required.
