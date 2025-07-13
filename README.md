# barnacle
DALI Data Challenge 2025

## Overview

Challenge prompt: Scientists with the National Park Service are researching barnacle populations in coastal tide pools on the east coast. To analyze the results of their experiments, they often need to count the number of barnacles in a given area. To do this, they place a fixed size frame on a barnacle-covered rock, then take a picture. Later, a scientist/lab tech will manually count the number of barnacles in the picture, then record their results. There are often upwards of 1000 barnacles in an image, so this is a very time consuming process. These scientists have now come to you to speed up their pipeline. **What system can you develop to help them process these images faster?**

My final approach primarily uses:
  **ORB (Oriented FAST and Rotated BRIEF)** to detect keypoints in grayscale images, capturing local visual features typical of barnacles.
  **DBSCAN**, a density-based clustering algorithm, to group these keypoints into clusters that ideally correspond to individual barnacles.

## This repo contains...

* `youmi_barnicles.ipynb`: Jupyter notebook documenting the entire process, from brainstorming to conclusions (steps 1-7).
* modified versions of img1.png and img2.png, manually cropped to around the same dimensions as masked_img1.png and masked_img2.png

---

## How to run it

1. Open the notebook directly in Google Colab by uploading youmi_barnicles.ipynb or using the Colab “Open notebook” feature.
2.Make sure to upload the provided challenge images (img1.png, masked_img1.png, etc.) to the Colab runtime. You can do this via the file sidebar in Colab. 
3. Run all cells to see the outputs. The results should look like this:
<img width="576" height="320" alt="Screenshot 2025-07-13 at 15 20 41" src="https://github.com/user-attachments/assets/f953a338-ee6a-4ddb-baed-be1dd21898c6" />

## Notes:
I tried using CNN, Random Forest, and other approaches in previous attempts to build this program, but the final version of this program using ORB and DBSCAN produced the most accurate results. See below for failed attempts (low accuracy, no barnacles detected, etc.)...
<img width="540" height="448" alt="Screenshot 2025-07-11 at 21 51 49" src="https://github.com/user-attachments/assets/13609b67-379c-4852-a1a5-812cf2ef754f" />
<img width="801" height="416" alt="Screenshot 2025-07-11 at 21 51 37" src="https://github.com/user-attachments/assets/3097c563-c47f-4891-8e1b-285332239409" />
<img width="801" height="254" alt="Screenshot 2025-07-11 at 21 51 21" src="https://github.com/user-attachments/assets/9a0dc301-37d1-4e1a-88ae-91653cdc50c3" />
<img width="443" height="520" alt="Screenshot 2025-07-11 at 20 47 52" src="https://github.com/user-attachments/assets/0fddbe66-c92f-4231-80b0-927a068a87c2" />

