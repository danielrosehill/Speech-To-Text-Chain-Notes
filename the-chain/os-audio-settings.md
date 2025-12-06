# 5: OS Audio Settings

The operating system's audio configuration represents another link in the chain between the physical microphone and audio processing software.

## Gain

Input gain determines how much the microphone signal is amplified:

- **Too low**: Quiet recordings that may fall below the noise floor, forcing later amplification that boosts noise
- **Too high**: Clipping and distortion that cannot be recovered

Optimal gain maximises signal level without clipping, typically targeting peaks around -6dB to -12dB.

## Sample Rate

The sample rate determines the frequency resolution of the recorded audio:

- **16kHz**: Common for telephony and some ASR models
- **44.1kHz**: CD quality, often more than sufficient for speech
- **48kHz**: Video standard, commonly used in professional settings

Many ASR models downsample to 16kHz internally, but recording at higher rates preserves more information for preprocessing.

## System Audio Processing

Operating systems may apply processing to audio inputs:

- **Noise suppression**: Can help or hinder depending on implementation and ASR model expectations
- **Echo cancellation**: Useful for calls but may affect solo recordings
- **Automatic gain control (AGC)**: Can normalise levels but may introduce pumping artifacts

Understanding and controlling these settings ensures predictable audio quality reaching the ASR system.
