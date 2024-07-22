# Fake Voice Generator :wink:

This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

It makes use of AI generated vocals.

## Preequisite
You're gonna need an API Key for using ElevenLabs’ API. Go ahead and create an account on [ElevenLabs](https://elevenlabs.io/) in order to get access tokens.

You first need to create a custom model on ElevenLabs’ website. After you’ve made an account, click on VoiceLab in the Navbar and then click on “Add Generative or Cloned Voice”.

Now click on Voice Design and feel free to go ham on the options there. Click on Generate Voice and if you’re satisfied with the result, click on use voice. Give it a name, add some labels if you want and then click on Create Voice. This is the voice we'll be using as a clone.

## Getting Started

First, install the required dependencies:
```bash
npm i
#or
yarn i
```

Second, run the development server:
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

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## How it works

1. User enters some text on the frontend they want the voice to "speak".
2. User will select one of the voices from the voices they've created on VoiceLab to use.
3. We'll send the text and their choice of voice to our backend, which will further call the ElevenLabs' API to get a sound recording
4. We get the audio and then display it on the frontend