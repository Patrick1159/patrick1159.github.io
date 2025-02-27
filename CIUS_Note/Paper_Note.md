# 目录
1. <a href="#paper1"> Large-scale Point Cloud Semantic Segmentation with Superpoint Graphs </a> <!--注意在引用时前面要加"#"-->
2. <a href="#paper2"> SEMI-SUPERVISED CLASSIFICATION WITH GRAPH CONVOLUTIONAL NETWORKS
3. <a href="#paper3"> Relationformer: A Unified Framework for **Image-to-Graph** Generation
4. Vision GNN

# Large-scale Point Cloud Semantic Segmentation with Superpoint Graphs
<a id="paper1"> paper1 </a>

## Introduction
- Challenges: Scale of data; lack of clear structure akin to the regular grid arrangement in images -> CNN performs badly
- Previous attempts:
  1. replicate successful CNNs: SnapNet(3D pointcloud -> RGBD image) 需要进行表面重建，丢失信息。
  2. SegCloud: 3D convolutions on voxel grid 效率低下。
  3. Conclusion: do not capture the **inherent structure** of 3D pcl.,  limited preformance
- Propose: representation of large 3D point clouds as a **collection of interconnected simple shapes coined super points**(superpoint graph: SPG). SPG is an *attributed directed graph 属性有向图*：
  - Nodes: simple shapes
  - Edges: adjacency relationship characterized by edge 
- Advantages: 
  - considers entire object parts *as whole* instead of single points/voxels
  - ability to describe the *relationship between adjacent objects* for contextual classification, e.g. cars are generally above roads, ceilings are surrounded by walls
  - size of SPG is defined by the number of simple structures in a scen
- Composation:
  1. superpoint embedding: Point-Nets
  2. contextual segmentation: GCN(novel Edge Conditioned Convolutions + Gated Recurrent Units)





# SEMI-SUPERVISED CLASSIFICATION WITH GRAPH CONVOLUTIONAL NETWORKS
<a id="paper2"> paper2 </a>



# Relationformer: A Unified Framework for **Image-to-Graph** Generation
<a id="paper3"> paper3 </a>
Key idea:
- 引入[rln]-token，和[obj]-token共同通过一系列的相互关联，利用图像中的局部和全局语义推理。
- Nodes: objects；Edges：nutual dependencies, semantic-relations
- 基于Transformer，暂时不看


# Vision GNN