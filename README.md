
## Overview

**Ayodance Ram Reduce** is a terminal-based memory optimizer built specifically for Ayodance — the rhythm game that holds a special place in Indonesian gaming culture. The tool monitors and trims the game's memory usage in real-time, helping it run smoother on low-to-mid spec machines.

## Why I Built This

Ayodance is beloved, but its memory behavior can get messy during long sessions — especially on older hardware. I wanted a zero-friction solution that just runs quietly in the background and keeps things smooth without needing to alt-tab out or tweak Windows settings manually.

## How It Works

The tool watches Ayodance's process in real-time and periodically trims its working set — freeing up memory that the game is holding but not actively using. All of this happens through a clean TUI so you can monitor what's going on without leaving your desk setup.

- Real-time process monitoring targeted at Ayodance
- Periodic working set trim to free unused memory
- Visual memory usage graph in the terminal
- Configurable trim interval and threshold
- Zero impact on gameplay — runs completely in the background

## Tech Stack

- **Golang** — process handling, Windows API calls, system memory management
- **TUI** — terminal interface with live memory graph and controls

## Usage

```bash
# Clone and run
git clone https://github.com/helloirfanaditya/ayodance-ram-reduce.git
cd ayodance-ram-reduce
```
Then run:
```bash
AMR.exe
```
> Make sure tool is running before launching the Ayodance.

## What I Learned

This project pushed me deeper into Windows process memory management from Go — specifically around `SetProcessWorkingSetSize` and how working sets differ from actual allocated memory. Also a good reminder that sometimes the best tools are the ones built for a very specific, very personal problem.