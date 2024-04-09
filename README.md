# AidEyeKit-SDK

AidEyeKit is an open-source toolkit that enables app makers to create visual guides within apps. Our goal is to make all apps user-friendly.

## Demo

[![Uploading Phantom.gif…]()](https://github.com/nuyiep/42KL-Transcendence-Learning/assets/53002130/328a9a2c-3a86-4703-9b1f-233f415255a0)


## How it works

AidEyeKit is a toolkit that consists of an SDK and a backend server. The SDK is used to call APIs easily to the backend server. The backend server is used to process images and generate descriptions for the visual guides.

This project uses Puppeteer and OpenAI's GPT-4 Vision together. Puppeteer first opens the app and takes a screenshot. The screenshot is then sent to OpenAI's GPT-4 Vision to decide which elements it should click to achieve the goal. After the click, another screenshot is taken which repeats the process until the AI reaches the desired goal of the visual guide.

<img src="github/FlowChart.png" alt="AidEyeKit Workflow Diagram">

## Building the SDK

To build the SDK, navigate to the `sdk` folder and run the following command:

```sh
bun run build
```

## Testing the SDK

To test the SDK, navigate to the `sdk-tester` folder, and link the original SDK to the tester SDK by running the following command:

```sh
bun run link
```

Then, run the following command to test the SDK:

```sh
bun run test
```

## Running the Backend Server

This server uses OpenAI's GPT-4 Vision API, so you will need to get an API key from OpenAI.

### Setting up the server

Navigate to the `server` folder and setup your `.env` file in the `server` folder. You can use the `.env.example` file as a template.

Paste your OpenAI API key in the `.env` file like this:

```
OPENAI_API_KEY=your_api_key
```

### Running the server

Before running the backend server, install the dependencies by running the following command:

```sh
bun install
```

To run the server in development mode, run the following command:

```sh
bun run start:dev
```

To run the server in production mode, first build the server by running the following command:

```sh
bun run build
```

Then, run the server by running the following command:

```sh
bun run start
```

## Team Members

[@DoughnutsNCookies](https://www.github.com/DoughnutsNCookies)
[@nuyiep](https://www.github.com/nuyiep)
