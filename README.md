# 7thWorld - World Expansion & Upkeep Plugin

7thWorld is a server-wide progression system for Paper/Spigot networks.  
Players fund world growth together, then defend that growth each month through upkeep.

## What is it

- Collaborative world expansion tied to a shared contribution pool.
- Monthly upkeep cycle that keeps the world stable when goals are met.
- Automatic border shrink penalty ("Incursion") if upkeep is missed.
- Clean in-game GUI for status, contributions, and contributor rankings.
- Bedrock-friendly menu support (via Geyser/Floodgate forms).
- Discord webhook announcements for all major world events.
- Persistent data saving for uninterrupted long-term progression.

## Core Systems

- Expansion System
  - Server collects expansion funding.
  - Reaching the target cost instantly increases world border size.
  - Supports repeat expansion cycles.
- Upkeep System
  - Monthly upkeep requirement is calculated from server economy snapshot.
  - If upkeep is paid, world remains safe.
  - If unpaid, border de-expands by configured amount (never below minimum size).
- Economy Snapshot System
  - Reads Vault economy balances.
  - Includes player balances and optional Towny town/nation accounts.
  - Uses Essentials account discovery when available for stronger coverage.
- Player Contribution System
  - Separate contribution channels for Expansion and Upkeep.
  - Tracks top contributors for both systems.
  - Supports quick presets and custom amount input.
- UI/UX System
  - Main menu dashboard with live progress bars.
  - Contribution submenus and chat-based amount entry.
  - Bedrock form fallback for cross-platform usability.
- Discord Notification System
  - Expansion unlocked alerts.
  - New upkeep month announcements.
  - Upkeep deadline reminders (with optional role mention).
  - Upkeep defended and incursion alerts.
- Admin Control System
  - Live status command.
  - Force monthly upkeep check command.
  - Manual border expand/shrink command with safety confirmation window.
- Persistence & Reliability
  - Auto-save on interval and on shutdown.
  - Stores expansion pool, upkeep cycle data, contributors, and reminder state.

## Command Access

- Main command: `/worldexpansion`
- Aliases: `/worldupkeep`, `/worldmenu`
- Key subcommands:
  - `status`
  - `forcemonth` (admin)
  - `border` / `borderconfirm` / `bordercancel` (admin)


## Configuration Highlights

- Select target world and timezone.
- Set expansion cost and border increase size.
- Set upkeep percentage, de-expansion amount, and minimum border.
- Customize menu title/prefix.
- Enable/disable Discord events individually.
- Configure upkeep reminder timing thresholds.

## Product Positioning

This plugin is designed for economy-driven survival servers that want long-term shared goals, recurring risk, and visible community progression tied directly to the world border.
