# 02_Clinical_Gait_Features.md
## GaitAI MobilityCare — Clinical Gait Features

## What Are Gait Features?

Gait features are measurable parameters extracted from how a person walks. Just like a doctor measures blood pressure or heart rate as numbers, GaitAI measures walking as numbers — cadence, speed, symmetry, sway — to objectively assess mobility and flag health concerns.

## Feature Table

### Part A — What Each Feature Measures

| Feature                  | What it Measures                                          | Video Extractable? |
|--------------------------|-----------------------------------------------------------|--------------------|
| Cadence                  | Number of steps per minute                                | Yes                |
| Walking Speed            | Distance covered per second while walking                 | Partly             |
| Step Time                | Time from one foot strike to the next (R to L)            | Yes                |
| Stride Time              | Time for one full gait cycle (R foot to R foot)           | Yes                |
| Left-Right Symmetry      | Timing and range difference between left and right sides  | Yes                |
| Trunk Sway               | Upper body wobble side to side or front to back           | Partly             |
| Posture Angle            | Forward lean or abnormal body alignment during walking    | Yes                |
| Knee/Hip Range of Motion | Degree of bend in knee and hip joints during walking      | Partly             |
| Gait Variability         | Step-to-step inconsistency in timing and length           | Yes                |
| Mobility Score           | Composite 0–100 score derived from all features above     | Derived            |

### Part B — Why Each Feature Matters Clinically

| Feature                  | Clinical Significance                                              | Useful For                              |
|--------------------------|--------------------------------------------------------------------|-----------------------------------------|
| Cadence                  | Low or irregular = mobility decline, fatigue, or neuro change      | Elderly care, rehab, general screening  |
| Walking Speed            | Slowness is one of the strongest predictors of fall risk           | Elderly care, hospital, rehab           |
| Step Time                | Irregular timing = instability or neuromuscular problems           | FallRisk, neuro monitoring              |
| Stride Time              | Rhythm and variability analysis across conditions                  | Rehab tracking, neuro monitoring        |
| Left-Right Symmetry      | Asymmetry = stroke, injury, pain, or compensation on one side      | Rehab, ortho, neuro                     |
| Trunk Sway               | High sway = balance problems and elevated fall risk                | FallRisk, elderly care                  |
| Posture Angle            | Poor alignment affects balance, stability, and efficiency          | Rehab, Parkinsonian gait                |
| Knee/Hip Range of Motion | Reduced range = stiffness, weakness, or post-surgical pain         | Rehab, ortho                            |
| Gait Variability         | High variability strongly linked to instability and fall risk       | FallRisk, elderly care, neuro           |
| Mobility Score           | Simple number for clinicians and caregivers to track over time     | Clinics, caregivers, general screening  |

## Feature Categories

### Group 1 — Fully Video Extractable
These features can be extracted from a standard walking video using pose estimation:
- Cadence
- Step Time
- Stride Time
- Left-Right Symmetry
- Posture Angle
- Gait Variability
- Mobility Score (derived)

### Group 2 — Partially Video Extractable
These features can be approximately detected from video but give more precise results with IMU sensors:
- Walking Speed (needs reference scale)
- Trunk Sway (needs front or back view)
- Knee/Hip Range of Motion (needs clear side view and good resolution)

### Group 3 — Needs Special Sensors
These features require IMU, force plate, or clinical sensors for accurate measurement:
- Ground Reaction Force (force plate)
- Muscle Activation (EMG sensors)
- Precise Joint Angles (IMU or motion capture lab)

## Feature to Use Case Mapping

| Use Case                  | Most Important Features                                                    |
|---------------------------|----------------------------------------------------------------------------|
| Elderly Care              | Cadence, Walking Speed, Trunk Sway, Gait Variability, Mobility Score       |
| Fall Risk Screening       | Walking Speed, Trunk Sway, Gait Variability, Left-Right Symmetry, Posture Angle |
| Neuro Movement            | Step Time, Stride Time, Left-Right Symmetry, Gait Variability, Posture Angle |
| Rehab Tracking            | All features tracked across sessions to measure improvement                |
| General Mobility Screening| Cadence, Walking Speed, Mobility Score                                     |
