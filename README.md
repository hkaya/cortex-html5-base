# cortex-html5-base

A skeleton HTML5 application built for Cortex.

## Build

```
npm install
make dist
```

## Project Setup
The HTML5 application is set up to run in two environments: development and production. You need to rebuild the app to switch
to an environment:
```
make dev # build the app in dev mode.
make build # build the app in prod mode.
```

### Development Mode
The final HTML5 application will be saved under `./build`. The app will start in simulation mode. Open `./build/index.html`
in your browser (tested on Chrome / Chromium) to run the app. In simulation mode, the app will fire Cortex events
periodically and use the test data stored in `./src/test-data.js`. This mode is useful for quickly building the UI.

### Production Mode
Similar to the development mode, the final HTML5 application will be saved under `./build`. However, you can build a final
zip file as well by running `make dist`. **The application will only work on Cortex player.**

### File Structure
- `./html/`: Contains `index.html`. You can put the app skeleton in this file or dynamically create the DOM elements in JavaScript.
- `./css/`: Contains CSS files. You can include the CSS files under this folder by `require`ing them in JavaScript. See `src/main.js` for an example. 
- `./assets/`: All files under this directory will get copied to the final HTML5 app directory. You can place images, fonts and any other resources under this directory.
- `./src/`: Source files. `src/main.js` is the entry point. All source files will get compiled into `./build/bundle.js` by webpack.

## Customizing the App
TODO