# Browser Guitar Tuner

A free, browser-based guitar tuner built with HTML, CSS, JavaScript, and the Web Audio API. The tuner uses your device’s microphone to detect the frequency of a played string and displays the nearest musical note, frequency, and tuning offset in cents.

The application runs entirely in the browser and can be hosted for free using GitHub Pages.

## Features

- Real-time microphone input
- Automatic pitch and note detection
- Sharp and flat tuning indicator
- Cents-based tuning meter
- Adjustable A4 reference pitch
- Support for standard guitar tuning:
  - E2
  - A2
  - D3
  - G3
  - B3
  - E4
- Responsive interface for desktop and mobile browsers
- No account or installation required
- No microphone recordings are stored or uploaded

## Live Demo

```text
https://YOUR-USERNAME.github.io/guitar-tuner/
```

Replace `YOUR-USERNAME` with your GitHub username after enabling GitHub Pages.

## How to Use

1. Open the tuner in a supported browser.
2. Press **Start Tuner**.
3. Allow the browser to access your microphone.
4. Play one guitar string at a time.
5. Use the tuning indicator:
   - **Tune up** means the string is flat.
   - **Tune down** means the string is sharp.
   - **In tune** means the detected pitch is within the acceptable range.
6. Press **Stop** when finished.

For the best results:

- Tune in a quiet environment.
- Hold the guitar close to the microphone.
- Play one string at a time.
- Allow the note to ring clearly.
- Use a recent version of Chrome, Edge, Firefox, or Safari.

## Standard Guitar Tuning

| String | Note | Approximate Frequency |
|---|---:|---:|
| 6th, lowest | E2 | 82.41 Hz |
| 5th | A2 | 110.00 Hz |
| 4th | D3 | 146.83 Hz |
| 3rd | G3 | 196.00 Hz |
| 2nd | B3 | 246.94 Hz |
| 1st, highest | E4 | 329.63 Hz |

Frequencies assume an A4 reference pitch of 440 Hz.

## Technology

- HTML5
- CSS
- JavaScript
- Web Audio API
- `navigator.mediaDevices.getUserMedia()`
- Client-side pitch detection

The microphone stream is analyzed locally using browser JavaScript. A backend server is not required.

## Privacy

Microphone audio is processed locally in the browser.

This application does not:

- Record microphone audio
- Upload audio to a server
- Store audio files
- Require a user account
- Send pitch information to a third party

The browser will request microphone permission before the tuner starts.

## Browser Requirements

The tuner requires:

- A microphone
- JavaScript enabled
- A browser that supports the Web Audio API
- A secure HTTPS connection

GitHub Pages automatically provides HTTPS.

Microphone behavior may vary between browsers and devices. On mobile devices, microphone access must normally be started through a button press or another user action.

## Run Locally

Because microphone access requires a secure context, opening `index.html` directly may not work in every browser.

Run the project through a local development server instead.

Using Python:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

Using Node.js:

```bash
npx serve .
```

`localhost` is treated as a secure context by modern browsers.

## Deploy with GitHub Pages

1. Create a GitHub repository.
2. Add the project files, including `index.html`.
3. Push the files to the `main` branch.
4. Open the repository’s **Settings**.
5. Select **Pages**.
6. Under **Build and deployment**, choose:
   - **Source:** Deploy from a branch
   - **Branch:** `main`
   - **Folder:** `/ (root)`
7. Save the settings.
8. Wait for GitHub to publish the site.

The application will be available at:

```text
https://YOUR-USERNAME.github.io/REPOSITORY-NAME/
```

## Project Structure

```text
guitar-tuner/
├── index.html
└── README.md
```

The proof of concept can be contained entirely in `index.html`. The CSS and JavaScript may also be separated into dedicated files as the project grows:

```text
guitar-tuner/
├── index.html
├── styles.css
├── tuner.js
└── README.md
```

## Limitations

- Background noise can interfere with pitch detection.
- Built-in phone and laptop microphones vary in quality.
- Guitar harmonics may occasionally cause octave detection errors.
- Microphone permission must be granted by the user.
- Some older or embedded browsers may not support the required APIs.

## Future Improvements

Possible enhancements include:

- Alternate tunings
- Chromatic tuning mode
- Bass guitar support
- Selectable target strings
- Improved noise filtering
- Frequency history visualization
- Configurable tuning sensitivity
- Progressive Web App support
- Offline installation
- Accessibility improvements

## Contributing

Contributions, bug reports, and feature suggestions are welcome. Fork the repository, create a feature branch, and submit a pull request.

## License

This project is available under the [MIT License](LICENSE).
