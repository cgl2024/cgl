# Vascular segmentation
* Generate Model
  * GAN
     * RV-GAN: Segmenting Retinal Vascular Structure in Fundus Photographs using a Novel Multi-scale Generative Adversarial Network.
       Sharif Amit Kamran, Khondker Fariha Hossain, Alireza Tavakkoli, Stewart Lee Zuckerbrod, Kenton M. Sanders, and Salah A. Baker.  
       https://arxiv.org/abs/2101.00535.
       #使用两个GAN生成网络分别
  * VAE
     * A Deep Learning Design for Improving Topology Coherence in Blood Vessel Segmentation. 
       Ricardo J. Ara´ujo, Jaime S. Cardoso, and H´elder P.Oliveira.  
       https://link.springer.com/chapter/10.1007/978-3-030-32239-7_11. 
* U-Net
  * SA-UNet: Spatial Attention U-Net for Retinal Vessel Segmentation.
    Changlu Guo, Márton Szemenyei,Yugen Yi, Wenle Wang, Buer Chen, Changqi Fan11Budapest University of Technology and Economics,Budapest, Hungary.
    https://ieeexplore.ieee.org/search/searchresult.jsp?newsearch=true&queryText=SA-UNet:%20Spatial%20Attention%20U-Net%20for%20Retinal%20Vessel%20Segmentation.
    # 在Unet的基础上引入了一个dropout卷积模块替代传统的卷积层，其主要由卷积dropblack，BN，Relu构成，防止模型过拟合；同时引入空间注意模块SA，SA首先沿着通道方向进行最大池化（H x W x 1）和平均池化（H x W x 1）操作，并将它们拼接（H x W x 2）起来，生成一个有效的特征描述符。然后通过卷积层和连接的特征描述符上的Sigmoid激活函数，生成空间注意图（H x W x 1）,最后将空间注意图和输入（H x W x C）进行点乘得到输出，然后作为解码器的输入继续计算。
