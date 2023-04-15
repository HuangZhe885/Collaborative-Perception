<img width="70%" alt="WechatIMG208" src="https://user-images.githubusercontent.com/44192081/232229514-6dacfb34-fc74-4fe9-947d-2cf08f75b7f6.png">

# AEV2V: Accurate and Efficient Vehicle-to-Vehicle Collaborative Perception


Multi-agent collaborative perception could significantly upgrade the perception performance by enabling agents to share information with each other through communication.However, duplicated data sharing and high communication overhead remain significant barriers to real-time communication for autonomous driving. 
<img width="70%" alt="WechatIMG206" src="https://user-images.githubusercontent.com/44192081/232229359-c2b8907d-31c9-4fd3-984b-0c153b6927ca.png">

Using spatially sparse depth information can reduce the amount of shared data, however the compressed depth features are sparse and low-resolution, resulting in inadequate fusion across multi-agents and unstable bounding boxes, leading in classification and regression misalignment.As a result, we present a sparse perception framework for fusing multi-agent features while decreasing communication traffic, keeping complementary features for complete fusion, enhancing the stability of bounding boxes, and reducing classification and regression misalignment.  Extensive experimental results demonstrate that AEV2V  sets new state-of-the-art performance for 3D object detection and achieves robust performance even under harsh, noisy environments.


https://user-images.githubusercontent.com/44192081/232229098-8d5a62a6-ac25-4e82-95ee-00d89994eec3.mp4


# METHOD
* we design a lightweight spatial semantic feature module, which expands the receptive field of the confidence map, making the confidence map richer in spatial and semantic information.
<img width="50%" alt="WechatIMG209" src="https://user-images.githubusercontent.com/44192081/232229752-7e397f39-6981-41ec-8e64-5c3a709ad49c.png">

* The Confidence Fused axial attention (Co-FAX) method was proposed to handle the information fusion of multi-agents and multi-views.   

* The predicted confidence is further rectified with our designed IoU-aware confidence rectification module to make the confidence more consistent with the localization accuracy.
<img width="50%" alt="WechatIMG209" src="https://user-images.githubusercontent.com/44192081/232229782-070cc47c-c56c-4424-91c5-ef24865d9193.jpeg">

# RESULTS
We evaluate the effectiveness of the proposed AEV2V on  the V2V perception dataset V2XSet. 

<img width="50%" alt="WechatIMG209" src="https://user-images.githubusercontent.com/44192081/232229918-3b35f90c-53ea-43ad-b8fb-5ffc1de73fe4.jpeg">
* Component ablation study
<img width="50%" alt="WechatIMG209" src="https://user-images.githubusercontent.com/44192081/232229935-f1d5c328-ef78-4b31-8819-f2c81434bb11.jpeg">
* Major components comparisons of collaborative perception systems.
<img width="50%" alt="WechatIMG209" src="https://user-images.githubusercontent.com/44192081/232230105-032371c8-9d80-46e8-9066-f05b40817916.jpeg">

# Visualization of collaboration

<img width="70%" alt="WechatIMG214" src="https://user-images.githubusercontent.com/44192081/232230149-82dd9560-3fcf-4168-9925-80b48c120b7c.png">
<img width="70%" alt="WechatIMG214" src="https://user-images.githubusercontent.com/44192081/232230167-bc661a63-bdb7-451c-b62f-fa0f82164e9b.png">

# CONCLUSION

We porpose AEV2V, a novel detection-efficient collaborative perception framework. Our main contributions include the spatical-semantic attention model for extracting  dilated spatial confidence map at each agent to promote pragmatic compression; we also propose a Confidence Fused axial attention (Co-FAX) method that can handle the information fusion of multi-agents and multi-views. It not only implements a combination of global and local attention methods in the high-dimensional feature space, but it also makes use of essential information from the upstream network for more focused fusion. To alleviate the misalignment between the localization accuracy and classification confidence, we design the confidence-aware IoU rectification module for post-processing the confidence. Extensive experiments on simulated  datasets  show that AEV2V achieves superior performance on multi-agent cooperative 3D object detection.

