## Requirements

- Python 3.x
- OpenCV 4.x
- editdistance
- TensorFlow 2.x

## Command line arguments

- `--source`: dataset/model name (bentham, iam, rimes, saintgall, washington)
- `--arch`: network to be used (puigcerver, bluche, flor)
- `--transform`: transform dataset to the HDF5 file
- `--cv2`: visualize sample from transformed dataset
- `--kaldi_assets`: save all assets for use with kaldi
- `--image`: predict a single image with the source parameter
- `--train`: train model using the source argument
- `--test`: evaluate and predict model using the source argument
- `--norm_accentuation`: discard accentuation marks in the evaluation
- `--norm_punctuation`: discard punctuation marks in the evaluation
- `--epochs`: number of epochs
- `--batch_size`: number of the size of each batch

## Installation

1. Download http://www.transcriptorium.eu/~tsdata/BenthamR0/BenthamDatasetR0-Images.zip
2. Unzip it to /raw/bentham
3. Download http://www.transcriptorium.eu/~tsdata/BenthamR0/BenthamDatasetR0-GT.zip
4. Unzip it to /raw/bentham
5. Folder structure should look like:

```
├── raw
│   ├── bentham
│   │   ├── BenthamDatasetR0-GT
│   │   └── BenthamDatasetR0-Images
```
6. run `pip install -r requirements.txt`
7. `cd src`
8. `python main.py --source=bentham --transform`
9. `python main.py --source=bentham --cv2` to see an example recognition
