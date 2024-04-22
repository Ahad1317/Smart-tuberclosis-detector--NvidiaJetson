# Smart Tuberculosis Detection with NVIDIA Jetson Nano 🚀

![Smart Psio (1)](https://github.com/Ahad1317/Smart-tuberclosis-detector--NvidiaJetson/assets/96586030/ac90ea47-1f17-4065-a39e-d25126329e5c)

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
  
- clone the repository 
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
  -- **Download here**: [Dataset](https://www.kaggle.com/datasets/mohamedhanyyy/chest-ctscan-images)
```
python/training/classification/data
```
- **In same folder create label.txt containing the label "Tuberculosis"**
## Conclusion 📜

In conclusion, this project not only aims to provide a technological solution to a complex medical problem but also strives to make healthcare more accessible and efficient. Through the use of cutting-edge technology like the NVIDIA Jetson Nano, Smart tuberuclosis Detection has the potential to transform how psoriasis is managed and treated, improving the quality of life for millions of patients worldwide.

---

Feel free to star and fork this repository if you find this project interesting!
