# LCL_Creation

- [x] 学习Python
- [x] 学习Pytorch
- [x] 从Posenet中导出单帧人体关键点坐标
- [x] 解析VideoPose3D
- [ ] 解析Posenet控制中输入摄像头的方法，并将其暂时替换成输入视频以便于测试。
- [ ] 解析video-pose-3d-China中对AplhaPose关键点的处理方法并将其套用到PoseNet的输出上
**决定使用网络直接导入js模型而不是使用本地识别，虽然有一个poseformobile的项目但是有点局限而且不好扩展，如果以后有必要可以尝试一下这个项目。（有一个posenet-python的项目，我已经装配好了，并且使用的是video-pose-3d-China的virtualenv环境，但是目前看来效果太差）**
- [ ] 将Posenet接入到VideoPose3D中
- [ ] 将VideoPose3D修改为实时运行
- [ ] 由于计算效率和应用场景问题，如果是应用于自拍上，我认为可以只识别上半身以减少运算量。
- [ ] 尝试将Openpose的手部和脸部模型转移到tensorflow上
- [ ] 学习Tensorflow及其Mobile版本
- [ ] 将Posenet和VideoPose3D的Pytorch模型转接到TensorflowMobile上
- [x] 
