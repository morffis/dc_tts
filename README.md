# A TensorFlow Implementation of DC-TTS: yet another text-to-speech model

This project was all about understading the technologies and algorithms of the original author Kyubyong[https://github.com/Kyubyong/dc_tts].

I've tried to adapt the original project that uses a female english (british) dataset in order to replicate the voices of Nick Kate Winslet's Audiobook to a replicate of a male portuguese dataset of president Jair Bolsonaro.

I've split this task in two main goals:

## Get the labeled dataset

I've only used one source of audio of Mr Jair Bolsonaro to train the model, that is contained in this video: https://www.youtube.com/watch?v=7OfUQd45ETw

I had to create a script that splits the audio in "silent periods" and then manually transcribed each prompt until the end.

## Adapt the original training algorithm

Since the original work is fully based on the English language, I had to adapt special characters such as [ç,é,á,ã,í, etc.] in my dataset to be compatible with the algorithm. My hope was that the model would be able to abstract the correct pronunciation even if the orthography wasn’t correct. The results are quite satisfying!

