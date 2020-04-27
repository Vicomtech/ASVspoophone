
# ASVspoophone


## Description

The ``ASVspoophone corpus`` is the telephonic version of the ``ASV Spoof 2019 corpus`` found at [https://www.asvspoof.org](https://www.asvspoof.org).

It contains the telephonic versions of the audios used for the countermeasure (CM) ASV Spoof 2019 challenge, which have been created by transferring each of them through real land-land, mobile-land and land-mobile telephonic channels.

The results are the corresponding 8 kHz 8 bit A-Law versions of the originial audios, which can be used to train anti-spoofing systems that will be used on real telephonic scenarios such as call and contact centres. 

## Names:

 * [Ander González-Docasal](https://www.vicomtech.org/en/vicomtech/team/835) <sup>1</sup>
 * [Aitor Álvarez](https://www.vicomtech.org/en/vicomtech/team/228) <sup>1</sup>
 * [Haritz Arzelus](https://www.vicomtech.org/en/vicomtech/team/343) <sup>1</sup>
 * [Ane Lazpiur]() <sup>2</sup>
 * [Paz Delgado]() <sup>2</sup>

Affiliations:

<sup>1</sup> [Vicomtech Foundation, Basque Research and Technology Alliance (BRTA)](https://www.vicomtech.org), Mikeletegi 57, 20009 Donostia-San Sebastián (Spain)
 

<sup>2</sup> [Natural Vox S.A.U.](http://www.naturalvox.eu), Araba-Álava, Spain


## Names ASV spoof 2019:

 * Names (equal contribution): 
 * Junichi Yamagishi <sup>1</sup><sup>2</sup>
 * Massimiliano Todisco <sup>3</sup>
 * Md Sahidullah <sup>4</sup>
 * Héctor Delgado <sup>3</sup>
 * Xin Wang <sup>1</sup>
 * Nicholas Evans <sup>3</sup>
 * Tomi Kinnunen <sup>5</sup>
 * Kong Aik Lee <sup>6</sup>
 * Ville Vestman <sup>5</sup>
 * Andreas Nautsch <sup>3</sup>

Affiliations: 

<sup>1</sup> National Institute of Informatics, Japan

<sup>2</sup> University of Edinburgh, UK

<sup>3</sup> EURECOM, France

<sup>4</sup> Inria, France 

<sup>5</sup> University of Eastern Finland, Finland

<sup>6</sup> NEC, Japan 

Copyright (c) 2019 The Centre for Speech Technology Research (CSTR) University of Edinburgh


========================

## Reference

When publishing studies or results on the ASVspoophone corpus, please cite:

___TODO: Add reference to paper___






# Directory Structure
```
    ASVspoophone/
        LA/
            ASVspoophone_LA_cm_baseline_scores/
            ASVspoophone_LA_cm_protocols/
            ASVspoophone_LA_dev/
            ASVspoophone_LA_eval/
            ASVspoophone_LA_train/
            README.md
        PA/
            ASVspoophone_PA_cm_baseline_scores/
            ASVspoophone_PA_cm_protocols/
            ASVspoophone_PA_dev/
            ASVspoophone_PA_eval/
            ASVspoophone_PA_train/
            README.md
        README.md
```

========================

# Overview

The ASV Spoof 2019 corpus was created in order to allow the scientific community to research on anti-spoofing measures for Automatic Speaker Verification systems. It merges the three different spoofing attacks that have been studied on previous years: synthetic and converted speech (2015) and replay attacks (2017). It is therefore subdivided in two different scenarios: Physical Access scenario (PA) for recording attacks and Logical Access scenario (LA) for synthesis and voice conversion. These two scenarios are at the same time subdivided on three partitions for train, development and evaluation purposes.

All the audios in the ASV Spoof 2019 corpus are encoded in single channel 16 kHz 16 bit FLAC format. However, this is not the ideal configuration for processing telephonic audios such as those from contact and call centres; and therefore there is a need for transferring this whole data set through a telephonic channel in order to better adapt the anti-spoofing systems to a real telephonic application scenario.

This is why we present the ASVspoophone corpus, where all the countermeasure audios have been converted to telephonic domain by transferring them through the corresponding channel. Some of the audios, marked by \*\_F, have been transferred from land- to land-lines through the traditional copper cable line; whereas the rest of them, marked by \*\_M, used a SIP proxy to be sent from mobile-line to land-line configuration or vice versa. The result are RAW audios codified in 8 kHz 8 bit A-Law format.


# COPYING 
You are free to use this database under [Open Data Commons Attribution License (ODC-By)](https://opendatacommons.org/licenses/by/1.0/index.html). 

Regarding Open Data Commons Attribution License (ODC-By), please see 
https://opendatacommons.org/licenses/by/1.0/index.html

THIS DATABASE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS 
OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF 
MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE 
COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, 
EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF 
SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) 
HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR 
TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS 
DATABASE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
