# 复现论文《A Novel Algorithmic Structure of EEG Channel Attention Combined with Swin Transformer for Motor Patterns Classification》



## 摘要

本工作旨在复现 Wang 等人提出的基于 Swin Transformer 的脑电通道注意力算法,  验证其在运动想象分类任务中的有效性。尽管未能完全重现原文的结果,但 Swin Transformer 在运动想象分类中的潜力仍然得到了验证。针对实验中遇到的问题,未来工作将聚  焦于优化数据预处理流程、调整模型架构、以及引入数据增强技术等方面,以进一步提升  分类效果和模型的鲁棒性。

## 依赖

*   python 3.8.0
*   CUDA 12.4

安装其他依赖：

```bash
pip install -r requirements.txt
```

## 数据集

An EEG motor imagery dataset for brain computer interface in acute stroke patients. For more detail, please refer to following information.

    - Author: Haijie Liu et al.
    - Year: 2024
    - Download URL: https://figshare.com/articles/dataset/EEG_datasets_of_stroke_patients/21679035/5
    - Reference: Liu, Haijie, et al. "An EEG motor imagery dataset for brain computer interface in acute stroke patients." Scientific Data 11.1 (2024): 131.
    - Stimulus: A video of gripping motion is played on the computer, which leads the patient imagine grabbing the ball. This video stays playing for 4 s. Patients only imagine one hand movement.
    - Signals: Electroencephalogram (30 channels at 500Hz sample rate,. Electrooculography (including horizontal and vertical EOG) (totally 50 participants).
    - label: left hand and right hand.
    
    In order to use this dataset, the downlowd root path is required, containing the following files and directories:
    
    - sourcedata (dir)
    - edffile (dir)
    - task-motor-imagery_events.tsv
    - ...

## 运行

运行workpipe.py文件：

```bash
python workpipe.py
```
