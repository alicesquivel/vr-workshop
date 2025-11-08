# 🎮 TigerHacks VR Workshop 🐯

This repository contains the slides and resources from the **VR Workshop at TigerHacks 2025 (University of Missouri)**.

Participants learned how to:
- Set up a Unity project for VR development  
- Use the **XR Interaction Toolkit** and **OpenXR**  
- Add a VR player rig (head + controllers)  
- Grab and interact with virtual objects in 3D space  
- Understand how VR is used in research, gaming, training, art, and simulation  

---

## 📂 Slides from the Workshop

You can view or download the slides here:

- **[VR Workshop Slides (PDF)](https://github.com/alicesquivel/vr-workshop/blob/main/TigerHacks.pdf)**  
- **[VR Workshop Slides (PPTX)](https://github.com/alicesquivel/vr-workshop/blob/main/TigerHacks.pptx)**

---

## 🛠 Setup Instructions (Follow-Along During Workshop)

### ✅ Requirements:
- **Unity 2022.3 LTS **
- **Meta Quest 3**
- **Windows PC + Oculus Link**
- Unity Hub installed

### ✅ Create a New VR Project:
1. Open **Unity Hub → New Project → 3D (URP or Core)**  
2. Name it something like `VR_Workshop`  

### ✅ Install VR Packages:
1. Open **Window → Package Manager**  
2. Enable *"Show Preview Packages"*  
3. Install:
   - **XR Interaction Toolkit**
   - **XR Plugin Management**  
4. Go to **Edit → Project Settings → XR Plugin Management**  
   - Enable **OpenXR**

### ✅ Add the VR Player:
1. In the **Hierarchy**:
   - Right-click → **XR → XR Origin (Action-Based)**  
2. This gives you:
   - Main Camera (your head in VR)  
   - Left and Right controllers

### ✅ Add a Grabbable Object:
1. Right-click → 3D Object → **Cube**  
2. Move it in front of the player (e.g., Position X:0, Y:1, Z:1)  
3. Add Component → **Rigidbody**  
4. Add Component → **XR Grab Interactable**  
5. Press **Play** → Put on headset → Grab and throw the cube

---

## 📚 Useful VR Learning Resources

| Topic | Link |
|-------|------|
| Unity VR Beginner Pathway | https://learn.unity.com/ |
| Meta Quest + Unity Setup | https://developer.oculus.com/documentation/unity/ |

---
