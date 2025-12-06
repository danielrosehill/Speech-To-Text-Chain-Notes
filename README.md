# The Speech-To-Text Chain

Notes documenting the various components that affect accuracy in ASR (Automatic Speech Recognition) workflows.

The key insight: **ultimate transcription accuracy is not simply achieved by using a bigger and better model**. Rather, it requires viewing all components in the chain as integral to the process. Each link can be optimised, and weaknesses in any one can limit the effectiveness of the others.

## The Chain

```mermaid
flowchart LR
    A[1. Speaker] --> B[2. Noise Environment]
    B --> C[3. Microphone]
    C --> D[4. Audio Processing]
    D --> E[5. ASR Model]
    E --> F[6. Punctuation Restoration]
    F --> G[7. Post-Processing]

    style A fill:#e1f5fe
    style B fill:#e1f5fe
    style C fill:#fff3e0
    style D fill:#fff3e0
    style E fill:#e8f5e9
    style F fill:#e8f5e9
    style G fill:#e8f5e9
```

## Chain Components

| Step | Component | Type | Description |
|------|-----------|------|-------------|
| 1 | [The Speaker](the-chain/the-speaker.md) | Human | Clarity of speech and pronunciation |
| 2 | [The Noise Environment](the-chain/the-noise-environment.md) | Environmental | Background noise, competing audio sources |
| 3 | [The Microphone](the-chain/the-microphone.md) | Hardware | Microphone type, positioning, gain settings |
| 4 | [Audio Processing](the-chain/audio-processing.md) | Software | Noise reduction, audio enhancement |
| 5 | [The ASR Model](the-chain/asr-model.md) | AI/ML | Speech-to-text model selection and configuration |
| 6 | [Punctuation Restoration](the-chain/puncutation.md) | AI/ML | Adding punctuation, VAD, diarisation |
| 7 | [Post-Processing](the-chain/postprocessing.md) | AI/ML | LLM cleanup, formatting, filler removal |

## Component Categories

- **Human/Environmental** (blue): Factors relating to the speaker and their surroundings
- **Hardware/Signal** (orange): Physical capture and signal processing
- **AI/ML Processing** (green): Model-based transcription and refinement
