## LLM 환경 구성 단계
- Ubuntu 22.04 LTS 사용
- nvidia 3060 TI 8GB 모델 사용
- python 3.11 이상

#### 필수 소프트웨어 설치
  - CUDA 및 NVIDIA 드라이버
    - 최신 NVIDIA 드라이버와 CUDA를 설치하여 GPU 가속을 활성화합니다.

```bash
sudo apt update
sudo apt install nvidia-driver-525
```

 - Python 및 PyTorch
   - PyTorch는 GPU 지원 버전으로 설치합니다.

```bash
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```

  - 양자화 도구 설치
    - transformers와 bitsandbytes 라이브러리를 설치합니다.

```bash
pip install transformers bitsandbytes accelerate
```

모델 다운로드
Hugging Face에서 DeepSeek-R1-Distill-Llama-8B 모델을 다운로드합니다.

bash
git lfs install
git clone https://huggingface.co/deepseek-ai/DeepSeek-R1-Distill-Llama-8B