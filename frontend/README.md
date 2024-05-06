# MultiOnChat Web

[🎥Video demo](https://youtu.be/XVZFZJgEtfA)

This is the frontend repository for MultiOnChat, check out [multionchat-platform](https://github.com/justinsunyt/multionchat-platform) for the backend code.

## Tech Stack

- Frontend: Next.js, TanStack Query, Tailwind, shadcn/ui, Framer Motion, Lucide, Sonner, Spline
- Backend: FastAPI, Supabase
- AI: MultiOn, Replicate, Groq

## Features

- Autonomously browse the internet with your own AI agent using only an image and a command - order a Big Mac, schedule events, and shop for outfits!
- Supabase database and email authentication with JWT token verification for RLS storage
- Currently supports llama3-70b, llava-13b, lava-v1.6-34b, qwen-vl-chat

## Getting Started

First, create a Supabase project with authentication. Make sure the same project is also used for the backend.

Next, create a .env.local file in the root of the project and store the following variables:

```bash
NEXT_PUBLIC_SUPABASE_URL="<Supabase project URL>"
NEXT_PUBLIC_SUPABASE_ANON_KEY="<Supabase anon key>"
NEXT_PUBLIC_PLATFORM_URL="localhost:8000 or deployed backend URL"
```

Now, clone [multionchat-platform](https://github.com/justinsunyt/multionchat-platform) and run the FastAPI development server.

Install required packages:
```bash
pnpm install
```

Finally, run the Next.js development server:

```bash
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## What's next?

- Llama tool calling to activate agent whenever appropriate
- Refine image prompt recursively with Llama
- Pause button to interrupt agent and prompt new command
- Chat selection menu to choose between any combination of LLMs and VLMs
- Deploy! (You will have to use your own API keys)

## Credits

Special thanks to [MultiOn](https://www.multion.ai/) for the epic agent package and [auroregmbt](https://community.spline.design/file/3ff7b617-2fe9-46c7-8e06-b6d7c382f4db) for the Spline animation!