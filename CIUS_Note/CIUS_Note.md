# 基本架构
输入image像素为1280 × 720，输出数据为一个graph，其node为障碍物的种类（type1、type2......）,edge为不同障碍物之间的关系（e.g.汽车在马路上移动，树在马路上静止，A在B前、后、左、右、上、下）。该graph的目的是使得栅格地图的更新更加迅速，增强鲁棒性。
## 模型搭建：
**Key idea: 利用Graph数据类型搭建image图像和点云处理结果的联系，使其make sense**
  1. image -> GCN -> graph, node：卷积后的分割结果；edeg：各部分的邻接关系 (ongoing)
  2. pointcloud -> graph -> GNN -> graph
  3. image + pointcloud -> map with label -> 更好的决策









mnist GNN进行graph层面的分类





## Tips
- `trainloader = DataLoader(train_dataset, batch_size=64, shuffle=True, num_workers=2)`中，trainloader 是PyTorch中的一个常见变量名，通常表示训练数据的加载器 (DataLoader),主要作用是从一个数据集（Dataset）中加载数据，并按批次（batch）提供给模型进行训练。num_workers为线程数
- 