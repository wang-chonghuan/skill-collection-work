---
name: cloudflare-skills-installer
description: Install the official Cloudflare Skills bundle for AI agents using the Cloudflare-published skills repository. Use when a user asks to add, install, verify, or refresh Cloudflare/Wrangler/Workers skills, or wants their agent to know how to deploy Cloudflare static sites, Workers, Pages, Durable Objects, or use Wrangler.
---

# cloudflare-skills-installer

Install Cloudflare's official Skills bundle from the Cloudflare-published repository so agents can work with Cloudflare, Wrangler, Workers, Pages/static assets, Durable Objects, Agents SDK, and web performance guidance.

## When to use

Use this skill when the user asks for an official or ready-made Cloudflare skill, mentions Cloudflare Skills, Wrangler skill, Workers skill, Cloudflare deployment skill, or wants agent help deploying static sites to Cloudflare.

## Install

Run from the user's intended workspace or home directory:

```bash
npx skills add https://github.com/cloudflare/skills
```

If npm asks to install the `skills` package, answer `y` unless the user asked for dry-run only.

## Verify

After installation, confirm the expected skill directories exist:

```bash
ls ~/.agents/skills | grep -E '^(cloudflare|wrangler|workers-best-practices)$'
```

Useful official skills commonly installed by the bundle include:

- `cloudflare`
- `wrangler`
- `workers-best-practices`
- `web-perf`
- `durable-objects`
- `agents-sdk`
- `cloudflare-email-service`
- `sandbox-sdk`

## Use after install

For static sites and Workers assets, prefer the installed `cloudflare`, `wrangler`, and `workers-best-practices` skills. Typical user prompts:

- "Use the Cloudflare skill to deploy this static site."
- "Use the Wrangler skill to check and deploy this project."
- "Install official Cloudflare skills for this agent."

## Notes

- This is the official existing Cloudflare Skills bundle installation path: `https://github.com/cloudflare/skills`.
- Review installed skills before use; they run with agent permissions.
- If installation fails because npm cannot fetch packages or GitHub, report the exact network/package error and do not invent a fallback skill as if it were official.
