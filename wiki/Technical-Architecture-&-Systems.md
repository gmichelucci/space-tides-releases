# ⚙️ Technical Architecture & Systems

Space Tides is engineered with **Godot Engine 4** utilizing an optimized, decoupled module architecture.

## 🗂️ Module Layout
- `Core/`: Core engine lifecycle, state machines (`GameManager.gd`), match loops, and arena coordinators (`arena.gd`).
- `Data/`: Godot Custom Resources (`.tres`) defining hull statistics, weapon attributes, and pilot implants.
- `Entities/`: World instances categorized by `Ships/`, `Structures/`, `Weapons/`, and `Neutral/`.
- `UI/`: Responsive HUD, shop interfaces, cyber-grid login terminals, and tactical status docks.
- `Network/`: Multiplayer WebRTC signaling (`WebRTCSignaling.gd`) and low-latency peer-to-peer battle synchronization.
- `launcher/`: Standalone Windows desktop launcher with automatic checksum verification and release auto-updating.

## 🔒 Security & Cloud Sync
Authentication and persistent profile metadata are handled via Supabase API integration with secure token caching and Guest Mode failover.
