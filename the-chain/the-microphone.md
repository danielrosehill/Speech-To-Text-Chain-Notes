# 3: The Microphone

The quality of the voice data that the user provides is a function of the microphone that they use to record the voice recording in, even if the digital recording will ultimately be downsampled before being processed by the ASR.

## Microphone Types

A wide variety of microphones exist, ranging from those intended specifically for voice recording to internal microphones on smartphones.

## Wired vs Wireless

Microphones may be wired or wireless. Within wireless microphones, the connectivity may include Bluetooth or devices with special dongles. The latter generally offer better wireless transmission.

## Codec and RF Considerations

Performance of wireless microphones is also influenced by the codec used. And in rare cases, exceptionally cluttered RF space may degrade audio fidelity.

## Address Pattern and Positioning

Even a high-quality microphone can produce suboptimal results if not properly addressed. Microphones have different polar patterns (cardioid, omnidirectional, figure-8, etc.) that determine how they capture sound from different directions. Speaking off-axis or at the wrong distance from a cardioid microphone, for example, can significantly degrade audio quality and subsequently affect ASR accuracy.

## OS-Level Microphone Settings

The operating system's audio configuration represents another link in the chain. Gain settings, sample rate, and input processing can all affect the quality of audio reaching the ASR system. Setting gain too low results in quiet recordings that may fall below the noise floor; setting it too high introduces clipping and distortion. System-level noise suppression or audio enhancements may help or hinder depending on the ASR model's expectations.