# Interactive Sound Instrument with Enhanced Randomization and GPU.js Integration

This project expands on the use of **GPU.js** and the **Web Audio API** to create an interactive sound instrument with improved randomization techniques. By integrating custom pseudo-random number generation and real-time user feedback mechanisms, the system dynamically generates music while allowing the user to rate and influence the results.

## Features

- **Custom Random Seed Management:** Uses a linear congruential generator (LCG) for reproducible pseudo-random number generation, with real-time seed adjustments.
- **Interactive User Feedback:** Users can rate the generated audio as "good" or "bad," which dynamically adjusts the random seed for future generations.
- **Dynamic Instrument Creation:** Instruments produce unique waveforms and sound properties.
- **Melody Generation:** A randomized melody generator based on musical scales and configurable patterns.
- **Real-Time Audio Synthesis:** Audio is computed in real-time using the Web Audio API.
- **GPU Acceleration:** GPU.js is employed for efficient waveform computations and advanced audio processing.
- **Visualization:** Real-time visualization of generated waveforms and musical scales.

---

## How It Works

### Core Components

1. **Random Seed Management:**
   - Implements a custom LCG for reproducible pseudo-random number generation.
   - Allows dynamic adjustment of the seed based on user feedback ("good" or "bad" ratings).

2. **Instrument Class:**
   - Generates sound waves using custom wave functions.
   - Visualizes waveforms on HTML canvas elements.

3. **Melody Class:**
   - Uses a scale to randomly generate musical notes.
   - Produces dynamic melodies by varying note selection and volume.

4. **Web Audio API Integration:**
   - Uses `AudioContext` to generate, buffer, and play audio.
   - Supports multi-channel (stereo) audio playback.

5. **GPU.js Acceleration:**
   - Provides fast, GPU-accelerated waveform computation.
   - Functions like `waveGPU` and `bongoGPU` compute complex audio data.

6. **User Interface:**
   - HTML elements for interaction, such as starting/stopping playback and rating generated audio.
   - Canvas elements for waveform and scale visualization.

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
4. Observe and interact with the waveform and scale visualizations in real-time.
5. Click **"Next please"** to stop the current playback and generate new audio.
6. Rate the audio as "GOOD" or "bad" to influence future audio generation.

### Key Features in Action

- **Instrument Rendering:**
  Each instrument has its unique wave function, which determines its sound characteristics. Three instruments are included:
  - **Accompaniment Instrument** (`cv1`): Adds background harmony.
  - **Main Instrument** (`cv11`): Plays the melody.
  - **Percussion Instrument** (`cv111`): Simulates rhythmic beats.

- **Randomized Scales:**
  A random scale is generated each time using intervals. The scale defines the melody's pitch and tonality.

- **Seed Dynamics:**
  - Initial seed is displayed and updated based on user feedback.
  - "Goods" and "Bads" lists influence seed adjustment.

---

## Code Structure

### Key Functions

- **`rand(n):`** Generates a random integer up to `n`.
- **`shuffle(xs):`** Shuffles an array.
- **`nextseed:`** Dynamically adjusts the seed based on the "Goods" and "Bads" lists.
- **`Instrument.render:`** Computes the audio buffer for an instrument.
- **`Melody.play:`** Plays a note sequence by rendering it into the audio buffer.
- **`waveGPU:`** GPU-accelerated computation of waveforms.
- **`bongoGPU:`** GPU-accelerated computation of percussion-like sounds.
- **`normalize:`** Normalizes audio data to fit the -1 to 1 range.

### Main Workflow

1. **Initialization:**
   - Create `AudioContext` and define audio parameters like sample rate and duration.
   - Initialize the custom random seed.
2. **Scale Generation:**
   - Generate a random musical scale.
3. **Audio Buffer Creation:**
   - Create and fill audio buffers with data rendered by `Instrument` and `Melody` objects.
4. **Playback:**
   - Use an `AudioBufferSourceNode` to play the generated audio.
5. **Feedback Integration:**
   - Collect user feedback ("GOOD" or "bad") to influence future seed values.

---

## Customization

1. **Adding New Instruments:**
   - Extend the `Instrument` class with new wave functions or sound characteristics.
2. **Adjusting Melodies:**
   - Modify the `Melody` class to include additional variations or rhythmic patterns.
3. **Enhancing Visualizations:**
   - Update the canvas rendering logic to display more complex visual effects.
4. **Tuning Randomization:**
   - Adjust the LCG constants or feedback influence logic for different randomization behaviors.

---

## Requirements

- A modern web browser with support for the Web Audio API and WebGL.
- JavaScript enabled.

---

## Future Enhancements

- Add user controls for changing tempo, scale, and instrument parameters.
- Implement more visual effects for better audio visualization.
- Expand the "Goods" and "Bads" influence logic for more nuanced adjustments.

---

## License

This project is licensed under the MIT License.

---

## Author

Developed by [Your Name]. For questions or feedback, please reach out to [your email/contact information].

