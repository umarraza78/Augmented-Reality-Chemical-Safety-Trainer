# 🧪 Augmented Reality Chemical Safety Trainer

An **Augmented Reality (AR) laboratory safety application** developed with **Unity and Vuforia Engine** to help users identify chemicals and access important safety information directly through a mobile device.

The application is designed as an interactive laboratory safety assistant that can provide information such as **chemical hazards, required personal protective equipment (PPE), handling precautions, and recommended safety measures** when a chemical is recognized.

The project was developed as part of an **Erasmus+ Bootcamp** with a focus on applying Augmented Reality to real-world laboratory safety and education.

---

## 📱 Project Overview

Laboratory environments contain many chemicals that require specific handling procedures and protective equipment. Remembering the hazards and safety requirements of every chemical can be difficult, especially for students and new laboratory users.

The **AR Chemical Safety Trainer** addresses this problem by using a mobile device to recognize supported chemical markers/targets and display relevant safety information through an Augmented Reality interface.

Instead of relying solely on traditional labels or safety manuals, users can interact with digital safety information directly within their physical environment.

### Example Information Provided

Depending on the recognized chemical, the application can display:

* 🧪 Chemical name
* ⚠️ Potential hazards
* 🥽 Required PPE
* 🧤 Recommended gloves
* 😷 Respiratory protection requirements
* 👕 Protective clothing recommendations
* 🔥 Flammability information
* ☣️ Health hazards
* 📋 Handling precautions
* 🚨 Emergency/safety guidelines
* 🗑️ Disposal precautions

---

## ✨ Key Features

### 🔍 Chemical Recognition

The application uses **Vuforia Engine** to recognize predefined targets associated with chemicals.

### 🥽 PPE Recommendations

After identifying a chemical, the application provides recommended protective equipment such as:

* Safety goggles
* Laboratory gloves
* Lab coat
* Face protection
* Respiratory protection

### ⚠️ Hazard Information

Users can access important information regarding potential chemical hazards and risks.

### 📱 Mobile AR Experience

The application is packaged as an **Android APK**, allowing users to interact with the system using a smartphone.

### 🎯 Vuforia-Based Tracking

Vuforia's image-target recognition capabilities are used to identify the relevant target and trigger the corresponding AR content.

### 📚 Educational Use

The system can be used as an interactive learning tool for:

* University laboratories
* Chemistry education
* Laboratory safety training
* Student demonstrations
* Safety awareness programs

---

# 🛠️ Technologies Used

| Technology         | Purpose                           |
| ------------------ | --------------------------------- |
| **Unity**          | AR application development        |
| **C#**             | Application logic and interaction |
| **Vuforia Engine** | Image recognition and AR tracking |
| **Android**        | Mobile deployment platform        |
| **ARM64**          | Android architecture              |
| **IL2CPP**         | Unity scripting backend           |
| **Unity UI**       | Safety information interface      |

---

# 🏗️ System Workflow

The basic workflow of the application is:

```text
                    ┌───────────────────┐
                    │   Start Android   │
                    │     Application   │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │  Camera Scanning  │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │ Vuforia Target    │
                    │    Detection      │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │ Identify Chemical │
                    └─────────┬─────────┘
                              │
                              ▼
              ┌───────────────┴────────────────┐
              │                                │
              ▼                                ▼
       Chemical Details                 Safety Information
              │                                │
              └───────────────┬────────────────┘
                              ▼
                    ┌───────────────────┐
                    │ Display AR Safety │
                    │    Information    │
                    └───────────────────┘
```

---

# 🎯 AR Interaction

The application uses a **camera-based Augmented Reality experience**.

When the camera detects a supported target:

1. Vuforia recognizes the target.
2. The application determines the associated chemical.
3. The corresponding AR content is activated.
4. Chemical information is displayed to the user.
5. Safety recommendations and PPE requirements are presented.
6. The user can interact with the available information through the mobile interface.

