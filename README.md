# React Native & Expo Complete Skills

The most comprehensive React Native, Expo, and React optimization skills for Claude Code. Combines **130+ rules** from Callstack, Expo, and Vercel best practices.

## Installation

In Claude Code, run:

```
/plugin marketplace add gigs-slc/react-native-skills
/plugin install react-native-expo-complete@react-native-expo-skills
```

Then restart Claude Code to load the skills.

## What's Included

### 10 Skills + 8 Agents + Templates

#### Skills

| Skill | Source | Content | Description |
|-------|--------|---------|-------------|
| `react-native` | **Callstack + Vercel** | 65 files | **THE ULTIMATE RN SKILL** - Combined profiling + patterns |
| `react-best-practices` | Vercel | 62 files | React patterns, hooks, performance, architecture |
| `composition-patterns` | Vercel | 12 files | Component composition, compound components |
| `building-ui` | Expo | 14 files | UI components, styling, animations, navigation |
| `data-fetching` | Expo | 1 file | fetch, axios, React Query, SWR, caching |
| `api-routes` | Expo | 1 file | API routes with Expo Router + EAS Hosting |
| `dev-client` | Expo | 1 file | Development client builds, TestFlight |
| `tailwind-setup` | Expo | 1 file | Tailwind CSS v4 + NativeWind v5 setup |
| `upgrading-expo` | Expo | 4 files | SDK upgrades, React 19, New Architecture |
| `use-dom` | Expo | 1 file | DOM components, web-to-native migration |

#### Agents

| Agent | Use When | Description |
|-------|----------|-------------|
| `orchestrator` | Coordinating multi-agent workflows | Master coordinator that enforces constraints and delegates to sub-agents |
| `react-native-expo-architect` | BEFORE implementation | Designs features, makes architectural decisions, creates implementation plans |
| `react-native-expo-implementation` | AFTER architecture plan exists | Writes production code following the approved plan |
| `react-native-expo-code-review` | AFTER code is written | Reviews diffs, validates scope, checks for bugs and constraint violations |
| `react-native-expo-bugfix` | Investigating runtime errors | Diagnoses crashes, bugs, and errors without implementing fixes |
| `performance-re-render` | Performance matters | Identifies re-renders, memory leaks, JS thread issues |
| `navigation-expo-router` | Navigation behavior involved | Validates routes, params, deep links, platform parity |
| `mobile-release-gate` | Before merging/shipping | Final production-readiness check - SHIP or NO SHIP decision |

### Agent Workflow

The agents work together in a specific sequence:

```
User Request
    ↓
[Orchestrator] - Reads constraints, delegates work
    ↓
[Architect] - Designs the solution (if new feature)
    ↓
[Implementation] - Writes the code
    ↓
[Code Review] - Validates the changes
    ↓
[Performance] - Checks for performance issues (if applicable)
    ↓
[Navigation] - Validates routing (if applicable)
    ↓
[Release Gate] - Final approval before ship
    ↓
[Orchestrator] - Updates progress, reports completion
```

### Orchestrator Agent

The **Orchestrator Agent** is the master coordinator. It:
- Reads `AI_CONSTRAINTS.md` before any work begins
- Tracks progress in `AI_PROGRESS.md`
- Delegates to specialized agents based on task type
- Ensures proper agent sequencing
- Never violates constraints

### Project Governance Templates

The `templates/` folder contains starter files for AI governance:

| Template | Purpose |
|----------|---------|
| `AI_CONSTRAINTS.md` | Define non-negotiable rules for all AI agents |
| `AI_PROGRESS.md` | Track work status, decisions, and blockers |

**Setup:**
1. Copy templates to your project's `docs/` folder
2. Customize constraints for your codebase
3. Reference in your `CLAUDE.md` or project instructions

### The Unified `react-native` Skill

The crown jewel - combines **Callstack profiling** with **Vercel code patterns**:

```
skills/react-native/
├── SKILL.md              # Combined quick reference
├── AGENTS.md             # Full 74KB Vercel compiled guide
├── rules/                # 36 Vercel rule files
│   ├── list-performance-*.md
│   ├── animation-*.md
│   ├── ui-*.md
│   ├── react-state-*.md
│   └── ...
└── references/           # 27 Callstack reference files
    ├── js-*.md           # FPS, re-renders, memory, animations
    ├── native-*.md       # TTI, profiling, Turbo Modules
    ├── bundle-*.md       # Size analysis, tree shaking, R8
    └── images/
```

### Coverage Areas

**Performance (Callstack)**
- FPS measurement & re-render profiling
- Bundle size analysis & tree shaking
- TTI optimization & native profiling
- Memory leak detection (JS & native)
- Hermes optimization, R8, compression

**Code Patterns (Vercel)**
- List virtualization (FlashList, LegendList)
- Animation best practices (Reanimated)
- React state patterns & architecture
- React Compiler compatibility
- UI components (native menus, modals, images)

**Expo & React (Expo + Vercel)**
- Expo Router navigation
- Data fetching strategies
- Tailwind/NativeWind styling
- SDK upgrades & migrations
- React hooks & composition patterns

## Usage

After installation, invoke skills in Claude Code:

```
/react-native              # THE BIG ONE - Callstack + Vercel combined
/react-best-practices      # General React patterns
/composition-patterns      # Component architecture
/building-ui               # Expo UI patterns
/data-fetching             # API & caching
```

## Attribution

This collection combines skills from:
- **Callstack** - "The Ultimate Guide to React Native Optimization"
- **Vercel** - React Native Skills, React Best Practices, Composition Patterns
- **Expo** - Official Expo skills for app development

## License

MIT - See individual skill directories for original licenses.
