# Sonified Audio Interface

### Project Description
This simulator visualizes and sonifies data from a discus throw, more specifically to perfect a throwers mid-spin form. This simulator allows for users to interact with various datasets to explore how different parameters affect the sound output. The simulator uses sound synthesis to represent changes in arm acceleration, release angle, foot position, hip rotation, shoulder alignment, and shoulder level.

### Interface Overview:
•	Sliders: Control the variables for arm acceleration, release angle, foot position, hip rotation, shoulder alignment, and shoulder level. These sliders directly affect the sound parameters. 
•	Buttons:
  o	Data Stream 1, 2, 3: Load pre-defined datasets representing different throwing techniques.
  o	Mute: Silences all sound output temporarily.
  o	Play: Resumes sound output using the current slider values.
  o	Reset: Resets all sliders to their midpoint values and silences the sound.
  o	Stop Simulation: Stops any running data stream and resets the interface.
•	Using the Simulator:
  1.	Start the Simulation: Open the Processing sketch and run it. The main window displays sliders for each throw parameter and buttons       to control the simulation.
  2.	Interact with Sliders: Manually adjust the sliders to hear how different values affect the sonification.
  3.	Load Data Streams: Click on "Data Stream 1", "Data Stream 2", or "Data Stream 3" to load pre-defined datasets that automatically         adjust the sliders and modify the sounds according to real-world discus throw data.
  4.	Control Sound Output: Use the "Mute", "Play", and "Stop Simulation" buttons to control the audio playback.
  5.	Reset the System: At any point, click "Reset" to return all sliders to their default positions and stop all sound.

### Detailed Sonification Scheme:
1.	Wave Generation:
  •	Each parameter controls a sine wave generator, with its base frequency set to one of the notes of a major eleventh chord.
  •	The waves are continuously played and modified in real-time based on the slider positions.
2.	Frequency and Gain Control:
  •	Frequency Modulation: The frequency of each sine wave is adjusted by the slider position. Moving the slider away from the center         increases or decreases the frequency, depending on the direction.
  •	Gain Control: The volume (gain) of each wave increases as the slider moves further from the center, making the sound louder as it        deviates more from the midpoint.
3.	Audio Processing:
  •	Low-Pass Filters: Each channel passes through a low-pass filter with a cutoff frequency set to 500 Hz, which smooths the tone by         attenuating higher frequencies.
  •	Panning: Sound from each wave is panned across the stereo field from left to right, with the exact position determined by the            slider's relative position, enhancing the spatial feel of the audio representation.
4.	Integration into Audio Context:
  •	Each processed signal is then combined into a single audio output, ensuring a cohesive auditory experience that dynamically reflects     the changes in discus throw parameters.
5.	Interactivity and Real-time Feedback:
  •	Users interact with the simulation via sliders, each corresponding to one of the discus throw parameters: Arm Acceleration, Release      Angle, Foot Position, Hip Rotation, Shoulder Alignment, and Shoulder Level.
  •	As users adjust these sliders, the changes in the audio output provide immediate feedback, illustrating how variations in throw          mechanics might affect the performance in a real-world scenario.
