This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.

Description:
To enable real-time metrics reporting for payment data, we need an aggregation table that calculates and stores key metrics (e.g., total number of payments, total payment amount) at defined intervals. Instead of an ETL job, this aggregation table will pull data directly from the Glue table (data in S3) using Amazon Athena or Redshift Spectrum. The table will allow the frontend UI to display metrics up-to-date without significant data movement or transformation processes.

Acceptance Criteria:
An aggregation table is created and populated by querying Glue tables using Athena or Redshift Spectrum.
Glue table schema is set up correctly, reflecting the required payment data structure.
Metrics (e.g., total payments, total payment amount) are calculated directly from the Glue table and updated every 15 minutes.
API endpoint provides access to the latest metrics for display in the frontend UI.
