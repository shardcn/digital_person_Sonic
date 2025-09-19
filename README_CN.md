## 搭建环境
conda create -n v3.12.7_sonic python=3.12.7
conda activate v3.12.7_sonic

pip install -r requirements.txt
pip install opencv-python

## 下载模型
python -m pip install "huggingface_hub[cli]"
huggingface-cli download LeonJoe13/Sonic --local-dir checkpoints
huggingface-cli download stabilityai/stable-video-diffusion-img2vid-xt --local-dir checkpoints/stable-video-diffusion-img2vid-xt
huggingface-cli download openai/whisper-tiny --local-dir checkpoints/whisper-tiny

## 命令行
python demo.py \
'examples/image/anime1.png' \
'examples/wav/sing_female.wav' \
'examples/results/anime1-sing_female.mp4'


## web界面
python3 gradio_app.py