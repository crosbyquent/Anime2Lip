# Anime2Lip

Anime2Lip is a fork of davidkundrats/Wav2Lip, an implementation of Wav2Lip, specifically trained on the [Anim400k dataset](https://github.com/davidmchan/Anim400K). This large-scale dataset consists of animated video clips in 
both English and Japanese, enabling synchronized lip-syncing for animated characters.

Canonical lip synchronization research has focused on generating accurate and expressive human talking-head video based on target audio. Little research has been done on the potential of canonical
lip synchronization approaches on animated video. 

We hope that training Wav2Lip's generator and expert discriminator on animated video will be a preliminary step in this research direction. Potential industry uses include automatic dubbing for animated films and series, 
enhancing the localization of animated content, and improving virtual character interactions in video games and virtual reality.

## Installation

Follow the steps below to set up Anime2Lip on your machine:

1. Clone this repository:
    ```bash
    git clone https://github.com/yourusername/Anime2Lip.git
    cd Anime2Lip
    ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Download the pre-trained model weights (link to weights).

## Usage

To use Anime2Lip, provide the path to your video and audio files:
```bash
python inference.py --checkpoint_path path_to_checkpoint --face video.mp4 --audio audio.wav
