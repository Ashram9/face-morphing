# face-morphing
人脸融合 face-morphing

实现步骤：
1. Landmark Detection: 通过特征点检测器(dlib)，找到起始图像和目标图像中的对应面部特征点；
2. Triangulation: 使用Delaunay算法确保三角形剖分的一致性；
3. Intermediate Image Coordinates Interpolation: 线性插值计算所有中间图像的顶点坐标；
4. Affine Transformation: 对于每对对应的三角形，使用三个对应的顶点估算仿射变换参数；
5. Bilinear Interpolation: 双线性插值计算像素值大小；
6. Blending Images: 通过参数控制图像混合比例，实现平滑过渡效果；
7. Creating a Video: 使用ffmpeg将所有生成的中间帧合成为视频。
