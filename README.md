# DARTs-UNET

The U-Net architecture was a major breakthrough in the image segmentation field at the time of its 2015 publishing. The network itself was able to efficiently and accurately segment images with a (comparatively) sparse model and little data. The advancement was mainly credited to an encoder-decoder structure that extracted high-level features, and skip connections that gave the decoder more fine-grained context. Iterations on U-Net such as U-Net++, U-Net3+, and ELU-Net, have attempted to improve the architecture by modifying the skip connection. This thesis aims to take a more high-level approach to designing these skip connections by utilization DARTs, a Neural Architecture Search algorithm, to make these decisions via a gradient-based relaxation of the filter search space. 

DARTs relaxes the assumption of binary relationships between feature maps, concerning their operations. Instead, many learnable parameters $\alpha$ are utilized in a weighted sum of many candidate operations when traversing from one feature map to the next. After bilevel training, where the learnable parameters $\alpha$ and network weights $w$ are modified in-turn, the operation(s) with the highest $\alpha$ value(s) are retained. Then the network is retrained with the final architecture. 

# Links

[Logged Model Weights](https://drive.google.com/drive/folders/1Rdo0cLG7ruatrH7tfh-9ng0mNC3faiAg?usp=sharing)

[Augmented Dataset](https://drive.google.com/drive/folders/1qhOcdow3ApTFXsvVHSokNMnlqtEAu25a?usp=sharing)

[Depreciated Info](https://drive.google.com/drive/folders/17oH-hUwa-B0bTQP1T76bOqwEAe7_jCaf?usp=sharing)

[Thesis Paper](https://docs.google.com/document/d/1_zbY-2XX0C2PiM7ar4lKihEwtL0I2CuomQyYIO653U0/edit?usp=sharing)
