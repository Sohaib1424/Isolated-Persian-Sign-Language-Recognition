# Isolated Persian Sign Langugage Recognition

This project was inspired by tge [Google - Isolated Sign Language Recognition](https://www.kaggle.com/competitions/asl-signs/overview) competition. To create the dataset used for this project, videos of 280 signs were recorded from the waist up (A few of them represent the same word, i.e., they convey the same meaning but with slightly different representations.) , and similar to Google's Isolated Sign Language dataset, labeled landmark data was extracted using [Mediapipe Holisitc](https://github.com/google-ai-edge/mediapipe/blob/master/docs/solutions/holistic.md). The videos had varying durations (i.e., different numbers of frames); therefore, the sequence lengths of the extracted landmarks vary across videos.

The Mediapipe Holisitc model extracts 543 landmarks per person in a frame:
- 33 body pose landmarks, representing key skeletal points (e.g., shoulders, elbows, hips).
- 468 face landmarks.
- 21 landmarks per hand.

With each landmark having 3 attributes `x`, `y`, and `z`. Consequently, presented in a tabular format, there are 1626 features + 2 more features, Video Number (`video_NO`) and Frame Number (`frame_NO`), and the label. For starters, a [starter notebook](Starter_Notebook.ipynb) has also provided to help you familiarize yourselves with the dataset.

The following is an example of landmarks extracted from a video corresponding to the word `مناسبت` (`Occasion`).

<img src="/gifs/sign1.gif" width="250" height="250"/>

The Dataset can be download either from [Google Drive](https://drive.google.com/file/d/1kWWU4PALe5zPkVDFyYB4fQzPFK5og2jT/view?usp=sharing) or [Kaggle](https://www.kaggle.com/datasets/sohaibmoradi/psl-tabular).

