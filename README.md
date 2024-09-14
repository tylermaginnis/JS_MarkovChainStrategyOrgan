# Infinite Harmonious Organ Composition

[Organ Composition Live Demo](https://tylermaginnis.github.io/JS_MarkovChainStrategyOrgan/) <!-- Replace with actual screenshot URL -->

## Table of Contents

- [Overview](#overview)
- [Technologies Used](#technologies-used)
- [Algorithmic Techniques](#algorithmic-techniques)
  - [Markov Chains](#markov-chains)
  - [Generative Functions](#generative-functions)
- [Musical Theories Implemented](#musical-theories-implemented)
  - [Harmonic Functions](#harmonic-functions)
  - [Melodic Strategies](#melodic-strategies)
- [Scheduler and Timing](#scheduler-and-timing)
- [Oscillator Management](#oscillator-management)
- [Logging and Console Features](#logging-and-console-features)
- [Limitations and Future Enhancements](#limitations-and-future-enhancements)
- [Getting Started](#getting-started)
- [Contributing](#contributing)
- [License](#license)

## Overview

The **Infinite Harmonious Organ Composition** is a web-based application that generates an endless, musically rich organ composition. Leveraging the power of the Web Audio API, Markov chains, and algorithmic generative functions, this project emulates the depth and complexity found in classical organ music, inspired by composers like Rachmaninoff.

## Technologies Used

- **Web Technologies:**
  - **HTML5:** Structure of the web page.
  - **CSS3:** Styling and layout.
  - **JavaScript (ES6):** Core logic for music generation and playback.

- **Web Audio API:**
  - Enables real-time audio synthesis and manipulation directly in the browser.

- **Algorithmic Techniques:**
  - **Markov Chains:** For probabilistic transitions between musical strategies.
  - **Generative Functions:** To dynamically create chords and melodies based on defined musical theories.

## Algorithmic Techniques

### Markov Chains

Markov chains are utilized to introduce variability and probabilistic transitions in the composition. Instead of a fixed sequence, the system can transition between different musical strategies based on predefined probabilities, ensuring that the music evolves organically over time.

- **Chord Strategy Markov Matrix:**
  - Dictates the probability of transitioning from one chord strategy (e.g., tonic) to another (e.g., dominant).
  
- **Melody Strategy Markov Matrix:**
  - Controls the likelihood of switching between different melodic strategies (e.g., stepwise, leap).

### Generative Functions

Generative functions are employed to create chords and melodies dynamically. These functions encapsulate specific musical techniques, ensuring that each generated element adheres to musical coherence and theory.

- **Chord Generators:**
  - Functions that return specific chord structures based on harmonic functions (e.g., tonic, dominant).
  
- **Melody Generators:**
  - Functions that produce melody notes using various strategies like stepwise motion, leaps, motifs, and arpeggios.

## Musical Theories Implemented

### Harmonic Functions

The composition incorporates fundamental harmonic functions to establish tonal centers and progression:

- **Tonic (`tonic`):** The home chord that provides a sense of resolution.
- **Dominant (`dominant`):** Creates tension that resolves back to the tonic.
- **Subdominant (`subdominant`):** Acts as a bridge between tonic and dominant.
- **Minor (`minor`):** Introduces a minor tonality for emotional depth.
- **Diminished (`diminished`):** Adds dissonance and tension, enhancing the harmonic complexity.

Each harmonic function is associated with specific chord structures, contributing to the overall musical narrative.

### Melodic Strategies

To ensure melodic interest and variation, multiple strategies are employed:

- **Stepwise Motion (`stepwise`):**
  - Melodies move predominantly by adjacent scale degrees, creating smooth and coherent lines.
  
- **Leap Motion (`leap`):**
  - Introduces larger intervals between notes, adding variety and excitement.
  
- **Motif (`motif`):**
  - Repeats short sequences of notes, establishing recognizable patterns within the melody.
  
- **Arpeggio (`arpeggio`):**
  - Plays the notes of a chord in succession, aligning the melody closely with the harmony.

These strategies are dynamically selected and combined using Markov chains to produce evolving and engaging melodies.

## Scheduler and Timing

A robust scheduling system ensures that musical events (chords and melodies) are played seamlessly without overlaps or gaps:

- **Scheduler Function:**
  - Continuously checks if new events need to be scheduled ahead of the current playback time.
  
- **Scheduling Parameters:**
  - **Lookahead:** Determines how frequently the scheduler runs (e.g., every 25ms).
  - **Schedule Ahead Time:** Specifies how far into the future events are scheduled (e.g., 0.1 seconds).
  
- **Beat Alignment:**
  - Both chords and melodies are scheduled based on beats per minute (BPM), ensuring synchronized playback.

## Oscillator Management

Effective management of oscillators is crucial for sound synthesis and preventing memory leaks:

- **Organ Oscillators:**
  - Each chord is synthesized using three oscillators representing the fundamental frequency and its harmonics.
  
- **Gain Nodes:**
  - Control the amplitude envelope (ADSR) for smooth note transitions.
  
- **Oscillator Lifecycle:**
  - Oscillators are started and stopped precisely based on the scheduled timing, ensuring clean and continuous playback.

## Logging and Console Features

An on-screen console provides real-time insights into the composition process:

- **Strategy Information:**
  - Logs the current chord and melody strategies being employed.
  
- **Rhythm Patterns:**
  - Displays the rhythm patterns used for each melody segment.
  
- **Event Logging:**
  - Records detailed information about each chord and melody note, including frequencies and timing.
  
- **Chord Limitation:**
  - Implements a counter to limit the number of consecutive chords, preventing excessive repetition and enhancing musical variation.

## Limitations and Future Enhancements

While the current implementation provides a dynamic and evolving composition, there are areas for further improvement:

- **Voice Leading Enhancements:**
  - Implement smoother transitions between chords by minimizing large leaps in individual voice parts.
  
- **Counterpoint and Polyphony:**
  - Introduce multiple melody lines interacting harmoniously, adding depth and complexity.
  
- **Ornamentation:**
  - Add grace notes, trills, and other embellishments to enrich the melody.
  
- **Dynamic Expression:**
  - Incorporate volume modulation (crescendo/decrescendo) and subtle tempo variations for expressiveness.
  
- **Effects and Reverb:**
  - Utilize `ConvolverNode` to simulate acoustic environments, enhancing the organ's richness.
  
- **Expanded Chord and Melody Libraries:**
  - Include additional chords (e.g., secondary dominants) and advanced melodic techniques for greater variety.
  
- **Rhythmic Variation:**
  - Implement polyrhythms and more complex rhythm patterns to further diversify the composition.

## Getting Started

### Prerequisites

- A modern web browser (e.g., Chrome, Firefox) that supports the Web Audio API.

### Installation

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/infinite-organ-composition.git```
