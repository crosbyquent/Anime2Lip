# **Anime2Lip**: Accurately Lip-syncing Animated Video In The Wild

Anime2Lip is a fork of davidkundrats/Wav2Lip, an implementation of Wav2Lip, specifically trained on the [Anim400k dataset](https://github.com/davidmchan/Anim400K). This large-scale dataset consists of animated video clips in 
both English and Japanese, enabling synchronized lip-syncing for animated characters.

Canonical lip synchronization research has focused on generating accurate and expressive human talking-head video based on target audio. Little research has been done on the potential of canonical
lip synchronization approaches on animated video. 

We hope that training Wav2Lip's generator and expert discriminator on animated video will be a preliminary step in this research direction. Potential industry uses include automatic dubbing for animated films and series, 
enhancing the localization of animated content, and improving virtual character interactions in video games and virtual reality.

## Installation

Open a conda prompt to a directory where you would like to install the wav2lip web ui.
```
conda create -n anime2lip python=3.10
conda activate anime2lip
git clone https://github.com/natlamir/Wav2Lip-WebUI.git anime2lip
cd anime2lip
conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia
pip install -r requirements.txt
```

Remember to get the model and weights from below. With those things done, you should be able to double click the **run.cmd** to launch the Web UI.

Make sure to download the pre-trained model and weights and place them in the appropriate directory:
Pre-trained model (rename to s3fd.pth and place in `face_detection/detection/sfd` folder): 

https://www.adrianbulat.com/downloads/python-fan/s3fd-619a316812.pth

## Usage

To use Anime2Lip, provide the path to your video and audio files:
```bash
python inference.py --checkpoint_path path_to_checkpoint --face video.mp4 --audio audio.wav
