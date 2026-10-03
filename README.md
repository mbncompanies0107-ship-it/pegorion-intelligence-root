# Pegorion Intelligence Demo

Pegorion is a synthetic decision-intelligence demo for wireless infrastructure and lease operations.

## Run locally

```bash
npm install
npm run dev
```

Open `http://localhost:3000` for Tower Intelligence or `http://localhost:3000/lease` for Lease Intelligence.

## Five-minute Lease Intelligence demo

1. Open **Lease Intelligence** from the product switcher or visit `/lease`.
2. Turn on **CEO Demo Mode** in the left sidebar.
3. Open the featured lease `TX-10482` and review the extracted fields and source references.
4. Use **Important Dates** and **Obligations** to show how document language becomes workflow.
5. Open **Risk** to explain the score and traceable reasons.
6. Use **Ask Pegorion** and select a question to show a grounded answer with a page reference.
7. Open **Documents** to show the synthetic amendment comparison.
8. Open **Lease Portfolio** to show the 100-record synthetic portfolio.
9. To demonstrate upload, click **Upload Lease**, choose any local PDF, and review the local demo analysis result.

## Deploy to Vercel

The project is configured for Vercel with `vercel.json` and needs no API keys or environment variables.

```bash
npx vercel login
npx vercel
npx vercel --prod
```

Alternatively, import the Git repository at [vercel.com/new](https://vercel.com/new). Vercel will detect Next.js automatically.

## Deploy to Netlify

The project also includes `netlify.toml` for Netlify's Next.js runtime. Import the repository in Netlify, or use the CLI:

```bash
npm install -g netlify-cli
netlify login
netlify init
netlify deploy --build
netlify deploy --build --prod
```

## Demo boundaries

- All lease, tower, company, date, financial, obligation, and risk data is synthetic.
- The local `DemoLeaseAnalysisProvider` is an API-independent adapter. It can later be replaced by a document parser or an OpenAI, Gemini, Claude, or Azure OpenAI provider.
- Uploaded PDFs are kept in the browser flow only. The MVP does not upload them to a server or claim to extract arbitrary documents; the demo provider returns the clearly labeled synthetic hero analysis.
- Risk scores and recommendations are illustrative and are not legal advice.
