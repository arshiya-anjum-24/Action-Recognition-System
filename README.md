# Action-Recognition-System
Group project to preprocess the Weizmann Human Action Dataset by separating mixed image/text data into specific action folders and generating a combined video using OpenCV. Implemented folder-based action classification and natural sorting of frames for accurate sequence rendering.

## Dataset Description

- Total files: **1500** (image + text files)
- Source: **Weizmann Human Action Recognition Dataset**
- We extracted **4 specific actions** from this data:
  - `walk`: First 300 images and text files
  - `run`: Files 600–900
  - `wave`: Files 900–1200
  - `jump`: Files 1200–1500
- Files from 300–600 were discarded (unwanted data).

---

##  How It Works

1. Organizes images into 4 separate action folders based on their sequence.
2. Sorts each folder's images in correct order using natural sorting.
3. Combines images from all action folders into a single output video.
4. Generates an `.avi` video with frame size matching input images and FPS of 10.

---

##  How to Run

1. **Clone the repo:**
    ```bash
    git clone https://github.com/arshiya-anjum-24/Action-Recognition-System.git
    cd Action-Recognition-System
    ```

2. **Install required packages:**
    ```bash
    pip install opencv-python natsort
    ```

3. **Set up your dataset:**
    - Place all 1500 image and text files inside a folder like:
      ```
      /Users/arshiya_anjum/weizmann dataset/weizmann/
      ```
    - Manually or via script, split them into these 4 subfolders:
      - `walk/`: first 300 images and text files
      - `run/`: images and text files 600–900
      - `wave/`: images and text files 900–1200
      - `jump/`: images and text files 1200–1500

4. **Run the script:**
    ```bash
    python code.py
    ```

---

##  Output

-  A combined video named `combined_video.avi` containing all relevant actions
-  Sorted frame-by-frame playback from the walk, run, wave, and jump folders

---

##  Sample Project Structure

weizmann/
┣ walk/
┃ ┗ img001.jpg, img002.jpg, ...
┣ run/
┃ ┗ img601.jpg, ...
┣ wave/
┃ ┗ img901.jpg, ...
┣ jump/
┃ ┗ img1201.jpg, ...


---

##  Authors

This project was developed as part of a **group academic contribution** by:

- **Arshiya Anjum Shaik** – Frame integration, video generation logic  
  [LinkedIn](https://linkedin.com/in/arshiya-anjum-shaik)

- **Velaga Mouli** – Dataset segmentation, folder structuring and cleanup
   [LinkedIn](https://linkedin.com/in/mouli-velaga)

---

##  Contribution

Contributions and improvements are welcome!  
If you'd like to improve the automation (e.g., dataset auto-sorting, video labeling), feel free to fork the repo, add features, and submit a PR.

---

##  License

This project is for educational purposes only, based on the publicly available **Weizmann Dataset**
