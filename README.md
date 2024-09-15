# Advanced Organ Composition with Markov Chains

[Live Demo - Advanced Organ Composition with Markov Chains](https://tylermaginnis.github.io/JS_MarkovChainStrategyOrgan/)

## Table of Contents
1. [Overview](#overview)
2. [Features](#features)
3. [How to Use](#how-to-use)
4. [Techniques and Strategies](#techniques-and-strategies)
   - [Chord Strategies](#chord-strategies)
   - [Melody Strategies](#melody-strategies)
   - [Rhythm Patterns](#rhythm-patterns)
5. [Computer Science Techniques](#computer-science-techniques)
6. [Music Theory Techniques](#music-theory-techniques)

## Overview

This project demonstrates an advanced organ composition system using Markov Chains. The system allows users to generate and manipulate organ music through various controls and strategies. The composition is driven by Markov Chains to determine the next chord and melody strategies, creating a dynamic and evolving musical piece.

## Features

- **Tempo Control**: Adjust the tempo of the composition between 60 and 180 BPM.
- **Volume Control**: Control the master volume, chord volume, and melody volume independently.
- **Reverb Control**: Adjust the intensity of the reverb effect.
- **Waveform Selection**: Choose different waveforms for chords and melody (Sine, Triangle, Sawtooth, Square).
- **Mute Controls**: Mute or unmute chords and melody separately.
- **Visual Feedback**: Display the current chord, melody, and strategies being used.
- **Console Logs**: View detailed logs of the composition process, including rhythm patterns and frequency information.

## How to Use

1. **Open the Live Demo**: Click on the [Live Demo](https://your-live-demo-link.com) link to open the application in your browser.
2. **Adjust Controls**: Use the sliders and dropdowns to adjust the tempo, volume, reverb intensity, and waveforms.
   - **Tempo**: Move the slider to set the tempo (BPM).
   - **Master Volume**: Adjust the overall volume of the composition.
   - **Chord Volume**: Adjust the volume of the chords.
   - **Melody Volume**: Adjust the volume of the melody.
   - **Reverb Intensity**: Adjust the intensity of the reverb effect.
   - **Chord Waveform**: Select the waveform for the chords.
   - **Melody Waveform**: Select the waveform for the melody.
3. **Mute/Unmute**: Click the "Mute Chords" or "Mute Melody" buttons to mute or unmute the respective parts.
4. **Play/Stop**: Click the "Play" button to start the composition. Click the "Stop" button to stop the composition.
5. **Visual Feedback**: Observe the current chord, melody, and strategies in the visual feedback section.
6. **Console Logs**: View detailed logs in the console section to see the rhythm patterns, frequencies, and other information.

## Techniques and Strategies

### Chord Strategies

The system uses various chord strategies within the key of C Major. These strategies are determined by a Markov Chain, which transitions between different chord types based on predefined probabilities.

- **Tonic**: C major 7
- **Dominant**: G major 7
- **Subdominant**: F major 7
- **Minor**: D minor 7
- **Diminished**: B diminished 7
- **Suspended**: C suspended
- **Minor7**: D minor 7
- **Augmented**: C augmented

### Melody Strategies

The melody is generated using different strategies, also determined by a Markov Chain. Each strategy produces a unique melodic pattern.

- **Stepwise**: Generates a melody that moves in small steps.
- **Leap**: Generates a melody with larger intervals.
- **Motif**: Repeats a short melodic motif.
- **Arpeggio**: Uses arpeggios to create the melody.
- **Pentatonic**: Uses the pentatonic scale.
- **Blues**: Uses the blues scale.
- **Chord Tones**: Prioritizes chord tones in the melody.
- **Ascending Run**: Creates an ascending melodic run.
- **Descending Run**: Creates a descending melodic run.
- **Random Walk**: Generates a random walk through the scale.

### Rhythm Patterns

The rhythm of the melody is determined by predefined patterns, which are randomly selected for each iteration.

- **Pattern 1**: [1, 0.5, 0.5, 1, 0.5, 0.5, 1]
- **Pattern 2**: [1, 1, 0.5, 0.5, 1, 1, 1]
- **Pattern 3**: [0.5, 0.5, 0.5, 0.5, 1, 1]
- **Pattern 4**: [1, 0.25, 0.25, 1, 0.5, 0.5, 1]
- **Pattern 5**: [0.25, 0.25, 0.5, 0.5, 1, 1, 1]
- **Pattern 6**: [1, 1, 1, 1, 0.5, 0.5, 0.5, 0.5] (Triplets)

## Computer Science Techniques

### Markov Chains

Markov Chains are used to determine the next chord and melody strategies. A Markov Chain is a stochastic model that describes a sequence of possible events where the probability of each event depends only on the state attained in the previous event. In this project, Markov Chains are used to transition between different chord and melody strategies based on predefined probabilities.

### Event Scheduling

The composition uses an event scheduling system to manage the timing of notes. The `scheduler` function ensures that notes are played at the correct time by scheduling events ahead of time and using a lookahead interval to keep the timing accurate.

### Audio Synthesis

The project uses the Web Audio API to generate and manipulate sound. Oscillators are created for each note, and various audio nodes (e.g., gain nodes, filters, panners) are used to shape the sound. The `createOrganOscillator` function is responsible for creating a rich organ sound by layering oscillators and applying filters and effects.

### User Interaction

Event listeners are used to handle user interactions with the controls. For example, sliders and buttons are used to adjust the tempo, volume, and other parameters. The `addEventListener` method is used to attach event handlers to the DOM elements.

## Music Theory Techniques

### Chord Progressions

The project uses various chord progressions within the key of C Major. Chord progressions are sequences of chords that are used to create harmony in music. The system transitions between different chord types (e.g., tonic, dominant, subdominant) based on the probabilities defined in the Markov Chain.

### Melody Generation

Melodies are generated using different strategies that define how the notes are selected and arranged. For example, the stepwise strategy generates melodies that move in small steps, while the leap strategy generates melodies with larger intervals. The melody strategies are designed to create interesting and varied melodic patterns.

### Scales

The project uses different scales to generate melodies. For example, the pentatonic scale and the blues scale are used in some of the melody strategies. Scales are sequences of notes that are used as the basis for melodies and harmonies in music.

### Rhythm Patterns

Rhythm patterns define the timing and duration of notes in the melody. The project uses predefined rhythm patterns that are randomly selected for each iteration. Rhythm patterns add variety and interest to the composition by varying the timing and duration of notes.

## Conclusion

This project demonstrates the use of Markov Chains and the Web Audio API to create an advanced organ composition system. By combining computer science techniques with music theory, the system generates dynamic and evolving musical pieces that can be controlled and manipulated by the user. Explore the live demo to experience the full capabilities of the system.