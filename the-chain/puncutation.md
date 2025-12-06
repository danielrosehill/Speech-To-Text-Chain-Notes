# 6: Punctuation Restoration

The difference between automatic speech recognition and speech to text may seem like splitting hairs, but there are some differences between the two.

ASR systems can be thought of as composites of a large speech to text model, as well as a couple of accessory models for adding in additional necessary functionality.

## Hallucination in ASR

Unlike legacy speech technology, ASR models by virtue of their method of operation, can hallucinate. Hallucination in the form of ASR tends to take the form of the model generating meaningless words when presented with a silence in the audio stream for transcription.

As many large ASR models were trained extensively on data from websites like YouTube, the models will commonly fill in blanks in the user's speech with phrases like "thanks for watching!"

## Voice Activity Detection

Voice activity detection is an important part of speech technology for other reasons, but also this one. This model adds the ability to determine when the user is speaking. Significantly, this means that a pipeline involving VAD can eliminate the need for periods of silence to hit the transcription model in the first place.

## Other Specialist Models

Other specialist sideloaded models include turn detection, emotion detection (sometimes embedded in STT), and speaker diarisation.

## Punctuation as a Differentiator

But in the context of pure single-user speech to text transcription, punctuation restoration is an important differentiator between models which inherently lack it and those which either integrate it, or ASR systems which achieve its integration through coupling an ASR model with a smaller specialist model for punctuation.

## Language-Specific Models

Specialist versions of these models exist for different world languages. Modern Hebrew, for example, is written without vowels. A diacritic model can be added alongside a speech to text model if the user needs to convert speech into vowelised Hebrew. Occasionally this practice is used for disambiguation.

## Paragraph Limitations

Smaller punctuation models do not generally consider paragraphs to be a form of punctuation.