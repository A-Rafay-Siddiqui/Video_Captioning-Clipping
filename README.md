# Video Captioning and Processing

The notebook provides a script for processing a video by generating captions for each frame using the BLIP (Bridging Language and Image Pretraining) model, adding captions to the video frames, and optionally clipping the video based on the similarity between the captions and a provided activity description.

## Dependencies

Make sure you have the following dependencies installed:

- OpenCV (`cv2`)
- NumPy (`numpy`)
- Transformers (`transformers`)
- MoviePy (`moviepy`)
- PyTorch (`torch`)

You can install them using pip:

```bash
pip install opencv-python-headless numpy transformers moviepy torch
```
## Usage
- Clone the repository or download the notebook.
- Install the dependencies.
- Open the notebook in Jupyter Notebook or GoogleColab.
- Run the cell in the notebook to execute the code.
- Follow the prompts to enter the video path and other details.

## Functions
The notebook contains the following functions:

-  generate_captions(video_path): Generates captions for each frame in the video using the BLIP model.
- add_captions_to_video(video_path, captions, output_path): Adds captions to the video frames.
- calculate_similarity(captions, description): Calculates the similarity between the captions and the provided description.
- clip_video(video_path, output_path, frame_indices, fps=30): Clips the video based on the provided frame indices.
- process_video(): Main function to process the video. It interacts with the user to get input video path and other details.

## Note
- The script uses the BLIP model (Salesforce/blip-image-captioning-base) for generating captions and calculating similarity. Ensure that you have the model downloaded or it will be downloaded automatically the first time you run the script.
- The BLIP model and processor are moved to GPU if available for faster processing.