---

# ⚙️ Development Configuration

## Unity

The project was developed using **Unity**.

Before opening the project, make sure the required Unity version and Android Build Support modules are installed.

Recommended Unity modules:

* Android Build Support
* Android SDK & NDK Tools
* OpenJDK

> **Note:** Use the Unity version compatible with the project's Vuforia Engine package.

---

# 🎯 Vuforia Configuration

The project uses **Vuforia Engine** for AR target recognition.

A Vuforia developer account/license is required when configuring the project.

The Vuforia configuration includes:

* Vuforia Engine package
* AR Camera
* Image Targets
* Target Database
* Vuforia License Key

### License Key

The Vuforia License Key should **not be committed to the public repository**.

If the project requires a license key, configure it locally through the Vuforia configuration settings.

For example:

```text
Vuforia Configuration
        ↓
License Key
        ↓
Local Development Configuration
```

### ⚠️ Security Notice

Do not publish your private Vuforia license key, API keys, credentials, or other sensitive configuration values in this repository.

If you fork or clone this project, configure your own Vuforia license key.

---

# 📱 Android Configuration

The project was configured for Android deployment and tested as an **APK** on a compatible Android smartphone.

### Build Platform

```text
Platform: Android
```

### Target Architecture

```text
ARM64
```

ARM64 is enabled to support modern Android devices.

### Scripting Backend

```text
IL2CPP
```

The project uses Unity's **IL2CPP scripting backend** for the Android build.

Typical Android configuration:

```text
Build Platform: Android
Scripting Backend: IL2CPP
Target Architecture: ARM64
```

---

# 🔧 Android Build Settings

Before generating the APK, configure the Unity project accordingly.

### 1. Switch Platform

Go to:

```text
File → Build Settings
```

Select:

```text
Android
```

Then select:

```text
Switch Platform
```

### 2. Player Settings

Navigate to:

```text
Edit → Project Settings → Player
```

Configure the Android settings according to the target device.

### 3. Architecture

Under Android configuration, enable:

```text
ARM64
```

### 4. Scripting Backend

Set:

```text
Scripting Backend → IL2CPP
```

### 5. Build APK

After configuring the project:

```text
File → Build Settings → Android → Build
```

The resulting APK can then be installed on a compatible Android device.

---

# 📂 Project Structure

The project follows a typical Unity project structure:

```text
AR-Chemical-Safety-Trainer/
│
├── Assets/
│   ├── Scenes/
│   ├── Scripts/
│   ├── Prefabs/
│   ├── Materials/
│   ├── Models/
│   ├── Textures/
│   └── ...
│
├── Packages/
│
├── ProjectSettings/
│
├── README.md
├── .gitignore
└── ...
```

Unity-generated folders such as `Library`, `Temp`, and other build/cache files should not be committed to the repository.

---

# 🧩 Main Components

## AR Camera

The AR Camera provides the camera feed used by Vuforia for target recognition.

## Image Targets

Image Targets are associated with the supported chemical information.

When a target is recognized, the corresponding AR content becomes active.

## Chemical Information UI

The user interface presents information such as:

```text
Chemical Name
      ↓
Hazards
      ↓
Required PPE
      ↓
Handling Precautions
      ↓
Emergency Information
```

## Safety Information

Each supported chemical can have its own safety information and recommendations.

---

# 🧪 Example Use Case

Imagine a student working in a university chemistry laboratory.

The student points their smartphone camera toward a supported chemical target.

The application recognizes the target and displays:

```text
🧪 Chemical: Example Chemical

⚠️ Hazards:
• Irritant
• Harmful if inhaled

🥽 Required PPE:
• Safety goggles
• Laboratory gloves
• Lab coat

🧤 Handling:
• Avoid direct skin contact
• Handle in a suitable laboratory environment

🚨 Safety:
Follow the laboratory's established safety procedures.
```

