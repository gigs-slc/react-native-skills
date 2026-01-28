# React Native & Expo Complete Skills

The most comprehensive React Native, Expo, and React optimization skills for Claude Code. Combines **130+ rules** from Callstack, Expo, and Vercel best practices.

## Installation

```bash
# Add the marketplace
claude plugins:marketplace:add github:gigs-slc/react-native-skills

# Install all skills
claude plugins:install react-native-expo-complete@react-native-expo-skills
```

## What's Included

### 10 Skills with 130+ Rules

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
