# VR Setup Guide (Unity + XR Interaction Toolkit)

## 0) Prerequisites

- Unity 2022.3 LTS or 2023.3 LTS
- Project created using:
  - 3D (Core) or
  - 3D URP Template
- Target device:
  - Meta Quest 2 or Quest 3
  - or Play Mode using XR Device Simulator

---

## 1) Install Required Packages

1. Open Window → Package Manager
2. In the Packages dropdown, choose Unity Registry
3. Install the following:
   - XR Interaction Toolkit
   - XR Plugin Management
   - OpenXR Plugin
   - Input System
4. When prompted by XR Interaction Toolkit, enable the new Input System and allow Unity to restart

---

## 2) Enable OpenXR and Controller Profiles

1. Go to Edit → Project Settings → XR Plug-in Management
2. Under both PC, Mac & Linux Standalone and Android tabs:
   - Check OpenXR
3. Go to Project Settings → XR Plug-in Management → OpenXR
4. Under Features, enable:
   - Oculus Touch Controller Profile or Meta Quest Touch Controller Profile
   - (Optional) Hand Tracking features
5. If validation errors appear, click Fix All

---

## 3) Ensure the Input System Is Active

1. Go to Edit → Project Settings → Player → Other Settings
2. Set "Active Input Handling" to "Input System Package (New)" or "Both"

---

## 4) Add XR Rig to the Scene

### Option A: Starter Assets

1. Open Window → Package Manager → XR Interaction Toolkit
2. Under Samples, import:
   - Starter Assets
   - XR Device Simulator
3. In the scene, add:
   - GameObject → XR → XR Origin (XR Rig)
   - GameObject → XR → XR Interaction Manager
   - Optional: GameObject → XR → XR Device Simulator

### Option B: Manual Setup

XR Origin usually already includes LeftHand Controller and RightHand Controller objects with components attached.

---

## 5) Verify Controller Components

Each hand controller under XR Origin should include:

- XR Controller (Action-based)
- XR Ray Interactor and/or XR Direct Interactor
- Line Renderer (for ray visuals)

For physical grabbing, make sure an XR Direct Interactor is available.

---

## 6) Create a Grabbable Object

1. Create 3D Object → Cube or Sphere
2. Rename (e.g. GrabbableBall)
3. Add components:
   - Rigidbody
     - Use Gravity: On
     - Is Kinematic: Off
     - Collision Detection: Continuous
   - Collider (Box, Sphere, or Mesh)
   - XR Grab Interactable

Recommended XR Grab Interactable settings:
- Movement Type: Velocity Tracking
- Track Position: On
- Track Rotation: On
- Throw on Detach: On
- Select Mode: Single

---

## 7) Adjust How the Object Sits in the Hand

1. Right-click the object → Create Empty → rename to AttachPoint
2. Position/rotate AttachPoint where the hand should hold the object
3. In XR Grab Interactable, assign AttachPoint to Attach Transform
4. Test and adjust if needed

---

## 8) Optional: Create a Socket to Snap Objects Into Place

1. Create Empty GameObject → rename ItemSocket
2. Add XR Socket Interactor
3. (Optional) Add a visual indicator for the socket location
4. Make sure the object’s layer and the socket's Interaction Layer Mask match
5. In Play Mode:
   - Grab object → move to socket → release → object should snap in

---

## 9) Improve Physics (Better Throwing and Interaction)

1. Go to Edit → Project Settings → Physics
2. Set:
   - Default Solver Iterations: 12
   - Default Solver Velocity Iterations: 12
3. Set realistic Rigidbody mass (0.2 – 1 kg)
4. Avoid extreme scales for objects

---

## 10) Test Without a Headset (XR Device Simulator)

1. Make sure XR Device Simulator exists in the scene
2. Enter Play Mode
3. Controls:
   - Right Mouse Button: Look around
   - Shift + WASD: Move camera
   - 1 or 2 or on-screen UI: Switch between left and right hand
   - Move hand to object and press the grab button (mapped in Input Actions)

---

## Finished

You can now:
- Grab, drop, and throw objects
- Use rays or direct hand interaction
- Test everything without a headset using XR Device Simulator
- Add sockets for object placement if needed

---
