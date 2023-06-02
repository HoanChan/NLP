# Môn học: Xử lý ngôn ngữ tự nhiên

Giảng viên: TS. Hoàng Thanh Tùng - 1990

Các bước thực hiện

Bước 1: Kiểm tra GPU NVIDIA có phù hợp CUDA không?  https://developer.nvidia.com/cuda-gpus Theo hardware requirement > 3.5 trở lên

Bước 2: Gỡ cài đặt toàn bộ drive NVIDIA trên máy và Cài đặt CUDA và cuDNN phù hợp tại 2 link sau https://developer.nvidia.com/cuda-toolkit-archive và https://developer.nvidia.com/rdp/cudnn-archive

CuDNN là thư viện hỗ trợ Deep Learning trên GPU, việc cài đặt cuDNN chỉ đơn giản là giải nén rồi copy vào folder cài đặt CUDA là được. 
Với CUDA 11.2 thì copy các file vào C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.2

Bước 3: Tạo mới môi trường Anacoda và cài đặt pytorch bằng lệnh

`pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118`

Bước 4: Kiểm tra pytorch có nhận GPU không?

``` python
import torch

if torch.cuda.is_available():
    print("PyTorch is using GPU.")
    device = torch.device("cuda")  # Chọn GPU làm thiết bị tính toán
    print(f"Current GPU device: {torch.cuda.current_device()}")
    print(f"Number of available GPUs: {torch.cuda.device_count()}")
else:
    print("PyTorch is using CPU.")
    device = torch.device("cpu")  # Chọn CPU là thiết bị tính toán
```