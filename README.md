<h1 align="center">
FastVC
</h1>

## Overview

FastVC is a fast and efficient, non-parallel and any-to-any *voice conversion (VC)* tool. VC involves the modification of the voice of a source speaker to make it sound like that of a target speaker, without changing the linguistic content of the sentence. Our tool exploits the task by cascading an Automatic Speech Recognition (ASR) model and a Text To Speech (TTS) model.

<p align="center">
  <img src="https://user-images.githubusercontent.com/17434626/122674111-014c9480-d1d4-11eb-9310-0b50250caeab.png" width="85%"//>
</p>

The ASR is based on [Wav2vec 2.0](https://arxiv.org/pdf/2006.11477.pdf) and is used to transcribe the speech from a source speaker. The TTS is based on [SV2TTS](https://arxiv.org/pdf/1806.04558.pdf) and is used to generate the output speech from a target speaker embedding.

For a more detailed explanation check out [the paper of our project](https://github.com/fmiotello/fastVC/files/6849958/L11_Report.pdf). A demo page is available [here](https://fmiotello.github.io/fastVC).

## Installation & usage

The software was implemented using `python 3.9.4`

1. Clone the repository (`git clone https://github.com/fmiotello/fastVC.git`) and enter the directory (`cd fastVC`)
2. (*optional*) Create virtual env and activate it: `python -m venv env` and `source env/bin/activate` (if using macOS/Linux) or `.\env\Scripts\activate` (if using Windows)
3. Upgrade pip: `python -m pip install --upgrade pip`
4. Install dependencies: `python -m pip install -r requirements.txt`
5. Download the pretrained models ([encoder](https://drive.google.com/file/d/1q8mEGwCkFy23KZsinbuvdKAQLqNKbYf1/view?usp=sharing), [synthesizer](https://drive.google.com/file/d/1EqFMIbvxffxtjiVrtykroF6_mUh-5Z3s/view?usp=sharing), [vocoder](https://drive.google.com/file/d/1cf2NO6FtI0jDuy8AV3Xgn6leO6dHjIgu/view?usp=sharing)) and put them in the correct directories:
  ````
  ./src/encoder/saved_models/pretrained.pt
  ./src/synthesizer/saved_models/pretrained/pretrained.pt
  ./src/vocoder/saved_models/pretrained/pretrained.pt
  ````
6. Run the main script: `python src/main.py` (use `--help` for displaying available options). The output audio will be `./src/audio/audio_out.wav`.

More instructions can be found [here](https://github.com/fmiotello/fastVC/tree/main/src).

## Notes

This application was developed as a project at [Politecnico di Milano](https://www.polimi.it/en/) (MSc in Music and Acoustic Engineering).

*[Luigi Attorresi](https://github.com/LuigiAttorresi)*<br>
*[Federico Miotello](https://github.com/fmiotello)*<br>
*[Eugenio Poliuti](https://github.com/Poliuti)*<br>

Marzieh Ali Atashi is a master's student from South Tehran University

40114140111030 student number

Digital signal processing course

Professor Dr. Mahde Eslami

https://github.com/fmiotello by Marzieh Ali Atashi 

Summary by Marzieh Ali Atashi 

The fastVC project is a fast and efficient non-parallel and audio conversion tool.
in which the voice of a source speaker is similar to the voice of a target speaker without changing the temporal content of the language and is shown in the output speaker.

This is a waterfall model. This waterfall model consists of three main parts
ASR, Transcription, TTs

In this project, there is an automatic speech recognition model, a text-to-speech model, and a speech-to-code conversion model. The source code of the speech-to-transcription and text conversion part is performed by the encoder and the related sourcecode is in the project.
Text-to-speech conversion is performed with the voice of the target speaker in the Synthesizer and Vocoder section, and the source code for its implementation is also available.

The remarkable thing about the fastVc project is that this cascade model has been used as a base in most of the projects of converting speech to other languages, changing speech to text, encoding, voice encryption, and the output of this cascade model.
This basic waterfall model is used in the main set of all projects implemented in all 120 languages in the world.
This cascade model can be taught and this training is well seen in the use of other languages and has been very efficient.



