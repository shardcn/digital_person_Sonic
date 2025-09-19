conda create -n v3.12.7_sonic python=3.12.7
conda activate v3.12.7_sonic

pip install -r requirements.txt
pip install opencv-python

python3 demo.py \
'examples/image/anime1.png' \
'examples/wav/sing_female.wav' \
'examples/results/anime1-sing_female.mp4'

python demo.py \
'examples/image/anime1.png' \
'examples/wav/sing_female.wav' \
'examples/results/anime1-sing_female.mp4'
