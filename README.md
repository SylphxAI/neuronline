# NeuronLine

> **Archived — no longer maintained (2026-09-24).** This repository is read-only and has no replacement.

⚡ Modern online learning neural network library for real-time user behavior prediction

## Features

- 🚀 **High Performance** - Core inference < 1ms, optimized for browser environments
- 🪶 **Lightweight** - Core < 20KB gzipped, full bundle < 50KB
- 🎯 **Accurate** - Incremental learning with experience replay for better predictions
- 🔒 **Privacy-First** - 100% local computation, no data leaves the browser
- 📦 **Modular** - Use only what you need with tree-shakeable exports
- 🔄 **Real-time** - True online learning, updates with every interaction

## Quick Start

```bash
bun add @sylphx/neuronline
```

```typescript
import { NeuronLine } from '@sylphx/neuronline'

// Initialize
const learner = new NeuronLine({
  scenario: 'ecommerce',
  storage: 'indexeddb',
})

// Track user behavior
learner.track('view', { productId: '123', category: 'electronics' })
learner.track('click', { productId: '123' })

// Get predictions
const recommendations = await learner.predict('next-action', {
  context: { currentPage: 'home' },
})
```

## Use Cases

- 🛒 **E-commerce** - Product recommendations, dynamic pricing, offer optimization
- 📰 **Content Platforms** - Article recommendations, reading time prediction
- 🎨 **UI/UX** - Navigation prediction, resource prefetching
- 📝 **Forms** - Smart autocomplete, field prediction

## Development

```bash
# Install dependencies
bun install

# Run tests
bun test

# Build packages
bun run build

# Lint and format
bun run check
```

## Architecture

```
neuronline/
├── packages/
│   ├── core/          # Core online learning engine
│   ├── predictors/    # Prediction modules
│   ├── storage/       # Local storage adapters
│   └── privacy/       # Privacy utilities
└── apps/
    └── demo/          # Demo applications
```

## License

MIT © SylphxAI
