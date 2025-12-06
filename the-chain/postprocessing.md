# 7: Post-Processing

The purpose of a speech to text model is generally assumed to be accurately reproducing the user's speech.

However, users generally do not want a perfect version of their spoken words to be transcribed.

## Filler Word Removal

For example, it is almost impossible for users transcribing ordinary spontaneous speech to avoid using filler words like "umm" (etc).

The inclusion of these words generally offers no value to the transcript, and indeed makes the transcript look amateurish.

## LLM Integration

A minimum level of post-processing can be undertaken by adding a large language model onto the voice processing chain.

## Punctuation Restoration Or LLM?

There is a slight duplication or potential duplication of resources between punctuation restoration and large language models. In this respect, they may be considered to be alternative approaches in an ASR chain. 

For example, a large language model is perfectly capable of inferring punctuation, and indeed a modern LLM, especially a quantized one, may do this just as quickly and efficiently and better than a specialist punctuation restoration model. 

Given that this LLM can also do something that the punctuation restoration model can't - make just about any alteration to the text - It's often unclear what the point of implementing this is when there is a better alternative.

## Post-processing levels

From personal experience, writing post processing prompts is less science and more art. 

There is almost an infinite variety of specific instructions that can be added to a large language model to enhance the clarity and intelligibility of text accurately transcribed by STT. 

A bare minimum prompt can instruct the model to remove the aforementioned filler words. 

More ambitiously, these prompts can attempt to leverage the innate reasoning of the models by asking them that if they can infer any words in the transcript which were obviously unintended, that these should be remediated in the edit. 

I commonly use a ridiculous example like: "If the transcript contains I drunk Coca Bola with some ice" then you would rewrite this to "I drunk Coca Cola with some ice."

The intent in wording the example this way is to instruct the LLM that if the surrounding context makes obvious that one word were mistranscribed, that it can be safely remediated. That's why I added the verb "drunk" and "ice" to the above example, so that the model would have little reason to doubt that "Coca Cola" were mistranscribed. 

As is often the case in working with large language models, the addition of one example significantly improves accuracy, with diminishing returns thereafter. 

## Punctuation And Headings

Depending on what the user is transcribing, two other elements of formatted text are commonly desired.

The first of these is paragraph spacing. I always find it surprising that punctuation restoration models do not add paragraph spacing.

An STT model with punctuation restoration, but without any other processing chain, will simply return all text as one continual block, even if the text is a 90-minute-long transcript.

In order for the user to render this text intelligible, manual editing is therefore required.

## Tone, Person, Format

I think it's helpful to consider a dividing line between the aforementioned forms of post-processing, which I would regard as really essential basic edits conducted easily and quickly by large language model, or in the case of a multimodal audio model by the model itself, in order to make transcribed text intelligible and make it closer towards a desired format, and between the wider and larger range of formatting edits that can be added on top of that.

A basic set of post-processing instructions is intended to take the "raw STT output" stage out of the chain—discarding that as intermediate data (for compliance it may be retained but not exposed to the user).

In the case of practical applications for STT, this doesn't mean that the text produced is always ready to be "used"—but it does make a significant difference in its readiness.

The next form of edits that are commonly seen in post-processing applications is editing the text into common formats to match intended delivery targets.

This bank of textual edits is extremely wide and can include matching for business levels of formality versus personal level for interpersonal correspondence.

It can also include taking a text spoken by the user and returning it not in text at all, but in a pseudocode representation or in code itself like in a JSON array for data.