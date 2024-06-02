


# Collaborative 3D Object Detection by Intelligent Vehicles Considering Semantic Information and Agent Heterogeneity

<img width="70%" alt="image" src="https://github.com/HuangZhe885/Collaborative-Perception/assets/44192081/a5f33c69-e67c-423d-aedf-eb8cf573f3d5">

Collaborative perception can significantly enhance perception performance through information sharing among multiple smart vehicles and roadside perception systems.  Existing methods often require sharing and aggregating all information from other collaborators. 

<img width="70%" alt="WechatIMG206" src="https://user-images.githubusercontent.com/44192081/232229359-c2b8907d-31c9-4fd3-984b-0c153b6927ca.png">

However, in practice, most information shared by collaborators is largely irrelevant to the final perception, making it challenging to identify distant and occluded objects. To address this issue, we propose a novel collaborative framework, named  Semantic Aware Heterogeneous Network (SAHNet), which shares and fuses perceptually crucial and useful information among heterogeneous collaborators to improve the performance of 3D object detection. Specifically, we firstly design Foreground and Boundary Feature Selection (FBFS) to enhance meaningful feature extraction. A Heterogeneous Feature Transfer module (HFF) is then proposed to consider collaborators'  heterogeneity to better transfer perception-critical features. Finally, we put forward a Semantic Feature Fusion module (SFF) that effectively aggregates features using semantic information. 




https://github.com/HuangZhe885/Collaborative-Perception/assets/44192081/2a860911-ee6f-44b6-ab13-17cf3e4aacad



# METHOD
* The essential problem in intermediate fusion-based collaborative perception is to allow multiple collaborators to share perceived features via communication networks to promote each agent's perception capability.  
However, the majority of the features perceived by  each agent are not relevant for object detection. 
For communication efficiency and object detection accuracy, we focus on maximizing each agent's perception capacity by selecting, transferring, and fusing the most important information.

<img width="633" alt="image" src="https://github.com/HuangZhe885/Collaborative-Perception/assets/44192081/2ad6faf9-edeb-4f47-8bb0-5091be057b48">


* For the 3D object detection in the collaborative perception, we need to focus on valuable features.  In such a process, it is crucial to consider  both foreground and boundary features because the literature has shown that they are essential to object classification and localization. To address this issue, we propose a lightweight foreground boundary attention module.  

* In a collaborative perception system, each collaborator has its own distinct characteristics. Their sensors, for example, will be affected by factors such as hardware quality and acquisition parameters,  impacting the quality of the output 3D point cloud. Besides, there are generally two different types of agents in collaborative perception system: infrastructure (road-side sensing system) and autonomous vehicles (AV). Each of them can share perceptive information with other agents, providing multiple viewpoints for the same scene. However, it is important to note that an infrastructure's  LiDAR installations are positioned at elevated locations, having  a broader field of view with minimal occlusions, while onboard LiDAR can provide more detailed information about the surrounding environment. In order to encode this kind of  heterogeneity during the transmission process, we propose a heterogeneous feature transfer module (HFF) that incorporates the types of collaborators into consideration.
<img width="316" alt="image" src="https://github.com/HuangZhe885/Collaborative-Perception/assets/44192081/e19ff0fe-1345-4ab2-9a16-fb07e506cc2c">

# RESULTS
We evaluate the effectiveness of the proposed AEV2V on  the V2V perception dataset V2XSet. 

<img width="50%" alt="image" src="https://github.com/HuangZhe885/Collaborative-Perception/assets/44192081/1441ef0d-d7bf-47b4-bb63-a6edc9e97ba5">
<img width="50%" alt="image" src="https://github.com/HuangZhe885/Collaborative-Perception/assets/44192081/dd1360e2-317d-4c65-bb39-7927cbbd3c50">

* Component ablation study
<img width="50%" alt="WechatIMG209" src="https://user-images.githubusercontent.com/44192081/232229935-f1d5c328-ef78-4b31-8819-f2c81434bb11.jpeg">
* Major components comparisons of collaborative perception systems.
<img width="50%" alt="WechatIMG209" src="https://user-images.githubusercontent.com/44192081/232230105-032371c8-9d80-46e8-9066-f05b40817916.jpeg">

# Visualization of collaboration

<img width="70%" alt="WechatIMG214" src="https://user-images.githubusercontent.com/44192081/232230149-82dd9560-3fcf-4168-9925-80b48c120b7c.png">
<img width="70%" alt="WechatIMG214" src="https://user-images.githubusercontent.com/44192081/232230167-bc661a63-bdb7-451c-b62f-fa0f82164e9b.png">

# CONCLUSION

We porpose AEV2V, a novel detection-efficient collaborative perception framework. Our main contributions include the spatical-semantic attention model for extracting  dilated spatial confidence map at each agent to promote pragmatic compression; we also propose a Confidence Fused axial attention (Co-FAX) method that can handle the information fusion of multi-agents and multi-views. It not only implements a combination of global and local attention methods in the high-dimensional feature space, but it also makes use of essential information from the upstream network for more focused fusion. To alleviate the misalignment between the localization accuracy and classification confidence, we design the confidence-aware IoU rectification module for post-processing the confidence. Extensive experiments on simulated  datasets  show that AEV2V achieves superior performance on multi-agent cooperative 3D object detection.

