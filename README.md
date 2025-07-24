# ESP32 Smart Gate – Frontend

This is the frontend interface for the ESP32 Smart Gate project — a modern, PIN-based gate access system with a mobile-first web UI.

The system enables residents to generate guest PINs, and allows guests to unlock a barrier or gate using a secure 4-digit code entered via a clean web interface. It is fully self-hosted, requires no subscriptions or proprietary hardware, and integrates with an ESP32 controller using Blynk and Cloudflare Workers.

> Built using React + Tailwind  
> Deployed using GitHub Pages  
> Designed for mobile access

---

## Live Demo

You can preview the public deployment here:  
[https://tinkeriotops.github.io](https://tinkeriotops.github.io)

---

## Features

- Guest interface for secure PIN entry
- Admin interface for generating temporary PINs
- Device status monitoring (via Blynk)
- QR code and community info display
- Language switcher (RO / EN)
- Fully responsive, mobile-optimized UI

---

## Installation

Clone the repo:

```bash
git clone [https://github.com/tinkeriotops/esp32-barrier-fe.git](https://github.com/tinkeriotops/tinkeriotops.github.io.git)
cd esp32-barrier-fe
npm install
```

### Set the API Base URL

Update the backend URL in:

- `src/hooks/useBarrier.ts`
- `src/components/GuestPinGenerator.tsx`

```ts
const CLOUDFLARE_API = "https://your-backend-subdomain.workers.dev";
```

Replace with your deployed backend Worker URL.

---

## Deployment via GitHub Pages (GitHub Actions)

This project uses a GitHub Actions workflow for automatic deployment.

Make sure the following is configured in `vite.config.ts`:

```ts
export default defineConfig({
  base: "/",
  build: {
    outDir: "docs"
  },
  ...
});
```

To deploy:

1. Commit and push to the `main` branch.
2. GitHub Actions will build and publish the frontend to Pages.
3. Your site will be live at:  
   `https://tinkeriotops.github.io/esp32-barrier-fe`

No manual build or FTP upload required.

---

## Full Build Guide

Want the complete step-by-step tutorial? Including backend, firmware, wiring, and hosting?

Read the full article here:

**[How I Built a Secure, Web-Based Smart Gate with ESP32](https://tinkeriot.com/esp32-smart-gate-access)**

Includes diagrams, screenshots, architecture, platform limits, and best practices.

---

## License & Usage

This project is provided for personal use.

You are allowed to:

- Fork, clone, or adapt the project for personal use
- Host it privately or on your own domain

You are not allowed to:

- Resell, redistribute, or share any part of the source code, guides, or product package
- Upload the files to a public GitHub repository as a public resource for others

Public forks are allowed only if they remain personal and unadvertised.

---

## Support

If this project saved you time or helped bring your idea to life, you can support continued updates and development:

[https://ko-fi.com/yourname](https://ko-fi.com/yourname)

Thank you.