This allows important information to be accessed quickly without manually searching through a safety manual.

---

# 🎓 Erasmus+ Bootcamp

This project was developed during an **Erasmus+ Bootcamp** as a practical application of Augmented Reality technology.

The project explored how AR can be applied beyond entertainment and gaming, particularly in areas such as:

* Laboratory education
* Safety training
* Interactive learning
* Hazard awareness
* Technical training

---

# 🚀 Future Improvements

Several improvements could be added in future versions:

* 🤖 AI-based chemical recognition
* 📷 Camera-based recognition without predefined image targets
* 🧪 Larger chemical database
* 🌐 Online chemical information database
* 🔊 Voice-based safety instructions
* 🌍 Multi-language support
* 📊 Laboratory safety analytics
* 🔔 Real-time hazard alerts
* 🥽 AR 3D visualization of molecular structures
* 📱 Improved Android UI/UX
* ☁️ Cloud-based chemical information management

---

# ⚠️ Safety Disclaimer

This application is intended as an **educational and laboratory safety assistance tool**.

The information displayed by the application should **not replace official Safety Data Sheets (SDS), laboratory safety procedures, institutional policies, or professional safety guidance**.

Users should always follow the safety procedures established by their laboratory or institution.

---

# 📸 Screenshots

Add screenshots of the application here.

Recommended screenshots:

1. Application home screen
2. Camera/AR scanning interface
3. Chemical target recognition
4. Chemical information display
5. PPE recommendations
6. Hazard information

Example:

```markdown
![AR Chemical Recognition](Screenshots/chemical-recognition.png)

![Safety Information](Screenshots/safety-information.png)

![PPE Recommendations](Screenshots/ppe-recommendations.png)
```

---

# 🎥 Demo

Add a short demonstration video showing:

```text
Open Application
      ↓
Scan Chemical Target
      ↓
Target Recognition
      ↓
Chemical Identification
      ↓
Safety Information
      ↓
PPE Recommendations
```

You can host the demonstration on YouTube or include a suitable video/GIF in the repository.

---

# 📦 Installation

## Requirements

* Android smartphone
* Compatible Android version
* Unity project for development
* Vuforia Engine configuration
* Vuforia License Key
* Android Build Support

## Using the APK

If an APK is provided in the repository/release:

1. Download the APK.
2. Transfer it to an Android device.
3. Allow installation from the required source if prompted.
4. Install the application.
5. Launch the application.
6. Point the camera toward a supported target.
7. View the corresponding chemical safety information.

---

# 💻 Running the Project in Unity

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/AR-Chemical-Safety-Trainer.git
```

Open the project using the compatible Unity version.

Then:

1. Install/configure Vuforia Engine.
2. Configure your own Vuforia License Key.
3. Open the main Unity scene.
4. Connect an Android device or configure Android Build Support.
5. Configure ARM64 and IL2CPP.
6. Build and deploy the application.

---

# 👨‍💻 Developer

**Muhammad Umar Raza**

**Software Engineer | FAST-NUCES**

Specializing in:

* MERN Stack
* DevOps
* Cloud Computing
* Computer Vision
* Artificial Intelligence
* Augmented Reality

### Connect

* GitHub: `https://github.com/umarraza78`
* LinkedIn: `https://linkedin.com/in/mumarraza789`
* Portfolio: `https://omer-raza78portfolio.vercel.app`

---

# 📄 License

This project is intended for educational and demonstration purposes.

If you plan to distribute or commercially use the project, review the licensing requirements of all third-party technologies and assets used in the project, including **Vuforia Engine, Unity packages, 3D models, images, and other external resources**.

---

## ⭐ Project Highlights

**AR + Laboratory Safety + Mobile Application + Vuforia + Unity**

This project demonstrates the practical use of **Augmented Reality for laboratory safety education**, allowing users to access chemical hazard and PPE information through an interactive mobile AR experience.
