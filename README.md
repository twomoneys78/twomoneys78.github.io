# Interactive Sound Instrument with GPU.js and Web Audio API

This project is a web-based application that generates interactive and dynamic audio using the **Web Audio API** and **GPU.js**. It features real-time sound synthesis, melodies, and rhythmic components that can be controlled and visualized in the browser.

## Features

- **Dynamic Instrument Creation:** Instruments can generate unique waveforms and sound properties.
- **Melody Generation:** A randomized melody generator based on scales and configurable patterns.
- **Real-Time Audio Synthesis:** Audio is computed in real-time using the Web Audio API.
- **GPU Acceleration:** GPU.js is used to optimize waveform computations and enable complex audio processing.
- **Interactive Controls:** Choose the duration of the generated audio and interact with the playback.
- **Visualization:** Real-time visual representation of the generated waveforms.

---

## How It Works

### Core Components

1. **Instrument Class:**
   - Generates sound waves using custom wave functions.
   - Distributes stereo sound with randomized channel volumes.
   - Visualizes waveforms on HTML canvas elements.

2. **Melody Class:**
   - Uses a scale to randomly generate musical notes.
   - Produces dynamic melodies by varying note selection and volume.

3. **Web Audio API Integration:**
   - Uses `AudioContext` to generate, buffer, and play audio.
   - Supports multi-channel (stereo) audio playback.

4. **GPU.js Acceleration:**
   - Provides fast, GPU-accelerated waveform computation.
   - Functions like `waveGPU` and `bongoGPU` compute complex audio data.

5. **User Interface:**
   - HTML elements allow user interaction, such as starting/stopping playback and selecting audio duration.
   - Canvas elements visualize the generated waveforms.

---

## Installation and Setup

1. Clone or download this repository.
2. Open the `index.html` file in any modern web browser (Chrome or Firefox recommended).

### Dependencies
- **GPU.js:** A JavaScript library for GPU-accelerated computations. The `gpu-browser.min.js` file must be included in the project.
- **Web Audio API:** Built into modern browsers. No additional setup is required.

---

## Usage

1. Open `index.html` in your browser.
2. Click the **"Sound"** button to generate and play a new audio sequence.
3. Use the dropdown menu to select the duration of the sound in seconds.
4. Waveforms and scales will be visualized in the respective canvas elements.
5. Click **"Next please"** to stop the current playback and generate new audio.

### Key Features in Action

- **Instrument Rendering:**
  Each instrument has its unique wave function, which determines its sound characteristics. Three instruments are included:
  - **Accompaniment Instrument** (`cv1`): Adds background harmony.
  - **Main Instrument** (`cv11`): Plays the melody.
  - **Percussion Instrument** (`cv111`): Simulates rhythmic beats.

- **Randomized Scales:**
  A random scale is generated each time using intervals. The scale defines the melody's pitch and tonality.

- **Visualization:**
  Each instrument's waveform is drawn on a canvas for visual feedback.

---

## Code Structure

### Key Functions

- **`rand(n):`** Generates a random integer up to `n`.
- **`shuffle(xs):`** Shuffles an array.
- **`Instrument.render:`** Computes the audio buffer for an instrument.
- **`Melody.play:`** Plays a note sequence by rendering it into the audio buffer.
- **`waveGPU:`** GPU-accelerated computation of waveforms.
- **`bongoGPU:`** GPU-accelerated computation of percussion-like sounds.
- **`normalize:`** Normalizes audio data to fit the -1 to 1 range.

### Main Workflow

1. **Initialization:**
   - Create `AudioContext` and define audio parameters like sample rate and duration.
2. **Scale Generation:**
   - Generate a random musical scale.
3. **Audio Buffer Creation:**
   - Create and fill audio buffers with data rendered by `Instrument` and `Melody` objects.
4. **Playback:**
   - Use an `AudioBufferSourceNode` to play the generated audio.

---

## Customization

1. **Adding New Instruments:**
   - Extend the `Instrument` class with new wave functions or sound characteristics.
2. **Adjusting Melodies:**
   - Modify the `Melody` class to include additional variations or rhythmic patterns.
3. **Changing Visualizations:**
   - Update the canvas rendering logic to display more complex visual effects.

---

## Requirements

- A modern web browser with support for the Web Audio API and WebGL.
- JavaScript enabled.

---

## Future Enhancements

- Add user controls for changing tempo, scale, and instrument parameters.
- Implement more visual effects for better audio visualization.
- Extend percussion sounds with additional wave functions.

---

## License

This project is licensed under the MIT License.

---

## Author

Developed by [Your Name]. For questions or feedback, please reach out to [your email/contact information].

