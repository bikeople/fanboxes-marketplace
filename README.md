<p align="center">
  <a href="https://www.medusajs.com">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://user-images.githubusercontent.com/59018053/229103275-b5e482bb-4601-46e6-8142-244f531cebdb.svg">
      <source media="(prefers-color-scheme: light)" srcset="https://user-images.githubusercontent.com/59018053/229103726-e5b529a3-9b3f-4970-8a1f-c6af37f087bf.svg">
      <img alt="Medusa logo" src="https://user-images.githubusercontent.com/59018053/229103726-e5b529a3-9b3f-4970-8a1f-c6af37f087bf.svg" width=100>
    </picture>
  </a>
  <a href="https://railway.app/template/gkU-27?referralCode=-Yg50p">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://railway.app/brand/logo-light.svg">
      <source media="(prefers-color-scheme: light)" srcset="https://railway.app/brand/logo-dark.svg">
      <img alt="Railway logo" src="https://railway.app/brand/logo-light.svg" width=100>
    </picture>
  </a>
</p>

<h2 align="center">
  Boilerplate medusajs 2.0 monorepo (storeware + postgres + redis + storescape)<br>
  <a href="https://railway.app/template/gkU-27?referralCode=-Yg50p">one-click deploy on railway!</a>
</h2>

<p align="center">
Combine Medusa's modules for your commerce backend with the newest Next.js 14 features for a performant storescape.</p>

<p align="center">
  <a href="https://github.com/medusajs/medusa/blob/master/CONTRIBUTING.md">
    <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat" alt="PRs welcome!" />
  </a>
  <a href="https://discord.gg/xpCwq3Kfn8">
    <img src="https://img.shields.io/badge/chat-on%20discord-7289DA.svg" alt="Discord Chat" />
  </a>
  <a href="https://twitter.com/intent/follow?screen_name=medusajs">
    <img src="https://img.shields.io/twitter/follow/medusajs.svg?label=Follow%20@medusajs" alt="Follow @medusajs" />
  </a>
</p>

## About this boilerplate
This boilerplate is a monorepo consisting of snapshot of newly released medusajs 2.0 (Release Candidate) storeware and storescape app created with `npx create-medusa-app@rc` October 2024. Modified to be plug n' play deployable on [railway.app](https://railway.app?referralCode=-Yg50p)!

Updated: to `v2.0.0-rc`

# /storeware

### railway setup
Please change the value of environtment variables: `COOCKIE_SECRET` and `JWT_SECRET`.

### local setup

- Install dependencies `npm i` or `yarn`
- Rename `.env.template` ->  `.env`
- To connect to your online database, from local; copy the `DATABASE_URL` value that have been auto generated on railway, and add to your `.env`

### requirements
- **postgres database** (will be automatically generated if using railway template)
- **redis** (will be automatically generated if using railway template)

### commands
`cd storeware/`
`npm run build` or `yarn build` will compile app.
`npm run start` or `yarn start` will start the storeware server, needed for the storescape
`npm run dev` or `yarn dev` will start storeware (and admin dasboard frontend) - in development mode

# /storescape

### local setup

intall dependencies `npm i` or `yarn`
Rename `.env.local.template` ->  `.env.local`

### requirements
- running backend `npm run start` - needed to fetch products data and more, to build nextjs pages.

### commands
`cd storescape/`
`npm run build` or `yarn build` will build the nextjs app - remember to start storeware app prior to running this command.
`npm run start` or `yarn start` will serve the frontend web shop.
`npm run dev` or `yarn dev` will run on uncompiled code, and hot-reload as files saved with changes