# The Speech-To-Text Chain

Notes documenting the various components that affect accuracy in ASR (Automatic Speech Recognition) workflows.

## The Chain

```mermaid
flowchart LR
    A[1. Speaker] --> B[2. Noise Environment]
    B --> C[3. Microphone]
    C --> D[4. Mic Positioning]
    D --> E[5. OS Audio Settings]
    E --> F[6. Audio Processing]
    F --> G[7. ASR Model]
    G --> H[8. Punctuation Restoration]
    H --> I[9. Post-Processing]

    style A fill:#e1f5fe
    style B fill:#e1f5fe
    style C fill:#fff3e0
    style D fill:#fff3e0
    style E fill:#fff3e0
    style F fill:#fff3e0
    style G fill:#e8f5e9
    style H fill:#e8f5e9
    style I fill:#e8f5e9
```

## Chain Components

| Step | Component | Type | Description |
|------|-----------|------|-------------|
| 1 | [The Speaker](the-chain/the-speaker.md) | Human | Clarity of speech and pronunciation |
| 2 | [The Noise Environment](the-chain/the-noise-environment.md) | Environmental | Background noise, competing audio sources |
| 3 | [The Microphone](the-chain/the-microphone.md) | Hardware | Microphone type, wired vs wireless, codec |
| 4 | [Microphone Positioning](the-chain/mic-positioning.md) | Hardware | Polar patterns, address angle, distance |
| 5 | [OS Audio Settings](the-chain/os-audio-settings.md) | Software | Gain, sample rate, system audio processing |
| 6 | [Audio Processing](the-chain/audio-processing.md) | Software | Noise reduction, audio enhancement |
| 7 | [The ASR Model](the-chain/asr-model.md) | AI/ML | Speech-to-text model selection and configuration |
| 8 | [Punctuation Restoration](the-chain/puncutation.md) | AI/ML | Adding punctuation, VAD, diarisation |
| 9 | [Post-Processing](the-chain/postprocessing.md) | AI/ML | LLM cleanup, formatting, filler removal |

## Component Categories

- **Human/Environmental** (blue): Factors relating to the speaker and their surroundings
- **Hardware/Signal** (orange): Physical capture and signal processing
- **AI/ML Processing** (green): Model-based transcription and refinement
