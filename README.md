# RunMyModel - Cloudflare Worker

A production-ready Cloudflare Worker project that serves a dark mode landing page with a guided workflow for GPU selection.

## Features

- **Dark Mode Landing Page**: Modern, responsive design with TailwindCSS
- **Interactive GPU Selection Workflow**: Step-by-step process for choosing GPUs
- **API Endpoints**: Health check and selection submission endpoints
- **Responsive Design**: Works on desktop and mobile devices
- **Production Ready**: Configured for deployment to Cloudflare Workers

## Project Structure

```
RunMyModel/
├── src/
│   └── index.js          # Main Cloudflare Worker entrypoint
├── package.json          # Dependencies and scripts
├── wrangler.toml         # Cloudflare Workers configuration
└── README.md            # This file
```

## Pages

- **`/`** - Landing page with hero section and GPU selection workflow
- **`/why-us`** - Advantages and features page
- **`/contact`** - Contact form and support information

## API Endpoints

- **`/api/health`** - Health check endpoint returning status and uptime
- **`/api/selector`** - POST endpoint for submitting GPU selections

## GPU Selection Workflow

The interactive workflow guides users through:

1. **GPU Brand Selection**: NVIDIA, Intel, AMD
2. **GPU Family Selection**: RTX, ADA, Arc, Radeon, etc.
3. **VRAM Range Selection**: 30s, 40s, 50s series
4. **Specific Model Selection**: Individual GPU models

## Development

### Prerequisites

- Node.js 18+ 
- Wrangler CLI (`npm install -g wrangler`)

### Local Development

```bash
# Install dependencies
npm install

# Start local development server
npm run dev
```

### Deployment

```bash
# Deploy to Cloudflare Workers
npm run deploy
```

## Configuration

The `wrangler.toml` file is configured for deployment to `runmymodel.org/*`. Update the domain and zone settings as needed for your deployment.

## Styling

- **TailwindCSS**: Loaded via CDN for rapid styling
- **Dark Mode**: Fully dark theme with good contrast
- **Responsive**: Mobile-first design approach
- **Custom Colors**: Primary blue, secondary dark blue, accent cyan

## Browser Support

- Modern browsers with ES6+ support
- TailwindCSS via CDN
- No external dependencies beyond TailwindCSS

## License

MIT License - see LICENSE file for details.