# Image AI

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Image AI is a web-based design tool that combines a rich canvas editor with AI services for generating and editing images. It helps creators build professional assets quickly with easy templates, AI-assisted features, and a modern subscription model.

## Table of Contents

- [Features](#features)
- [Demo](#demo)
- [Setup](#setup)
  - [Simple Mode Setup](#simple-mode-setup)
  - [Advanced Mode Setup](#advanced-mode-setup)
- [Usage](#usage)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [FAQ](#faq)
- [License](#license)
- [Acknowledgements](#acknowledgements)
- [Contact](#contact)

## Features

- Manage design projects and templates with a PostgreSQL database.
- Rich canvas editor supporting text, shapes, drawing, filters and more.
- AI powered image generation and background removal using Replicate.
- Stock image search from Unsplash right inside the editor.
- Auth with credentials, GitHub or Google via NextAuth.
- Subscription and billing flows handled by Stripe.
- Real‑time updates and caching with React Query and Zustand.
- Upload and store assets through UploadThing.
- Responsive UI built with Next.js 14 and Tailwind CSS.

## Demo

Coming soon!

## Setup

Both quick start and advanced steps are provided below. Ensure all environment variables are configured.

### Simple Mode Setup

1. **Clone the Repository**
   ```bash
   git clone [repo-url]
   cd designer
   ```

2. **Install Dependencies**

   ```bash
   npm install
   ```

3. **Configure Environment**

   ```bash
   cp .env.example .env.local
   ```

   Required variables:

   * `DATABASE_URL`
   * `NEXT_PUBLIC_APP_URL`
   * `AUTH_SECRET`
   * `NEXT_PUBLIC_UNSPLASH_ACCESS_KEY`
   * `REPLICATE_API_TOKEN`
   * `STRIPE_SECRET_KEY`
   * `STRIPE_PRICE_ID`
   * `STRIPE_WEBHOOK_SECRET`
   * `GITHUB_CLIENT_ID` and `GITHUB_CLIENT_SECRET`
   * `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET`

4. **Run the App**

   ```bash
   npm run dev
   ```

### Advanced Mode Setup

- Provision a PostgreSQL instance (the project uses Neon) and update `DATABASE_URL`.
- Configure OAuth credentials for GitHub and Google in your developer consoles.
- Set up a Replicate account for AI services and provide `REPLICATE_API_TOKEN`.
- Configure Stripe products and webhooks, then fill in `STRIPE_SECRET_KEY`, `STRIPE_PRICE_ID`, and `STRIPE_WEBHOOK_SECRET`.
- Adjust any additional environment variables as needed for production.

## Usage

1. Sign up or log in with your preferred provider.
2. Create a new project or start from a template.
3. Use the editor sidebars to add text, shapes, images and apply filters.
4. Generate new images or remove backgrounds with the AI tools.
5. Save your project and return to the dashboard to manage or duplicate it.

## Deployment

The app is optimized for Vercel. After configuring your environment variables in the Vercel dashboard, you can deploy directly from GitHub.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/import)

## Contributing

Contributions are welcome! Fork the repo, create a branch and open a pull request describing your changes. Please run `npm run lint` and ensure the project builds before submitting.

## FAQ

**How do I get an Unsplash API key?** Create a developer account at [Unsplash](https://unsplash.com/developers) and generate an access key.

**Why do some templates require a subscription?** Certain premium templates and AI features are limited to paying users. Subscribe via the Stripe checkout to unlock them.

**Where are my images stored?** Uploaded files are handled through UploadThing and stored securely on their CDN.

## License

This project is licensed under the MIT license.

## Acknowledgements

- [Next.js](https://nextjs.org/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Drizzle ORM](https://orm.drizzle.team/)
- [Hono](https://hono.dev/)
- [Stripe](https://stripe.com/)
- [Replicate](https://replicate.com/)
- [Unsplash](https://unsplash.com/)
- [UploadThing](https://uploadthing.com/)

## Contact

For questions or support, please open an issue on this repository.
