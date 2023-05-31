# Môn học: Xử lý ngôn ngữ tự nhiên

Giảng viên: TS. Hoàng Thanh Tùng - 1990

Các bước thực hiện

Bước 1: Xác định phiên bản CUDA và cuDNN phù hợp với phiên bản Tensorflow: https://www.tensorflow.org/install/source#gpu.  

Tiếp tục tìm phiên bản CUDA và cuDNN phù hợp tại 2 link sau https://developer.nvidia.com/cuda-toolkit-archive và https://developer.nvidia.com/rdp/cudnn-archive

Bước 2: kiểm tra GPU NVIDIA có phù hợp với Tensorflow và CUDA không?  https://developer.nvidia.com/cuda-gpus Theo hardware requirement của Tensorflow thì support 3.5 trở lên

Bước 3: cài đặt CUDA https://developer.nvidia.com/cuda-toolkit-archive

Bước 4: cài đặt cuDNN. 

CuDNN là thư viện hỗ trợ Deep Learning trên GPU, việc cài đặt cuDNN chỉ đơn giản là giải nén rồi copy vào folder cài đặt CUDA là được. 
Với CUDA 11.2 thì copy các file vào C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.2
https://developer.nvidia.com/rdp/cudnn-download

Bước 5: cài đặt `pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118`

Bước 6: kiểm tra tensorflow-gpu có nhận GPU không?