# Lip-Syncing-Model
This repository contains an AI model for lip-syncing, which synchronizes an audio file with a video file. The model is trained using deep learning techniques and consists of two main components: a lip-syncing model and a text-to-speech (TTS) model.

## Requirements

To run the lip-syncing model, you will need the following dependencies:

- Python 3.x
- TensorFlow
- NumPy
- OpenCV
- dlib
- face_alignment
- moviepy
- Wav2Lip (optional, if using the Wav2Lip model)

You can install the required dependencies by running the following command:

```shell
pip install -r requirements.txt
```

## Running the Model

1. Clone the repository:

```shell
git clone https://github.com/def-TharunL/lip_syncing_model.git
```

2. Navigate to the project directory:

```shell
cd lip_syncing_model
```

3. Prepare your input data:
   - Place your audio file in the `audio` directory.
   - Place your video file in the `video` directory.
   - (Optional) If using the Wav2Lip model, extract video frames using the provided script:

   ```shell
   python extract_frames.py --video_path video/video_file.mp4 --output_dir frames/
   ```

4. Run the lip-syncing model:
   - If using the default lip-syncing model:

   ```shell
   python lip_sync.py --audio_path audio/audio_file.wav --video_path video/video_file.mp4
   ```

   - If using the Wav2Lip model:

   ```shell
   python lip_sync_wav2lip.py --audio_path audio/audio_file.wav --frames_dir frames/
   ```

5. The lip-synced video will be saved in the `output` directory.

## Evaluating Performance

To evaluate the performance of the lip-syncing model, you can use the following metrics:

1. Visual Inspection: Watch the lip-synced video and assess whether the lip movements are synchronized with the audio.

2. Lip Movement Accuracy: Manually annotate a subset of the lip-synced videos and calculate the accuracy of the lip movements compared to the ground truth.

3. Subjective Evaluation: Collect feedback from users or a panel of judges to assess the quality and naturalness of the lip-synced videos.

4. Objective Evaluation: Use pre-defined metrics such as frame-level or phoneme-level accuracy, lip-sync error rate, or spectral similarity measures to quantify the performance of the model.
