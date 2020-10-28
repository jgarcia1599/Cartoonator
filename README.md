# Cartoonator

By Estelle Ocran and Junior Garcia

You can access the project <a href = "https://cartoondraw.herokuapp.com/">here</a>

## Description
For our Visual Project, we were fascinated in building upon the idea of the neural style transfer, which basically leverages deep neural networks to change the appearance of a target image based on the appearance of a style image.  
    
**First Paper on Neural Style Transfer**
```
@misc{gatys2015neural,
      title={A Neural Algorithm of Artistic Style}, 
      author={Leon A. Gatys and Alexander S. Ecker and Matthias Bethge},
      year={2015},
      eprint={1508.06576},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```
Not only did we find this technically interesting when exploring it in class, we also thought that it opened a vast array of creative possibilities.  As such, we began a process of exploring different tools and jupyter notebooks that implemented neural style transfers in order to gain inspiration as to what we wanted our project to be about. We knew from the get got that we wanted our project to be a tool anyone could use to create stylized images. After delving into different technologies and learning about them, we were able to conceive **Cartoonator**: a web-based tool that allows you to change your own target images based on your own style images. Users can upload target images and style images and see them being combined right there in their browser. In addition to adding ML-based styling, we alow users to draw on top of the image in order to spice up the generated artwork. We added this functioonality as we were interested in exploring authorship in AI-generated art. Are we the authors of the generated images as we were the ones who created this tool? Or are the authors the creators of the libraries we joined together to make this project a reality? Are the users of the tool the authors as well given how they can draw on top of the image after its been modified by our AI tool? How much do they need to draw oon the image to be authors? We dont know the answers to this questions, but we hope our tool creates discussions that one day can lead to solving them. 

## Process and Implementation
For this project, we used the <a href = "https://www.jsdelivr.com/package/npm/@magenta/image">magenta/image</a> library that performs stylization on a content/style image pair without having to retrain the model if the style image changes. The magenta/image library wraps around <a href = "https://twitter.com/ReiiYoda">Reiichiro Nakano's</a> TensorFlow.js <a href = "https://github.com/reiinakano/arbitrary-image-stylization-tfjs">port</a> of Ghiasi et al.'s < a href = "https://arxiv.org/abs/1705.06830">arbitrary stylization model.</a><br>

  The regular and cartoon images uploaded on the page are then passed to the already trained model for the style of the cartoon image to be applied to the regular image. The result which is a cartoonized image is then displayed on the right of the screen. <br>
  
  Using vanilla javascript, we then added drawing/scribbling capablities to the cartoonized image produced such that the user can draw upon the image. The user can has the option of selecting different colors for the drawing and can download the image at the end.

## Reflection and Evaluation
We initially wanted to train a model with our own data but found that hard to achieve with the existing solutions; we encountered errors in some of the pre-existing code we were trying and the few ones that could have worked used too much computational time. Thus, we turned to the magenta/image library which fit our needs perfectly. We also tried using p5js for the drawing capabilities but had issues using it in conjunction with the magenta library. All in all, we are happy we came up with a very minimal implementaton of Cartoonator. We think the next step is to introduce real-time camera capturing.
 
