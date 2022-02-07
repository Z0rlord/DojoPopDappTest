<!-- language-all: javascript -->

<h1 align="center">
  <img src="https://raw.githubusercontent.com/koii-network/koii.X/main/.github/images/koii_logo.svg" width="224px"/><br/>
  Create Koii Fundraise :fish:
</h1>
<p align="center">
  <img src="https://img.shields.io/badge/TypeScript-007ACC?style=flat&logo=typescript&logoColor=white" alt="typescript" />&nbsp;
   <a href="https://discord.gg/koii" target="_blank"><img src="https://img.shields.io/badge/Discord-7289DA?style=flat&logo=discord&logoColor=white" alt="cli version" /></a>&nbsp;
   <a href="http://koii.network/" target="_blank"> <img src="https://img.shields.io/badge/made%20by-koii-blue" alt="made-by-koii" /></a>&nbsp;
</p>

## ⚡️ Quick start

First of all, run `npx create-koii-fundraise` to create a Koii Fundraise Portal.

After the installation is done head to the installed project and inside it run `yarn start`.

(If the `yarn start` doesn't work, please try `react-scripts --openssl-legacy-provider start`)

## Table of Contents

- [Fundraiser Customization](#fundraiser-customization)
- [Deploy to Arweave](#deploy-to-arweave)
- [App Customization](#app-customization)
- [Environment](#environment)
  - [Node](#node)
  - [Yarn](#yarn)

# Fundraiser Customization

To customize your fundraiser head to [./src/config/funding-config.tsx](./src/components/funding/funding-config.tsx) file in your app, you'll notice a `config` that you can change to match your portal config.

Example:

```javascript
const config = {
  title: "Plagiarism Registry DAO", // Project title
  companyLogo: "https://pbs.twimg.com/profile_images/1424786684194041859/lkDa9l1U_400x400.png", // Logo to appear in the navbar.
  companyName: "Koii Network Creator Studio",
  fundGoal: 1000, // Your funding goal in "eth"
  images: [
    // Images to be placed in the top slider
    { src: "https://picsum.photos/700" },
    { src: "https://picsum.photos/701" },
    { src: "https://picsum.photos/702" },
    { src: "https://picsum.photos/703" },
    { src: "https://picsum.photos/704" },
    { src: "https://picsum.photos/705" }
  ],
  socials: {
    // Your social network links
    website: "https://koii.network",
    twitter: "https://twitter.com/KoiiNetwork",
    discord: "https://discord.com/invite/koii",
    facebook: null,
    github: "https://github.com/koii-network"
  },
  paymentType: "ar", // 'eth' or 'ar' Portal currency "eth" (ethereum) or "ar" (Arweave)
  fundAddress: "_JHZaUrLyOVSf_t87GBASHXziurNqXmxJ0VgYg-rggM", // Your funding address that people will deposit to. (Ethereum or Arweave address, depends on paymentType)
  // A brief description about the project as html.
  about: (
    <div>
      <p>About us</p>
    </div>
  ),

  faqs: [
    // FAQs content
    { question: "Question 1", answer: "Answer 1" },
    { question: "Question 2", answer: "Answer 2" },
    { question: "Question 3", answer: "Answer 3" }
  ]
};
export default config;
```

# Deploy to Arweave

Few simple steps to deploy to your crowdfunding portal to Arweave

# App Customization

Edit the [app-config](./src/config/app-config.ts) file to change the basic details about your app. e.g.

```javascript
const config = {
  lang: "en", // language of your website
  locale: "en_US", // locale of your website
  title: "Koii.X — Your Koii DApp",
  description: "Create Koii DApp",
  canonical: "http://koii-x.vercel.app/", // Your production website link
  twitterHandle: "@KoiiNetwork", // Twitter username
  companyName: "Koii"
};
```

To change the favicon, head to [public](./public) folder and replace the `favicon.svg` with yours.\
To change the logo, head to [assets](./src/assets) folder and replace the `logo.png` with yours.

# Environment

### Node

We recommend installing the latest LTS node version `v16.13.1` to provides stable compatibility with React

- **Node v16.XX** (`node --version`)

**[Or Download Node with NVM](https://github.com/nvm-sh/nvm#usage)**

### Yarn

We install and run our scripts with yarn, as an alternative to npm:

**[Download Yarn](https://yarnpkg.com/lang/en/docs/install/)**
