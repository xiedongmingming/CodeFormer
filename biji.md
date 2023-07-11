# 环境搭建

1. 安装依赖：除了REQUIREMENTS.TXT中的依赖项之外还需执行如下命令
```
python basicsr/setup.py develop
```

```
!python inference_codeformer.py 
    -w $CODEFORMER_FIDELITY 
    --input_path inputs/user_upload 
    --bg_upsampler realesrgan 
    --face_upsample
```
- CODEFORMER_FIDELITY：平衡质量(低数字)和保真度(高数字)
- BACKGROUND_ENHANCE：用REAL-ESRGAN增强背景图像
- FACE_UPSAMPLE：为高分辨率人工智能创建的图像上采样恢复人脸

支持输入文件夹：
```
!python inference_codeformer.py 
    -w $CODEFORMER_FIDELITY 
    --input_path inputs/whole_imgs 
    --bg_upsampler realesrgan
```

直接处理对齐的脸？？？
```
!python inference_codeformer.py 
    -w $CODEFORMER_FIDELITY 
    --has_aligned 
    --input_path inputs/cropped_faces
```
