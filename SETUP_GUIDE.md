# Content Hub - Complete Setup Guide

## Quick Start (5 minutes)

### 1. Clone Repositories

```bash
# Navigate to workspace
cd D:\quantumsearch-engine

# Clone Content Hub
git clone https://github.com/netguy47/content-hub.git

# Clone QuantumLeap
git clone https://github.com/netguy47/Quantum-Leap-search-Engine.git
```

### 2. Run Setup Script

**Windows:**
```bash
cd content-hub
powershell -ExecutionPolicy Bypass -File setup.ps1
```

**Mac/Linux:**
```bash
cd content-hub
chmod +x setup.sh
./setup.sh
```

### 3. Configure Environment Variables

Edit `content-hub/.env` and add your credentials:

```env
# Substack Credentials
SUBSTACK_EMAIL=donwoods@substack.com
SUBSTACK_PASSWORD=your_password_here

# QuantumLeap Configuration
QUANTUMLEAP_API_URL=http://localhost:3000
QUANTUMLEAP_API_KEY=your_quantumleap_api_key_here

# App Configuration
NEXT_PUBLIC_APP_URL=http://localhost:3001
```

### 4. Start QuantumLeap

```bash
# Terminal 1
cd D:\quantumsearch-engine\Quantum-Leap-search-Engine
npm install
npm run dev
```

QuantumLeap will be available at: http://localhost:3000

### 5. Start Content Hub

```bash
# Terminal 2
cd D:\quantumsearch-engine\content-hub
npm run dev
```

Content Hub will be available at: http://localhost:3001

---

## API Endpoints

When both servers are running:

### Health Check
```bash
GET http://localhost:3001/api/health
```

### Generate Analysis
```bash
POST http://localhost:3001/api/analyze
Content-Type: application/json

{
  "topic": "South China Sea tensions",
  "mode": "GEOPOLITICAL",
  "depth": "deep",
  "includeScenarios": true,
  "includeHeatmap": true,
  "formatAsArticle": true
}
```

### Full Pipeline (Analyze + Publish)
```bash
POST http://localhost:3001/api/publish
Content-Type: application/json

{
  "topic": "Economic volatility in supply chains",
  "mode": "ECONOMIC",
  "depth": "deep",
  "autoPublish": false,
  "publishDelay": 24,
  "sendEmail": true
}
```

---

## Available Modes

- `GENERAL` - Cross-domain correlations
- `ECONOMIC` - Volatility & supply chain
- `MILITARY` - OSINT & force posture
- `GEOPOLITICAL` - Geopolitical analysis
- `CIVIL_UNREST` - Crowd dynamics & protest flashpoints
- `STRATEGY` - High-level decision modeling
- `TRAVEL` - Executive protection & extraction routes
- `CRIME` - Urban risk & resource mapping
- `POLICE` - Urban risk & resource mapping

---

## CLI Commands

### Generate Analysis
```bash
npm run generate:analysis -- --topic "Your topic here" --mode GEOPOLITICAL
```

### Publish to Substack
```bash
npm run publish:substack -- --input output/pipeline-xxx.json --autoPublish true
```

### Full Pipeline
```bash
npm run pipeline -- --topic "Your topic" --mode ECONOMIC --autoPublish true
```

---

## Troubleshooting

### QuantumLeap Not Responding
- Ensure QuantumLeap is running on port 3000
- Check QuantumLeap logs for errors
- Verify `QUANTUMLEAP_API_URL` in .env

### Substack Authentication Failed
- Verify email and password in .env
- Check if Substack account is active
- Ensure email/password combination is correct

### Dependencies Failed to Install
- Ensure Node.js 20+ is installed: `node --version`
- Clear npm cache: `npm cache clean --force`
- Delete node_modules and reinstall: `rm -rf node_modules && npm install`

---

## Project Structure

```
D:\quantumsearch-engine\
├── Quantum-Leap-search-Engine/    # QuantumLeap (port 3000)
├── content-hub/                   # Content Hub (port 3001)
│   ├── src/
│   │   ├── integrations/
│   │   │   └── quantumleap/      # QuantumLeap API client
│   │   ├── generators/            # Content generation
│   │   ├── publishers/
│   │   │   └── substack/          # Substack client
│   │   └── utils/
│   ├── api/                       # Next.js API routes
│   ├── pages/                     # React frontend
│   ├── scripts/                   # CLI utilities
│   └── output/                    # Generated content
└── content-hub-heartbeat/         # Documentation
```

---

## Development

```bash
# Run tests
npm test

# Build for production
npm run build

# Start production server
npm start

# Lint code
npm run lint
```

---

## Support

For issues or questions:
1. Check [heartbeat.md](https://github.com/netguy47/content-hub-heartbeat/blob/main/heartbeat.md) for project status
2. Review [README.md](https://github.com/netguy47/content-hub) for usage documentation
3. Check logs in `content-hub/logs/` directory
