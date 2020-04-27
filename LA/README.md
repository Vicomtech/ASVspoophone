# ASVspoophone - Logical Access (LA)




## Names:

 * [Ander González-Docasal](https://www.vicomtech.org/en/vicomtech/team/835) <sup>1</sup>
 * [Aitor Álvarez](https://www.vicomtech.org/en/vicomtech/team/228) <sup>1</sup>
 * [Haritz Arzelus](https://www.vicomtech.org/en/vicomtech/team/343) <sup>1</sup>
 * [Ane Lazpiur]() <sup>2</sup>
 * [Paz Delgado]() <sup>2</sup>

## Affiliations:

<sup>1</sup> [Vicomtech Foundation, Basque Research and Technology Alliance (BRTA)](https://www.vicomtech.org), Mikeletegi 57, 20009 Donostia-San Sebastián (Spain)
 

<sup>2</sup> [Natural Vox S.A.U.](http://www.naturalvox.eu), Araba-Álava, Spain


## Information


### 1. Directory Structure

```
LA/
    ASVspoophone_LA_cm_baseline_scores/
    ASVspoophone_LA_cm_protocols/
    ASVspoophone_LA_dev/
    ASVspoophone_LA_eval/
    ASVspoophone_LA_train/
    README.md
```


### 2. Description of the audio files


``ASVspoophone_LA_train, ASVspoophone_LA_dev, and ASVspoophone_LA_eval`` contain audio files for training, development, and evaluation ``(LA_T\_\*.ALW, LA_D\_\*.ALW, and LA_E\_\*.ALW, respectively)``. 
    
The audios are codified in ``8 kHz 8 bit A-Law RAW`` format.

They can be easily converted to another extension with the following command:


```
avconv -f alaw -ar 8000 -i $ALW_file $new_file
```
e.g.:
    
```
avconv -f alaw -ar 8000 -i LA_D_1024892_F.ALW LA_D_1024892_F.wav
```


### 3. Description of the CM protocol

>___Disclaimer: The ASVspoophone corpus has only used the files for the Countermeasure (CM) protocol inside ASVspoophone corpus.___

``ASVspoophone_LA_cm_protocols`` contains protocol files in ASCII format for ASVspoof countermeasures:

```
ASVspoophone.LA.cm.train.trn.txt: training file list
ASVspoophone.LA.cm.dev.trl.txt: development trials
ASVspoophone.LA.cm.eval.trl.txt: evaluation trials 
```

Each column of the protocol is formatted as:

```
SPEAKER_ID AUDIO_FILE_NAME - SYSTEM_ID KEY

1) SPEAKER_ID:          LA_****, a 4-digit speaker ID
2) AUDIO_FILE_NAME:     LA_****, name of the audio file
3) SYSTEM_ID:           ID of the speech spoofing system (A01 - A19), 
                        or for bonafide speech SYSTEM-ID is left blank ('-')
4) -:                   This column is NOT used for LA.
5) KEY:                'bonafide' for genuine or 'spoof' for spoofing speech
```

_Note that:_
   
1. The third column is left blank (-) to make the structure coherent with physical access file list

2. Brief description on LA spoofing systems, where TTS and VC denote text-to-speech and voice-conversion systems:



||||
| ------------- |:-------------| :-----|
| A01	| TTS	| neural waveform model		|
| A02	| TTS	| vocoder		|
| A03	| TTS	| vocoder		|
| A04	| TTS	| waveform concatenation		|
| A05	| VC	| vocoder		|
| A06	| VC	| spectral filtering		|
| A07	| TTS	| vocoder+GAN		|
| A08	| TTS	| neural waveform		|
| A09	| TTS	| vocoder		|
| A10	| TTS	| neural waveform		|
| A11	| TTS	| griffin lim		|
| A12	| TTS	| neural waveform		|
| A13	| TTS_VC	| waveform concatenation+waveform filtering		|
| A14	| TTS_VC	| vocoder		|
| A15	| TTS_VC	| neural waveform		|
| A16	| TTS	| waveform concatenation		|
| A17	| VC	| waveform filtering		|
| A18	| VC	| vocoder		|
| A19	| VC	| spectral filtering		|




### 4. Baseline CM Scores
