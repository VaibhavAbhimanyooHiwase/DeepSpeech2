# DeepSpeech2
Python3 installation and complete setup only for prediction of Baidu's deep speech 2 model.

Implementation of DeepSpeech2 architecture for ASR. It is an open-source
implementation of end-to-end Automatic Speech Recognition (ASR) engine, based on
Baidu&#39;s Deep Speech 2 paper, with PaddlePaddle platform. Biadu’s pre-trained model for
English is used for inference.

# System Requirements:
OS: Ubuntu 16.04.5 LTS
Language: Python3 and Bash
Database: None

# Tools:
PaddlePaaddle
SoundFile
Efficient Signal Resampling
Python Speech Feature extraction

# Packages:
List of Python packages has been attached in requirements.txt

# Environment setup

## Folders setup
sh folder_setup.sh

OR

git clone https://github.com/PaddlePaddle/DeepSpeech/
cd DeepSpeech/
mkdir checkpoints
cd checkpoints/
mkdir baidu
cd baidu/
mkdir step_final/
cd step_final/
cd .. 
cd .. 
cd ..
cd models/
cd baidu_en8k/
sh download_model.sh
cd ..
cd ..
cp -p models/baidu_en8k/params.pdparams checkpoints/baidu/step_final/params.pdparams
cp -p ../data_utils/audio.py ../DeepSpeech/data_utils/audio.py
cp -p ../data_utils/data.py ../DeepSpeech/data_utils/data.py
cp -p ../data_utils/utility.py ../DeepSpeech/data_utils/utility.py
cp -p ../model_utils/model.py ../DeepSpeech/model_utils/model.py
cp -p ../utils/utility.py ../DeepSpeech/utils/utility.py
cp -p ../utils/error_rate.py ../DeepSpeech/utils/error_rate.py
cp -p ../decoders/swig_wrapper.py ../DeepSpeech/decoders/swig_wrapper.py
cp -p ../swig_decoders.py ../DeepSpeech/swig_decoders.py
cp -p ../_swig_decoders.py ../DeepSpeech/_swig_decoders.py
cp -p ../_swig_decoders.cpython-35m-x86_64-linux-gnu.so ../DeepSpeech/_swig_decoders.cpython-35m-x86_64-linux-gnu.so
cp -p ../create_manifest.py ../DeepSpeech/create_manifest.py
cp -p ../infer_deepspeech2_baidu.py ../DeepSpeech/infer_deepspeech2_baidu.py
cp -p ../models/lm/download_lm_en.sh ../DeepSpeech/models/lm/download_lm_en.sh
cp -p ../deploy/demo_server.py ../DeepSpeech/deploy/demo_server.py
cp -p ../deploy/demo_client.py ../DeepSpeech/deploy/demo_client.py
mkdir test_dataset
cp -r ../vaibhav_data_test_wav16k/ ../DeepSpeech/test_dataset/vaibhav_data_test_wav16k/
cd data
mkdir baidu_en8k/
cd ..
cd models/lm
sh download_lm_en.sh
cd ../..


## Utilities setup

Either run required_packages.sh 

OR

sudo apt-get install python3-pip
sudo python3 -m pip install paddlepaddle

## Libraries setup

sudo python3 -m pip install -r requirements.txt

OR

sudo python3 -m pip install scipy==1.2.1
sudo python3 -m pip install SoundFile==0.9.0.post1
sudo python3 -m pip install resampy==0.1.5
sudo python3 -m pip install python_speech_features

## Other steps

Replace </data_utils/utility.py> from repo
