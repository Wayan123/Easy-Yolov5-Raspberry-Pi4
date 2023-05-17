![Screenshot from 2023-05-16 21-50-03](https://github.com/Wayan123/Yolov5-Raspberry-Pi4/assets/17795544/3b764890-7727-451a-8f56-f6a5fb1647ba)

# Easy Yolov5-Raspberry-Pi4
Tutorial menjalankan Yolov5 di Raspberry Pi 4 dengan mudah.

Tutorial lainnya silakan kunjungi youtube berikut: https://www.youtube.com/@codeandrobotid2466

- Adapun alat-alat yang diguanakan:
1. Raspberry Pi 4 Model B dengan 2 GB RAM atau lebih,
2. Webcam Logitech 720P,
3. SD Card minimal 16 GB atau lebih.

- Langkah-langkah menginstall Raspberry Pi OS:
1. Download Raspberry Pi Imager disini https://www.raspberrypi.com/software/. Software ini akan digunakan untuk meng-install OS Pi pada SD Card/Flashdisk/USB SSD
2. Pytorch membutuhkan arsitektur Raspbian 64 bit, jadi pilih OS Raspbian 64 Bit, jangan menggunakan versi 32 bit karena akan gagal selama install pytorch.
3. Versi python yang digunakan adalah 3.9.

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
2. Atau mengguanakan cara kedua pada gambar berikut,
![image](https://github.com/Wayan123/Yolov5-Raspberry-Pi4/assets/17795544/3b8c7462-8379-4884-ab74-e82f37c44f8d)
3. Atau bisa tes dengan kode yang sudah disediakan dengan mengetik $ python pytorch-test.py atau seperti pada gambar,
![image](https://github.com/Wayan123/Yolov5-Raspberry-Pi4/assets/17795544/93f835e9-445f-412f-867f-3082ae176e7f) 
5. Jika tidak ada yang error dan muncul seperti pada gambar berarti proses install sudah berjalan dengan baik.

- Install Yolov5:
1. Cloning repository yolov5 berikut https://github.com/ultralytics/yolov5.git dengan ketik $ git clone https://github.com/ultralytics/yolov5.git
2. cd yolov5
3. pip install -r requirements.txt
4. Jika tidak ada error proses instalasi selesai.

- Langkah terakhir jalankan streaming yolov5 menggunakan webcam:
1. Kita akan menggunakan model nano yolov5n.pt agar lebih ringan, ukuran gambar kita kecilkan menjadi 224 agar bisa mendapatkan frame lebi cepat atau bisa juga menggunakan ukuran standar 640. Ketik kode berikut pada terminal $ python detect.py --weights yolov5n.pt --imgsz 224 --conf 0.25 --source 0, source 0 menandakan kita menggunakan webcam logitech. Lebih jelasnya seperti pada gambar berikut:
![image](https://github.com/Wayan123/Yolov5-Raspberry-Pi4/assets/17795544/e12fba57-9333-433f-98d3-303227190a20)
3. Hasilnya sebagai berikut jika tidak ada error:
![Screenshot from 2023-05-16 21-50-03](https://github.com/Wayan123/Yolov5-Raspberry-Pi4/assets/17795544/715d858b-b740-4df8-8002-e69b1c6cc2dd)
3. Selamat yolo anda berhasil terinstall dan bisa berjalan dengan baik.
