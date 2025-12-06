# 5: The ASR Model

Central to the act of transcribing spoken speech into text is, of course, the role of the ASR model itself.

In addition, the ASR model depends on hardware for inference.

## Stock vs Fine-Tuned Models

The ASR model can be a stock model such as one of the OpenAI Whisper models.

Alternatively, it may be a fine-tune of a stock ASR model.

This practice is somewhat commonplace in situations in which users use specialized vocabulary and accuracy is paramount—consider, for example, medical transcription and emergency dispatch.

## Model Variety

Just like large language models, there is a large variety of ASRs available. Some are optimized specifically for running on edge inference. Others are quantized versions of large models.

## Traditional ASR vs Multimodal Models

Finally, there is a very significant difference in functionality between what can now be regarded as "traditional" speech to text models, used for automatic speech recognition, which were designed and intended exclusively for accurate reproduction of human speech in textual format, and a newer breed of multimodal AI model (for example Gemini 2.5) which can process audio binary data as well as user prompts to provide guidance for the transcription.

While lacking the specialization of the first category, utilising this second form of model for transcription opens up a much wider variety of possibilities.

The user can instruct the model to format the transcript according to specific instructions without needing to layer a large language model onto the pipeline.
