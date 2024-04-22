# Smart Tuberculosis Detection with NVIDIA Jetson Nano 🚀

![Smart Psio (2)](https://github.com/Ahad1317/Smart-tuberclosis-detector--NvidiaJetson/assets/96586030/1b26afb1-2095-42e3-bd5a-f43e7f3987fc)

## Abstract 📄
This project harnesses the NVIDIA Jetson Nano to develop a sophisticated, real-time tuberculosis detection system utilizing advanced deep learning and image processing techniques. This innovative solution aims to aid in the early detection and monitoring of tuberculosis, offering a non-invasive, transformative approach to managing this respiratory disease.

## Objective 🎯
The main goal is to develop a reliable and accessible tuberculosis detection system for use in both clinical and home settings. This technology seeks to empower patients and healthcare providers with improved capabilities for the early detection and management of tuberculosis.

## Existing System: Challenges 😰
Current diagnostic methods for tuberculosis rely heavily on sputum analysis and chest X-rays, which are not only invasive but also have several limitations:
- **Diagnostic Delays**: Lengthy lab results can delay treatment.
- **Accessibility Issues**: Limited access to advanced medical facilities in remote areas.
- **Cost and Resource Intensive**: High costs and significant healthcare infrastructure required.

## Proposed System 🌟
The proposed system includes:
- **Automated Detection**: Using deep learning algorithms to identify tuberculosis indicators from chest X-ray images.
- **Real-Time Analysis**: Instant feedback facilitated by the NVIDIA Jetson Nano's robust processing power.
- **User-Friendly Interface**: Easy-to-use interface for both patients and healthcare professionals.

## Software Requirements 🛠️
- Python 3.8 or higher
- TensorFlow 2.x
- OpenCV for image processing
- NVIDIA JetPack SDK
- Additional dependencies can be found in `requirements.txt`

## Application 🌍
The system can be utilized in various settings:
- **Home Monitoring**: Allows patients to perform regular health check-ups.
- **Clinical Assistance**: Assists healthcare professionals in making more accurate diagnoses.
- **Research**: Supports ongoing research and data collection on tuberculosis.

## System Requirements 🖥️
- **NVIDIA Jetson Nano**: Primary computing device.
- **High-resolution camera module**: For capturing chest X-ray images.
- **Adequate lighting conditions**: Essential for high-quality image capture.
- **memory card**
- **card reader**
- **other setups**: follow the hardwarw setup section

## Setup and Installation
1. **Hardware Setup**:
      - Ensure the setup is in a well-lit area.
      - Here is jetson connection setup :

      ![jetson setup](https://github.com/Ahad1317/Smart-tuberclosis-detector--NvidiaJetson/assets/96586030/36da2479-1eec-4919-ade9-ec2ada96436d)

## Follow these commands for software installation and working :

- Open terminal
  
- clone the repository and open directiry in terminal
```bash
git clone https://github.com/Ahad1317/Smart-tuberclosis-detector--NvidiaJetson
```
- run docker container (enter jetson password)
```
docker/run.sh
```
- check if model has installed properly(camera will run)
```
video-viewer /dev/video0
```
- **Now download the dataset and paste into**
  -- **Download here**: [Dataset](https://www.kaggle.com/jtiptj/chest-xray-pneumoniacovid19tuberculosis/download)
```
python/training/classification/data/xray
```
- **In same folder create labels.txt containing the label "Tuberculosis"**
  
- Train xray dataset
```
python3 train.py --model-dir=models/xray --batch-size=4 --workers=1 --epochs=35 data/xray
```

- export the trained model in onnx file
```
python3 onnx_export.py --model-dir=models/xray
```
### Testing

- open the repo directly in terminal

- run docker docker/run.sh

- change directory
```
cd python/training/classification
```

- to test:
```
imagenet --model=models/xray/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=data/xray/labels.txt data/Project/Test02/Input/mix data/Project/Test02/Output
```
- For webcam based detection
```
imagenet --model=models/xray/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=data/xray/labels.txt /dev/video0
```


## Conclusion 📜

In conclusion, this project not only aims to provide a technological solution to a complex medical problem but also strives to make healthcare more accessible and efficient. Through the use of cutting-edge technology like the NVIDIA Jetson Nano, Smart tuberuclosis Detection has the potential to transform how psoriasis is managed and treated, improving the quality of life for millions of patients worldwide.

---

Feel free to star and fork this repository if you find this project interesting!
