# RD_Takehome

```bash
See my first takehome I completed and deployed in AWS:
https://www.loom.com/share/b8389cb7109e462a9fc8dccd3f0aa5c3?sid=7eaa432e-ab42-49fe-897c-1960d564a36f
```
## Q/A

### 1. Create datasets:
   I haven't uploaded any as they are too large. However, I uploaded a way to scrape images for the Image Detector and the others can be found on Kaggle as they are open source. The text was from multiple sources so it is harder to locate but the audio is from: https://www.kaggle.com/datasets/birdy654/deep-voice-deepfake-voice-recognition/data

### 2. Explain the choices
#### a. For the image detector my goal was to get real photos and fake photos. The fake photos were pulled from a website where you have to pay for their AI generated headshots but I just scraped them by copying the website's html and generating a list of links in which I locally downloaded each image. Same for the headshots I retrieved. The fake images all have a pretty similar format and I didn't want this to trip up the Model so I augmented the images as well which created more data and moved it away from the format the photos are locked in. The last model seemed flawless; but needs more in-depth analysis because flawless can be scary from time to time. 
#### b. For Audio Generator I was given audio files as well as a CSV that was generated using the Audio with numerous imports. Being that I want to generate my own CSV's in the future I created a function that reproduces the data and then continued with the data already given. I tested a LogRegressor vs a custom Nueral Network and the Nueral Network, which was very simple, outperformed the LogRessor by a major margin which can be reflected in the confusion matrix visualized in the notebook. 
#### c. The Text analysis needs more work. I was able to create 4 different models to compare against but there were other advanced techniques such as ensembling which I have yet to integrate. I also built a very basic NN to compare to some of the other classifiers I was competing with. I used different Vectorizers as a medium to test which one would perform better as well. In the end, It accurately works at 93%. I use Accuracy as a metric for all of the above given the fact that I am unsure if a False positive rate is helpful (like in a medical situation) so I defaulted to accuracy vs F1 score for example. 
### 3. The third question is answered in the uploaded notebooks by visualizing the confusion matrixes. A lot of the binary classifications are percentages out of 100 so I set a threshold of .5 and anything greater became 1 or anything less became 0 to differentiate between what is real and fake. Communicating this to a non-technical audience would include the visualization of the corresponding confusion matrix to a specific use case and model and going in-depth about the performance and the story of significance for the chosen scoring metric (in this case accuracy) held in the use case. 
