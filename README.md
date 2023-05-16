# Yolov5-Raspberry-Pi4
Tutorial menjalankan Yolov5 di Raspberry Pi 4 dengan mudah.

- Adapun alat-alat yang diguanakan:
1. Raspberry Pi 4 Model B dengan 2 GB RAM atau lebih,
2. Webcam Logitech 720P,
3. SD Card minimal 16 GB atau lebih.

- Langkah-langkah menginstall Raspberry Pi OS:
1. Download Raspberry Pi Imager disini https://www.raspberrypi.com/software/. Software ini akan digunakan untuk meng-install OS Pi pada SD Card/Flashdisk/USB SSD
2. Pytorch membutuhkan arsitektur Raspbian 64 bit, jadi pilih OS Raspbian 64 Bit, jangan menggunakan versi 32 bit karena akan gagal selama install pytorch.

- Langkah-langkah install Pytorch pada OS Raspbian 64 Bit:
1. sudo apt update
2. sudo apt upgrade -y
3. sudo apt-get -y install python3-pip libjpeg-dev libopenblas-dev libopenmpi-dev libomp-dev
4. pip install torch torchvision torchaudio
5. pip install opencv-python
6. pip install numpy --upgrade
7. Jika tidak ada error proses install selesai.

- Testing pytorch apakah sudah terinstall dengan benar atau belum:
1. Ketik berikut pada terminal $ python -c "import torch; print(torch.__version__)", atau
![image](https://github.com/Wayan123/Yolov5-Raspberry-Pi4/assets/17795544/7df91399-cb2d-49e9-8b84-46139f164ad4)
2. 
