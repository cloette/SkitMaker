# SkitMaker

An RPG-style skit maker app built on React Native, enabling users to make short skits and export them as videos for use on social media platforms.


### 2.2 Running

Run the backend first, then the frontend.

In `./server`:

```
npm run start || yarn start || 
npm run dev || yarn dev 
```

`dev` uses nodemon, allowing automatic recompiling on saved changes. `start` should be used in production. 


In `./client`:

```
npm run start || yarn start || exp start
```

Opens the expo client to run the React-Native app on mobile emulator.


```
npm run web || yarn web
```

Runs the React app on web browser.

### 2.3 Building

For build instructions for the client, please see [Expo documentation](https://docs.expo.io/versions/latest/distribution/building-standalone-apps/) for building. This project uses Expo SDK 33. 

Options include:
* `expo build:android` 
* `expo build:ios`
* `expo build:web`


## 3 | Structure

### 3.1 Ports

The back-end will be running in localhost:4000, while the front-end will be opened by the expo cli.

### 3.2 Requesting Data

To run the app on Expo for mobile, no proxy is used. Instead, the port is
written in the `fetch` requests

```
fetch('http://localhost:4000/users')
```

### 3.3 Server API

Backend Express REST API routes are found in `.server/routes/`. To add a new page, configure it in `.server/app.js`, similar to current pages.