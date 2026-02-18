🚀 AniBiee: AnimeWorldIndia Scraper API
<div align="center">
A high-performance RESTful API service for scraping and extracting structured data from AnimeWorldIndia.
</div>
📸 Preview
⚠️ Legal Disclaimer
> [!IMPORTANT]
> This API is provided for educational and research purposes only. Users are responsible for ensuring their use complies with all applicable copyright laws and terms of service. The developers do not endorse or facilitate piracy. All content accessed through this API remains the property of its respective copyright holders. Use responsibly and respect intellectual property rights.
> 
✨ Features
 * 🎬 Dynamic Content: Extract home page content (newest drops, trending, etc.)
 * 📺 Deep Extraction: Get detailed information about series and movies
 * 📚 Episode Management: Fetch episodes organized by season
 * 🎥 Stream Ready: Extract multiple embed player links automatically
 * 🔍 Advanced Browsing: Filter by category (movies, series, anime, cartoon, genres, languages)
 * 🔤 A-Z Index: Browse alphabetically by letter with full pagination
 * 🔎 Smart Search: Supports both AJAX suggestions and comprehensive page search
 * 🔒 Enterprise Security: Origin-based access control and rate limiting
 * 🛡️ Hardened Middleware: Integrated Helmet.js, CORS, and Compression
 * 📄 Custom UX: Professionally designed HTML error pages (403, 404)
⚙️ Prerequisites
 * Runtime: Node.js >= 18.0.0
 * Package Manager: npm or yarn
🛠️ Installation & Setup
 * Clone the Repository
   git clone https://github.com/DPModsPro/AnimeWorldIndia-Api.git
cd AniBiee-AnimeWorldIndia-scraper

 * Install Dependencies
   npm install

 * Environment Setup
   cp .env.example .env

 * Launch Service
   # Development mode (with auto-restart)
npm run dev

# Production mode
npm start

🔧 Configuration
Update your .env file with the following variables for secure operation:
PORT=3000
NODE_ENV=development
CORS_ORIGIN=https://example.com

Environment Variables Breakdown
| Variable | Description | Default |
|---|---|---|
| PORT | The port on which the server will listen | 3000 |
| NODE_ENV | Environment mode (development or production) | development |
| CORS_ORIGIN | Allowed domains (* for all, or comma-separated list) | * |
📡 API Reference
> [!NOTE]
> All endpoints are prefixed with /api and require valid headers if CORS_ORIGIN is restricted.
> 
🏠 Home Page
GET /api/home
Returns newest drops, trending content, and top movies.
📂 Category Listing
GET /api/category/{type}?page={page}
Types: movies, series, anime, cartoon, genre/sci-fi, language/hindi.
🔠 Alphabetical Browse
GET /api/letter/{letter}?page={page}
Letter: A through Z.
🔍 Search Engine
 * Suggestions: GET /api/search?suggestion=naruto
 * Full Search: GET /api/search?q=naruto
ℹ️ Series/Movie Details
GET /api/info/{id}
Returns complete metadata, including duration, genres, and episode lists.
📼 Episode Provider
GET /api/episodes/{id}/{season}
Retrieves all episodes for a specific series season.
🎬 Streaming Links
GET /api/embed/{id}
Fetches direct embed server links (Play, Abyss, etc.). Includes automatic fallback to series page if episode is 404.
💓 System Health
GET /api/health
Returns system status, uptime, and timestamp.
🕸️ Generic Scraper
GET /api/scrape?url={url}&extractor={extractor}
Scrape custom URLs using the internal engine.
🛡️ Security Architecture
1. Origin Blocking
 * Strict validation of Origin or Referer headers.
 * Automated 403 Forbidden responses for unauthorized traffic.
2. Rate Limiting
 * Threshold: 100 requests per 15 minutes per IP.
 * Protects against DDoS and scraping abuse.
3. Protection Layer
 * Helmet.js: Sets secure HTTP headers.
 * Compression: Optimized Gzip response sizes.
📂 Project Structure
AniBiee-AnimeWorldIndia-scraper/
├── public/              # Premium HTML pages (index, 404, 403)
├── src/
│   ├── base/           # Core scraper classes
│   ├── config/         # App configuration
│   ├── controllers/    # Logical route handlers
│   ├── extractors/     # Source-specific parsing logic
│   ├── middleware/     # Security & Rate-limiting
│   ├── routes/         # API Routing definitions
│   └── router.js       # Main Router integration
├── server.js           # Express entry point
└── .env.example        # Configuration template

❤️ Support the Project
If this API helps your project, please consider:
 * ⭐ Starring the repository on GitHub.
 * 📢 Joining our community: Telegram @SagaBox_app
 * 🌐 Visiting the developer: basirulakhlak.tech
📜 License & Copyright
Copyright (c) 2026 Basirul Akhlak Borno. All Rights Reserved.
Distributed under the ISC License. See LICENSE for details.
Would you like me to help you generate the professional LICENSE file or the .env.example file next?
