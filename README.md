# Tennis AI Mainland

本项目是一个面向中国大陆用户的网球视频分析AI工具，**无需翻墙即可使用**。本仓库对依赖和模型下载做了适配，方便在国内环境下顺利运行。

## 项目简介
本项目旨在通过深度学习和计算机视觉技术，对网球比赛视频进行自动分析，包括球员追踪、球轨迹检测、场地线识别、数据统计等。


## 模型文件
链接: https://pan.baidu.com/s/1sG9e-lX9HnhfWXxao7XaWA?pwd=1y6q 提取码: 1y6q


## 主要模块说明

- `app/tennis_analysis/`
  - **main.py**：主程序入口，串联各个分析模块，完成视频的读取、分析、结果输出。
  - **yolo_inference.py**：基于YOLO模型进行目标检测的推理脚本。
  - **trackers/**：
    - `player_tracker.py`：球员检测与追踪。
    - `ball_tracker.py`：网球检测与追踪。
  - **court_line_detector/**：
    - `court_line_detector.py`：场地线检测与关键点识别。
  - **mini_court/**：
    - `mini_court.py`：小场地映射与可视化。
  - **utils/**：
    - `video_utils.py`：视频的读取与保存。
    - `bbox_utils.py`、`conversions.py`、`player_stats_drawer_utils.py`：辅助工具函数。
  - **constants/**：存放常量配置。
  - **training/**：模型训练相关数据与脚本。
  - **output_videos/**：输出分析后的视频。
  - **input_videos/**：输入待分析的视频。
  - **runs/**、**tracker_stubs/**、**models/** 等：存放模型、缓存、运行结果等。

## 依赖环境
请参考 `requirements.txt` 安装依赖。

## 适用人群
- 中国大陆AI开发者、网球爱好者、体育数据分析师
- 无需科学上网即可完整体验

## 快速开始
```bash
# 创建并激活虚拟环境
python3 -m venv tennis_ai_env
source tennis_ai_env/bin/activate

# 安装依赖
pip install -r requirements.txt

# 运行主程序
cd app/tennis_analysis
python main.py
```

声明：本项目仅为学习目的

项目原仓库地址：https://github.com/abdullahtarek/tennis_analysis
项目代码逐行复现视频：https://www.youtube.com/watch?v=L23oIHZE14w&t=14900s
感谢abdullahtarek创建的运动视频分析代码库