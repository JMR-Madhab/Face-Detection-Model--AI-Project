# Face-Detection-Model--AI-Project
A Python-based attendance system using face detection and recognition. The project leverages OpenCV and deep learning for real-time face identification, simplifying and automating the process of recording attendance in classrooms, offices, or events.


**Features**
- Automatic face detection using Haar Cascade classifiers.

- Real-time face recognition powered by a deep learning model.

- Attendance marking based on recognized faces.

- Support for streaming video sources (e.g., IP cameras).


**Project Structure**
- collect_data.py: Captures facial data from a video stream, detects faces, and saves face images for training.

- consolidated_data.py: Processes saved face images, converts them into numerical arrays, and serializes both images and corresponding labels using pickle for model training.

- recognize.py: Performs real-time face recognition, displays predictions on-screen, and marks attendance using the trained model.

- haarcascade_frontalface_default.xml: Pre-trained XML file for frontal face detection using Haar Cascades.

**Setup Instructions**
1. Clone the repository:
   git clone https://github.com/yourusername/face-detection-attendance.git
   cd face-detection-attendance

2. Install dependencies:

  - Python 3.x

  - OpenCV (pip install opencv-python)

  - NumPy (pip install numpy)

  - Keras (pip install keras)

  - Matplotlib (pip install matplotlib)

3. Collect Training Data:

  Run collect_data.py to collect 100 face samples per user. Enter the person's name when prompted.

4. Prepare Data for Training:

  Use consolidated_data.py to convert face images and labels into serialized files required for model training.

5. Train a Recognition Model:

  - Develop and train your own recognition model (not included here) or adapt the provided workflow.

  - Ensure the model is saved as model.h5 in the repository directory.

6. Run Real-Time Recognition:

  Start recognize.py to detect and recognize faces from a live video stream, marking attendance for recognized individuals.


**Usage**
- Data Collection: Point your webcam or IP camera to the participant, run the collection script, and follow the on-screen instructions.
- Recognition & Attendance: After successful training and model installation, the recognition script will automatically identify faces and log attendance.

**Credits**
- Built using OpenCV and Keras.
- Haar Cascade classifier (haarcascade_frontalface_default.xml) from OpenCV package.


**Customization**
- Adding User Labels: Edit the labels list in recognize.py to match your participants’ names.
- Camera Source: Change the URL variable in collect_data.py and recognize.py as per your camera's live feed address.


