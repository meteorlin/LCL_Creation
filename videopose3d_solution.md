* videopose.py[inference_video()]：设置后面用于videopose3d的各项超参数。
* videopose.py[get_detector_2d()]：返回包含2d检测器的字典。
* 检查初始传入的参数，若其中的`input_npz`参数为空，即之前没有对视频进行检测，则`if not args.input_npz`为真，则会使用前文所选的2d检测器进行2d关键点推导，
否则就加载对应的npz文件。

---

至此2d检测器任务完成

---

**定义关节的相关位置和顺序**

* 由于人体关键点是对称的，需要将其分离开：`keypoint_symmetry`即“关键点对称”，其中包含的是关键点的对称序号；
* 再将`keypoint_symmetry`分成左右一对关键点`kps`(keypoints)；
* 而后再指定关节点。

**根据相机的参数对关键点进行正则化**

* 这里使用的函数是“正则化屏幕坐标”`normalize_screen_coordinates`，作用是：“标准化关键点，使[0，w]映射到[-1,1]，同时保留纵横比”。
* 此处的三个参数分别代表：
    * （1）关键点<此处因为未研究所以不知道是什么内部结构>；
    * （2）w：画面宽；
    * （3）h：画面长。

---

下面进行3d姿态推导（temporal model：时间模型）

---

