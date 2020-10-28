# Cartoonator

By Estelle Ocran and Junior Garcia

You can access the project <a href = "https://cartoondraw.herokuapp.com/">here</a>

## Description

## Process and Implementation
For this project, we used the <a href = "https://www.jsdelivr.com/package/npm/@magenta/image">magenta/image</a> library that performs stylization on a content/style image pair without having to retrain the model if the style image changes. The magenta/image library wraps around <a href = "https://twitter.com/ReiiYoda">Reiichiro Nakano's</a> TensorFlow.js <a href = "https://github.com/reiinakano/arbitrary-image-stylization-tfjs">port</a> of Ghiasi et al.'s < a href = "https://arxiv.org/abs/1705.06830">arbitrary stylization model.</a><br>

  The regular and cartoon images uploaded on the page are then passed to the already trained model for the style of the cartoon image to be applied to the regular image. The result which is a cartoonized image is then displayed on the right of the screen. <br>
  
  Using vanilla javascript, we then added drawing/scribbling capablities to the cartoonized image produced such that the user can draw upon the image. The user can has the option of selecting different colors for the drawing and can download the image at the end.

## Reflection and Evaluation
We initially wanted to train a model with our own data but found that hard to achieve with the existing solutions; we encountered errors in some of the pre-existing code we were trying and the few ones that could have worked used too much computational time. Thus, we turned to the magenta/image library which fit our needs perfectly. We also tried using p5js for the drawing capabilities but had issues using it in conjunction with the magenta library. All in all, we are happy we came up with a very minimal implementaton of Cartoonator. We think the next step is to introduce real-time camera capturing.
 
