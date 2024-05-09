# college-dropout-s
Our project is on license plate recognition. Our code supports license plate preprocessing, character segmentation, and two different model implementations for character sequence recognition based on image input.

Devpost Link: https://devpost.com/software/college-dropouts

<img width="612" alt="Screen Shot 2024-05-09 at 4 52 58 PM" src="https://github.com/erc-ma/License-Plate-Recognition/assets/103232379/6973b0ff-c088-417e-93ef-db0a47e3115c">

<img width="350" alt="Screen Shot 2024-05-09 at 4 53 21 PM" src="https://github.com/erc-ma/License-Plate-Recognition/assets/103232379/31ba6623-14ff-476f-88b2-ad2f493e609d">

<img width="350" alt="Screen Shot 2024-05-09 at 4 53 34 PM" src="https://github.com/erc-ma/License-Plate-Recognition/assets/103232379/5c13295d-8a6e-4e7e-a537-30df02af9011">

<img width="350" alt="Screen Shot 2024-05-09 at 4 53 47 PM" src="https://github.com/erc-ma/License-Plate-Recognition/assets/103232379/0d59d4bd-7bf8-4957-ab3d-d02300c0362a">

<img width="350" alt="Screen Shot 2024-05-09 at 4 53 57 PM" src="https://github.com/erc-ma/License-Plate-Recognition/assets/103232379/b9d3ac6f-50ab-4597-8247-b9b924e05bcb">

<br>
<img width="345" alt="Screen Shot 2024-05-09 at 4 54 13 PM" src="https://github.com/erc-ma/License-Plate-Recognition/assets/103232379/4cc25041-5faa-4bc9-b069-be0d3e565122">
<img width="345" alt="Screen Shot 2024-05-09 at 4 54 26 PM" src="https://github.com/erc-ma/License-Plate-Recognition/assets/103232379/38191fe9-d5fb-493f-940c-1eb6406cb6c4">

## To Run
Download the dataset here: https://www.inf.ufpr.br/vri/databases/tbFcZE-RodoSol-ALPR.zip (3 GB)
Create a folder in the project directory called 'data'
Navigate to the 'cars-br' folder in the dataset and add that to the 'data' folder.
Create a second folder called 'cars-br-cropped' in the data folder.
Run the preprocess function, which will populate the project with images, now cropped to only include the license plates.
Now, you can run both models on this data!

### Pre-process
Our pre-processing includes cropping the car images to include only the license plates. <br>
'get_inputs_lprnet' returns these cropped images as a tensor, to be used in the LPRNet Model which makes use of non-descript sequence data. <br>
'get_labels_lprnet' returns the labels of each image as a tensor in our integer to character mapping<br>
'get_segmented_images' returns a tensor of the segmented characters for each image, to be used in the Segmentation Model. This is done systematically through deterministic computer vision functions (cv2).<br>
'get_labels' returns the labels of each image as a tensor as one-hot encodings<br>

### LPRNetModel
Accuracy: 0 :(

### Segmented Model
Character-wise Accuracy: 44.4% <br>
Sequence-wise (True) Accuracy: 5.4%
