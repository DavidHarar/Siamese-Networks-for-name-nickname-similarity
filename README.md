# Siamese Networks for name and nickname similarity  
In this project, I design, implement and compare variouse deep learning siamese networks in order to learn a similarity measure between names and nicknames. Please see a thourough description of the project in [here](https://medium.com/towards-data-science/conversion-to-audio-may-improve-results-using-siamese-networks-for-nickname-classification-647cb0f88680).  
In short, I explore both text based models, implementing [Neculoiu, Versteegh and Rotaru (2017)](https://aclanthology.org/W16-1617.pdf) and modified versions of [Gehring et. al (2017)](https://arxiv.org/abs/1705.03122). Then, I also test the effect of converting texts to audio, and using 2d-CNNs siamese networks on spectograms rather on texts.  

![2D-CNN architecture](/images/2dCNN.jpg?raw=true)

Converting to audio makes sense in the current use-case, since that in many cases nicknames invloves changing letters while keeping the sounds of the nickname similar to the original name (for example, replaceing "i" with "ea"). Results showed that converting to audio using Googl's `gTTS` and then using 2d-CNN models on spectograms led to significant improvement on balanced accuracy, F1 and PR AUC, and for a much lower number of parameters.  

