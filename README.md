# Vascular segmentation
* Generate Model
  * GAN
     * RV-GAN: Segmenting Retinal Vascular Structure in Fundus Photographs using a Novel Multi-scale Generative Adversarial Network.
       Sharif Amit Kamran, Khondker Fariha Hossain, Alireza Tavakkoli, Stewart Lee Zuckerbrod, Kenton M. Sanders, and Salah A. Baker.  
       https://arxiv.org/abs/2101.00535.
       旨在解决编码阶段中连续的分辨率损失，解码阶段无法恢复丢失的信息。使用两个GAN生成网络，生成器Gfine通过提取微分支、连接、阻塞等局部特征来合成细粒度的血管分割图像，生成器Gcraure试图学习和保存全局信息。<br>
  * VAE
     * A Deep Learning Design for Improving Topology Coherence in Blood Vessel Segmentation.<br>
       Ricardo J. Ara´ujo, Jaime S. Cardoso, and H´elder P.Oliveira.<br>
       https://link.springer.com/chapter/10.1007/978-3-030-32239-7_11.<br>
       通过在U-Net网络之后连接一个VAE模型学习血管图像中的拓扑结构对U-Net输出图像做进一步的细化操作。
* U-Net
  * SA-UNet: Spatial Attention U-Net for Retinal Vessel Segmentation.<br>
    Changlu Guo, Márton Szemenyei,Yugen Yi, Wenle Wang, Buer Chen, Changqi Fan11Budapest University of Technology and Economics,Budapest, Hungary.<br>
    https://ieeexplore.ieee.org/search/searchresult.jsp?newsearch=true&queryText=SA-UNet:%20Spatial%20Attention%20U-Net%20for%20Retinal%20Vessel%20Segmentation.<br> 
    主要针对视网膜血管的分割，在Unet的基础上引入了一个dropout卷积模块替代传统的卷积层，其主要由卷积dropblack，BN，Relu构成，防止模型过拟合；同时引入空间注意模块SA，SA首先沿着通道方向进行最大池化和平均池化操作，并将它们拼接起来，生成一个有效的特征描述符。然后通过卷积层和连接的特征描述符上的Sigmoid激活函数，生成空间注意图,最后将空间注意图和输入进行点积，作为解码器的输入继续计算。<br>
