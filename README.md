# React in Vue — Module Federation Demo

A proof-of-concept that loads a React component from a remote React application and mounts it inside a Vue host application using Webpack Module Federation.

The remote exposes a React button that increments a counter controlled by the Vue host. The demo also lets you change the button label and mount/unmount the component, illustrating cross-framework communication and lifecycle handling.

## Run locally

Requirements: Node.js and Yarn compatible with the project's lockfile.

```bash
yarn install
yarn start
```

The workspace starts two development servers:

- Vue host (`layout`): [http://localhost:3001](http://localhost:3001)
- React remote (`home`): [http://localhost:3002](http://localhost:3002)

## End-to-end tests

The original project documents Cypress commands:

- `npm run cypress:debug` — interactive Cypress runner
- `yarn e2e:ci` — build and run the configured end-to-end suite headlessly

Check the scripts in `package.json` if the commands differ in your current branch.

## What this demonstrates

- Loading a federated remote component inside a different framework
- Passing interaction/state between Vue and React
- Handling component mount/unmount lifecycle

## Limitations

This is a proof-of-concept, not a complete micro-frontend platform. For production, add remote-load failure handling, explicit shared dependency/version policy, deployment versioning, and tests for unavailable remotes.
