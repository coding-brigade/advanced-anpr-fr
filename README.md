# Advance ANPR And FRS Solution

**A surveillance system powered by machine learning and deep learning that integrates Automatic Number Plate Recognition (ANPR) and Facial Recognition System (FRS) to enhance traffic law enforcement in India through real-time offender identification, automated challan processing, and centralized analytics.**

## Table of Contents

- [Advance ANPR And FRS Solution](#advance-anpr-and-frs-solution)
  - [Table of Contents](#table-of-contents)
  - [Acknowledgement:](#acknowledgement)
  - [Problem Statement](#problem-statement)
  - [Objectives \& Vision](#objectives--vision)
    - [Objectives](#objectives)
    - [🌍 Vision](#-vision)
  - [Proposed Solution](#proposed-solution)
    - [System Overview](#system-overview)
      - [End-to-End Intelligent Workflow](#end-to-end-intelligent-workflow)
    - [Implementation Video](#implementation-video)
    - [Key Innovations](#key-innovations)
- [Use Cases \& Scenarios](#use-cases--scenarios)
    - [🚦 Traffic Violation Enforcement](#-traffic-violation-enforcement)
    - [🛡️ Security, Crime Prevention \& Law Enforcement](#️-security-crime-prevention--law-enforcement)
    - [🧑‍🏫 Administrative \& Civil Use Cases](#-administrative--civil-use-cases)
    - [🧠 Governance, Planning \& Smart City Applications](#-governance-planning--smart-city-applications)
    - [🏙️ Ideal Deployment Zones](#️-ideal-deployment-zones)
  - [Dataset \& Preprocessing](#dataset--preprocessing)
    - [🛣️ Phase 1: Real-World Data Acquisition](#️-phase-1-real-world-data-acquisition)
    - [🛠️ Phase 2: Dataset Construction \& Annotation](#️-phase-2-dataset-construction--annotation)
      - [📌 ANPR (Automatic Number Plate Recognition)](#-anpr-automatic-number-plate-recognition)
      - [📌 FRS (Facial Recognition System)](#-frs-facial-recognition-system)
    - [🔧 Phase 3: Preprocessing \& Augmentation Pipeline](#-phase-3-preprocessing--augmentation-pipeline)
      - [🧹 Preprocessing Techniques](#-preprocessing-techniques)
      - [🧪 Augmentation Strategies](#-augmentation-strategies)
    - [📊 Data Composition Matrix](#-data-composition-matrix)
  - [Model Training Details](#model-training-details)
    - [🧩 Training Infrastructure](#-training-infrastructure)
    - [📌 ANPR Training](#-anpr-training)
    - [🧠 FRS Training](#-frs-training)
    - [🔄 Combined System Evaluation](#-combined-system-evaluation)
  - [Team \& Roles](#team--roles)
    - [👨‍🏫 Team Mentor](#-team-mentor)
  - [Special Thanks](#special-thanks)
    - [References](#references)

## Acknowledgement:

We, the team "Coding Brigades," extend our sincere gratitude to the Ministry of Education's Innovation Cell, AICTE, along with the Bureau of Police Research and Development (BPR&D) and the Indian Cybercrime Coordination Centre (I4C) under the Ministry of Home Affairs (MHA) for organizing the National Cybersecurity Hackathon – Kavach 2023.

We are especially thankful to our mentor, Dr. Himani Trivedi, for her unwavering guidance and support throughout the journey. We also express our appreciation to our university, Kadi Sarva Vishwavidhyalay, for fostering a nurturing environment that enabled us to ideate, build, and refine our project with the right resources. Finally, we thank Pillai College of Engineering (PCE), Panvel for hosting the event and providing excellent support, accommodation, and hospitality that made the experience truly memorable.

## [Problem Statement](#problem-statement)

The current system of traffic enforcement in India faces multiple inefficiencies. Despite efforts like the "One Nation, One Challan" initiative, there are inconsistencies in challan generation across states, limited automation, and no centralized offender database. Manual monitoring remains error-prone, biased, and incapable of handling modern-day traffic complexities. The absence of real-time offender detection and outdated datasets further hinder effective law enforcement. These issues highlight the urgent need for a smart, scalable, and data-driven traffic surveillance solution.

## [Objectives & Vision](#objectives--vision)

### Objectives

- Design and deploy a real-time surveillance system integrating ANPR and FRS for offender detection and identity verification.
- Extend violation coverage beyond red-light jumping to include:
  - No helmet or seatbelt
  - Driving without a valid license
  - Use of mobile phones while driving
  - Obscured or fake number plates
- Build a **centralized challan generation system** compliant with the “One Nation, One Challan” initiative for national uniformity.
- Strengthen **offender traceability** by linking vehicle data with biometric identity using deep learning models.
- Enable law enforcement with **smart dashboards**, violation heatmaps, and **real-time alerts** for timely intervention.
- Minimize human bias and reduce manual workload by automating detection, recognition, and reporting processes.
- Ensure adaptability of the system across regions, lighting conditions, and occlusion scenarios using robust model training.

### 🌍 Vision

To develop and deploy a **machine learning and deep learning–based traffic surveillance infrastructure** that:

- Promotes **road safety and behavioral accountability** through intelligent, automated enforcement.
- Supports **fair, consistent, and non-discriminatory traffic governance** across all states.
- Empowers law enforcement with **data-driven decision-making tools**, central dashboards, and violation analytics.
- Enables **real-time traceability and evidence-backed enforcement** through integrated biometric and vehicle data.
- Scales nationwide with future integration potential into **Aadhaar, RTO, and law enforcement networks** to support long-term digital governance goals.

## [Proposed Solution](#proposed-solution)


![](/public/architecture.png)


### [System Overview](#system-overview)

Our solution presents a **multi-modal intelligent surveillance architecture** that integrates high-performance computer vision models to automate, authenticate, and enhance traffic law enforcement workflows.

At its core, the system leverages:

- **Automatic Number Plate Recognition (ANPR)** using deep convolutional models (YOLOv8) to localize and extract license plate numbers from real-time CCTV feeds — robust to motion blur, angle distortions, and low-light scenarios.
- **Facial Recognition System (FRS)** powered by pretrained deep learning models to identify and match drivers’ faces, even in the presence of occlusions like helmets, masks, or low-resolution feeds.

The system conducts **contextual violation analysis**, correlates vehicle and identity data, and triggers **automated e-challan generation** using a secure, centralized backend.

#### End-to-End Intelligent Workflow

1. **Surveillance Input**: Real-time CCTV feeds are captured and preprocessed.
2. **Plate Detection & Parsing**: YOLOv8-based ANPR extracts plate data with character segmentation.
3. **Facial Identity Resolution**: Deep FRS modules detect and match the rider’s face against a database.
4. **Violation Recognition**: System detects conditions like no helmet, mobile usage, or fake number plates.
5. **Rule Violation Trigger**: If violation is confirmed, it auto-generates a **digitally signed challan**.
6. **Offender Registry Update**: Records are logged with visual proof, timestamps, and geolocation.
7. **Role-Based Dashboard Notification**: Alerts are pushed to RTO, Police, and Admin portals with violator profiles.

The system is built to be **modular, API-driven, and deployment-ready** for city-wide and national use cases.

### [Implementation Video](#implementation-video)

[Watch the implementation video and GUI of the application](https://drive.google.com/file/d/1sKYhQLe2XFoGAoStt0fGGCqbaGF-jFOB/view?usp=sharing)

---

### [Key Innovations](#key-innovations)

- 🔁 **Bi-Modal Surveillance Fusion**: First-of-its-kind integration of ANPR + FRS ensures dual-entity verification — minimizing false positives.
- 🌐 **Nation-Scale Compatibility**: Fully compliant with the “One Nation, One Challan” framework — ensuring uniformity across states and departments.
- 🧠 **Real-World Adaptive Training**: Trained on handcrafted datasets featuring diverse illumination, occlusion, and multi-angle perspectives to maximize model generalization.
- ⚡ **Fully Autonomous Violation Processing**: Requires zero manual intervention post-deployment — ideal for smart city integration.
- 📊 **Actionable Analytics Interface**: Dynamic dashboards allow authorities to filter violators by region, gender, offense type, and frequency — turning data into decisions.
- 🧩 **Plug-and-Play Modularity**: Clean microservice architecture supports easy integration with Aadhaar, RTO, and central policing databases.
- 🔒 **Cross-Domain Identity Validation**: Synchronizes face recognition with license plate identity to flag mismatches, stolen vehicles, or shared licenses.

# [Use Cases & Scenarios](#use-cases-scenarios)

### 🚦 Traffic Violation Enforcement

- **Helmet & Seatbelt Violation Detection**  
  Identifies riders/drivers not wearing protective gear with facial visibility validation, even under occlusion.

- **Mobile Phone Usage While Driving**  
  Detects improper usage of mobile devices by analyzing spatial hand-face proximity and eye orientation.

- **Unauthorized Driver Identification**  
  Cross-matches driver faces with pre-verified license holders to detect impersonation or unlicensed drivers.

- **Tampered or Fake Number Plate Recognition**  
  Validates number plates against government databases to flag cloned, painted, or manipulated plates.

### 🛡️ Security, Crime Prevention & Law Enforcement

- **Hit-and-Run Offender Reconstruction**  
  Combines timestamped plate and facial data for real-time and post-incident offender tracking.

- **Stolen Vehicle & Watchlist Detection**  
  ANPR scans are instantly matched with the national vehicle crime registry to flag stolen or blacklisted vehicles.

- **Facial Re-identification for Repeat Offenders**  
  FRS helps identify faces recurring across time-stamped events, even in different geographic locations.

- **Snatch-and-Flee or Trespassing Alerts**  
  Cross-verification between rider identity and plate registration enables alerts when mismatched or unauthorized access is detected.

### 🧑‍🏫 Administrative & Civil Use Cases

- **Driving Exam Identity Verification**  
  Prevents impersonation during RTO driving exams by matching live images with applicant data.

- **Automated Entry/Exit Logging for Institutions**  
  Used in campuses, residential gates, and corporate zones for secure access based on identity verification.

- **Violation Frequency Dashboards**  
  Generates behavioral analytics by gender, zone, and frequency—supporting targeted traffic awareness campaigns.

### 🧠 Governance, Planning & Smart City Applications

- **Violation Hotspot Heatmaps**  
  Detects and visualizes clusters of repeated violations to support geo-targeted infrastructure upgrades or patrolling.

- **Traffic Load Analytics**  
  Real-time vehicle flow analysis helps urban planners monitor congestion and optimize signal timings.

- **Integrated Enforcement Intelligence**  
  Bridges vehicle data, biometric identity, and offense history into a central, searchable platform for policy-driven decision making.

### 🏙️ Ideal Deployment Zones

- Urban intersections, smart city grids, and expressways  
- Government transportation checkpoints  
- State-level RTO offices and testing tracks  
- High-security gated areas, university campuses, and metro stations  
- Police surveillance command centers

## [Dataset & Preprocessing](#dataset--preprocessing)

Building a reliable and intelligent surveillance system required a thoughtfully planned data pipeline that captured the diversity, complexity, and unpredictability of real-world Indian traffic conditions. Here’s how we approached it—step by step:

---

### 🛣️ Phase 1: Real-World Data Acquisition

To ensure authenticity, we initiated collaboration with the **East-West Traffic Control Room, Ahmedabad**, under the guidance of the **Honourable Additional Commissioner of Police**. From there:

- We sourced **live CCTV footage** from high-traffic intersections, entry/exit points, and overhead surveillance grids.
- These recordings included a wide range of violations like **helmetless riding**, **mobile phone usage**, **unlicensed driving**, and **plate forgery**.

In parallel, we manually collected supplemental footage from:

- 🏫 College campuses  
- 🏘️ Residential society entry gates  
- 🅿️ Institutional parking zones  

This step helped fill class imbalance for facial identity recognition under occlusion and skewed angles.

---

### 🛠️ Phase 2: Dataset Construction & Annotation

We structured the dataset into two major modules: ANPR and FRS.

#### 📌 ANPR (Automatic Number Plate Recognition)

- **Raw Images Collected**: 7,412
- **Post-Augmentation Size**: 16,972
- **Classes Annotated**: License plate region
- **Challenges Handled**:
  - Rusted, bent, or faded plates
  - Plate distortion due to angles and motion blur
  - Shadow and lighting inconsistency

#### 📌 FRS (Facial Recognition System)

- **Raw Face Images**: 1,190  
- **Face Boxes Annotated**: 16,234
- **Subjects**: 38 individuals across age groups, genders, and demographics
- **Challenges Handled**:
  - Helmets, masks, sunglasses, scarves
  - Side profiles, head tilt, occlusion
  - Low-resolution video face segmentation

For annotation, we used:

- **LabelImg** for bounding box labeling
- **Custom Python scripts** for automated tag validation and correction

---

### 🔧 Phase 3: Preprocessing & Augmentation Pipeline

To maximize performance under real-world variability, we applied the following transformation pipeline:

#### 🧹 Preprocessing Techniques

- Image normalization & aspect-ratio preservation  
- Resizing inputs for YOLOv8 and FRS model compatibility  
- RGB/BGR conversion for uniformity across sensors  

#### 🧪 Augmentation Strategies

- Brightness & contrast randomization  
- Rotation & affine transformations  
- Horizontal flipping for symmetrical balance  
- Gaussian blur & noise injection to simulate degraded footage  
- Partial occlusion overlays (masks, helmets) to improve FRS generalization

---

### 📊 Data Composition Matrix

| Dataset Component  | Images Collected | Final Count (Post-Aug) | Annotations Used         |
|--------------------|------------------|-------------------------|---------------------------|
| ANPR               | 7,412            | 16,972                  | License plate bounding boxes |
| FRS (Detection)    | 1,190            | 1,190                   | 16,234 facial bounding boxes |

---

## [Model Training Details](#model-training-details)

<!-- 
Our training strategy focused on building high-accuracy, low-latency models capable of operating in real-time conditions across variable environments. 
Both ANPR and FRS components were trained separately, followed by end-to-end integration testing. 
-->

### 🧩 Training Infrastructure

All deep learning models were trained on the **Param Shavak Supercomputer**, configured for high-performance computing:

- **GPU**: Quadro GP100 (accelerated via Quadro P400)
- **CPU**: Intel Xeon Phi – 2.2 TFLOPS (18 cores × 2)
- **Training Frameworks**: PyTorch for YOLOv8, Dlib & `face_recognition` for FRS

This setup enabled parallelized training, robust augmentation pipelines, and high-throughput model evaluation.

---

### 📌 ANPR Training

We used multiple variants of the YOLOv8 model for Automatic Number Plate Recognition:

| Model     | Precision | Recall | mAP@50  | Box Loss | Class Loss | DFL Loss |
|-----------|-----------|--------|---------|----------|------------|----------|
| YOLOv8_S  | 94.37%    | 95.66% | 96.37%  | 1.0014   | 0.3924     | 0.9341   |
| YOLOv8_M  | 95.56%    | 97.75% | 97.75%  | 1.236    | 0.4481     | 1.034    |
| YOLOv8_N  | 93.08%    | 94.74% | 97.01%  | 1.1686   | 0.6201     | 1.063    |

**Key Highlights:**

- Optimized for real-world CCTV conditions: motion blur, low-light, skewed plates
- Trained on 16,972 annotated images (augmented from real-world datasets)
- Uses multi-scale detection and label smoothing to improve generalization

---

### 🧠 FRS Training

Our Facial Recognition System was designed for **both detection and recognition**:

- **Face Detection**: Trained on 1,190 real images with 16,234 bounding boxes
- **Face Recognition**: Used a custom dataset with **38 individuals**, capturing angle, expression, and occlusion variance

| Metric        | Value    |
|---------------|----------|
| Precision     | 98%      |
| Recall        | 98%      |
| mAP@50        | 99%      |
| Face Model    | `face_recognition` (Dlib-based HOG + CNN)

**Noteworthy Points:**

- Designed to detect partial occlusions (helmets, masks, sunglasses)
- Achieved near-human accuracy in real-time face matching
- API-compatible with Aadhaar or driving license registries for future scalability

---

### 🔄 Combined System Evaluation

Once independently trained, both models were integrated into the end-to-end surveillance pipeline. The final pipeline was benchmarked using real-time footage to ensure:

- **Challan generation latency** < 1.5 seconds per violation event
- **Cross-modal consistency** between ANPR and FRS
- **Robust violation detection** under varied weather, angles, and occlusion levels

## [Team & Roles](#team--roles)

| Sr. No. | Name                          | Role                  |
|--------:|-------------------------------|------------------------|
| 1       | Dhruvkumar Rakeshbhai Patel   | Team Leader           |
| 2       | Kovil Hasmukhbhai Savaj       | Front End             |
| 3       | Malani Prince Hiteshbhai      | Machine Learning      |
| 4       | Patel Jay Ravindrakumar       | Backend               |
| 5       | Krutika Vijaybhai Patel       | Database Management   |
| 6       | Nancy Rajesh Patel            | Database Management   |

---

### 👨‍🏫 Team Mentor

| Name                 | Expertise           | Domain Experience |
|----------------------|----------------------|-------------------|
| Dr. Himani Trivedi | ML, Deep Learning    | 8+ years          |

---

## Special Thanks

In the realm of innovation and technology, success is rarely achieved in isolation. Our project—Automatic Number Plate Recognition (ANPR) and Face Recognition System (FRS), developed for KAVACH-2023—is a reflection of meaningful collaboration and the trust placed in us by those committed to building a safer and more secure future.

Recognizing the critical role of data in developing robust ANPR and FRS systems, we reached a major milestone in our journey: acquiring high-quality, real-world traffic data from the Deputy Commissioner of Police, Traffic East, Ahmedabad City.

This was not merely a transaction, but a story of mutual trust and aligned objectives. With guidance and formal communication, we had the privilege of personally submitting our request to the Honourable Commissioner of Police. That moment, filled with hope and anticipation, underscored the responsibility entrusted to us.

With this dataset, we began the rigorous process of preparation, model training, and system development. The data from the Ahmedabad Traffic Police Department became the cornerstone of our project—capturing real-world traffic scenarios that allowed our systems to learn, adapt, and perform effectively.

As we conclude this chapter, we extend our deepest gratitude to the Deputy Commissioner of Police, Traffic East, and the entire department for their unwavering support and trust. Your contribution was not just data—it was the foundation that made this project possible.

### References

> Find all supported documents, references, reports and the presentation in the /documents directory.