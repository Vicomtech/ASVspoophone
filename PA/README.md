# ASVspoophone - Physical Access (PA)


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
PA/
    ASVspoophone_PA_cm_baseline_scores/
    ASVspoophone_PA_cm_protocols/
    ASVspoophone_PA_dev/
    ASVspoophone_PA_eval/
    ASVspoophone_PA_train/
    README.md
```


### 2. Description of the audio files

``ASVspoophone_PA_train, ASVspoophone_PA_dev,`` and ``ASVspoophone_PA_eval`` contain audio files for training, development, and evaluation ``(PA_T_*.ALW, PA_D_*.ALW, and PA_E_*.ALW, respectively)``. 
    
The audios are codified in ``8 kHz 8 bit A-Law RAW`` format.
They can be easily converted to another extension with the following command:

```
avconv -f alaw -ar 8000 -i $ALW_file $new_file
```
e.g.:

```
avconv -f alaw -ar 8000 -i PA_D_0000003_M.ALW PA_D_0000003_M.wav
```


### 3. Description of the CM protocol

>___Disclaimer: The ASVspoophone corpus has only used the files for the Countermeasure (CM) protocol inside ASVspoophone corpus.___

``ASVspoophone_PA_cm_protocols`` contains protocol files in ASCII format for ``ASVspoof`` countermeasures:

```
ASVspoof2019.PA.cm.train.trn.txt: training file list
ASVspoof2019.PA.cm.dev.trl.txt: development trials
ASVspoof2019.PA.cm.eval.trl.txt: evaluation trials
```

Each column of the protocol is formatted as:

```
SPEAKER_ID AUDIO_FILE_NAME ENVIRONMENT_ID ATTACK_ID KEY
```

```
1) SPEAKER_ID: PA_****, a 4-digit speaker ID
2) AUDIO_FILE_NAME: name of the audio file
3) ENVIRONMENT_ID: a triplet (S,R,D_s), which take one letter in the set {a,b,c} as categorical value, defined as:

                           a        b         c
                    -------------------------------------
                    S:     2-5      5-10      10-20
                    R:     50-200   200-600   600-1000
                    D_s:   10-50    50-100    100-150

                Where 
                    S: Room size (square meters)
                    R: T60 (ms)
                    D_s: Talker-to-ASV distance (cm)

4) ATTACK_ID:  a duple (D_a,Q), which take one letter in the set {A,B,C} as categorical value, defined as:

                         A         B        C
                    --------------------------------
                    Z:   10-50     50-100   > 100
                    Q:   perfect   high     low

                Where
                    Z: Attacker-to-talker distance (cm) 
                    Q: Replay device quality

        	For bonafide speech, ATTACK_ID is left blank ('-')
    
5) KEY: 'bonafide' for genuine speech, or, 'spoof' for spoofing speech
```

Definition of Replay Device Quality (Q):


```

              OB (kHZ)   minF (Hz)   linearity (dB)
    --------------------------------------------------------------
    Perfect   inf        0           inf     
    High      > 10       < 600       > 100
    Low       < 10       > 600       < 100

    where:  
        OB: is the occupied bandwidth
        minF: is the lower bound of OB
        linearity: is the linear/non-linear OB power difference
```


### 4. Baseline CM Scores

