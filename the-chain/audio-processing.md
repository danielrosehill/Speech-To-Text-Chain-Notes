# 4: Audio Processing

One determinant of the accuracy of ASR that is absent in many uses is audio processing technologies.

Audio processing can be integrated at several stages of the STT "journey":

## On-Device Real-Time Processing

Real-time audio processing on device processes the input audio in real time and applies optimizations intended to improve accuracy. For example: background noise removal running on an Ubuntu computer (DeepFilterNet).

## Edge Device Processing

On device, real-time processing can also take place on edge devices like smartphones. However, on consumer devices like Android smartphones, this is challenged greatly by security restrictions around access to the audio stream.

## Embedded Processing

Another form of audio processing is embedded in hardware. This involves implementing audio processing in embedded systems within microphones such as Bluetooth headsets. The disadvantage of this form of real-time processing compared to that running on more powerful processing power is precisely that.

## Server-Side Processing

Audio processing can also be built into server-side systems for ASR such as cloud ASR models. For example, the user's raw audio input can be run through a clarification pipeline before being passed to the ASR model itself. This may be implemented dynamically in transcription workflows in which audio is chunked and streamed or asynchronously as in the case of long-form recordings.

## Local ASR Pipeline Processing

Audio processing workflows can be implemented in local ASR transcription setups such as running Whisper locally. This can be implemented through real-time input processing or within the ASR chain—eliminating the need for the user to run always-on input processing for microphone streams.