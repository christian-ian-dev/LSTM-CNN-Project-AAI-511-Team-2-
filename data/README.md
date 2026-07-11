Download the Kaggle MIDI dataset and extract it here. Do not upload the MIDI files to GitHub.

import kagglehub

# Download latest version
path = kagglehub.dataset_download("blanderbuss/midi-classic-music")

print("Path to dataset files:", path)
