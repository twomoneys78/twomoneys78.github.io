# Project: Dynamic Music Tool with GPU.js

## Overview
This project is an interactive application that uses GPU.js and the Web Audio API to generate and play complex audio sequences. The user interface allows for creating scales, rendering instruments, and generating audio in real time.

## Project Structure

- **index.html**: The main code of the application. Contains logic for audio generation, user interaction, and graphical rendering.
- **gpu-browser.min.js**: The GPU.js library for parallel computations.
- **back.webp**: Background image.

## Features

- **Scale Generation:**
  - The project creates random scales that are used for audio playback.
  - These scales can be visualized.

- **Instruments:**
  - The `Instrument` class manages tones and generates waveforms using GPU.js.
  - Three types of instruments are supported (bongo, main melody, and accompaniment).

- **Melodies:**
  - The `Melody` class continuously generates tones based on a randomly generated scale.

- **GPU Acceleration:**
  - Waveform calculations for instruments are parallelized with GPU.js to enhance performance.

- **User Interaction:**
  - Users can start generation, rate songs, and modify instruments.

## Usage

1. **Run the Project:**
   - Ensure all project files (HTML, JS, images) are in the same directory.
   - Open `index.html` in a browser.

2. **Generate Audio:**
   - Click the "Sound" button to start generation.
   - The application creates a new random scale and begins audio playback.

3. **Observe Scales and Instruments:**
   - Visual representations of scales and waveforms are visible in the canvas elements.

## Requirements

- **Browser:** Supports Chrome, Edge, or Firefox with Web Audio API enabled.
- **Files:**
  - `gpu-browser.min.js`
  - `index.html`

## Important Notes

- The code is designed to run on modern browsers. If issues arise, ensure JavaScript is enabled and the GPU.js library is properly included.
- Some features, like rating songs (functions `ratebad` and `rategood`), are currently commented out.

---

If you would like to extend the project or report issues, please create an issue or pull request.

