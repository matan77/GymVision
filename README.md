# GymVision

## Introduction

GymVision is a workout tracking app that incorporates computer vision technology. While it functions as a standard workout tracker, it offers advanced computer vision features-such as using the phones camera to log reps and sets instead of manual entry. users point their camera at themselves during the exercise, and the app identifies the movement, counts the sets, and assesses whether the technique is correct.

---

## The Problem

Tracking workouts manually creates friction, leading most people to abandon logging usually. Additionally, working out without a trainer makes it difficult to maintain proper form, verify full range of motion, and prevent injury. GymVision automates tracking and movement feedback using standard phone hardware, removing the friction from workout logging.

---

## Core Concept

The user positions their phone to capture the exercise. A computer vision pipeline performs real-time pose estimation, tracking joint angles and movement phases (eccentric/concentric) to validate reps and flag mechanical breakdown. All logged data syncs directly to the user's profile and history.

---

## Development Roadmap

### Phase 1: MVP

* Support for 2–3 core compound/bodyweight movements (e.g., Squat, Push-up)
* Real-time rep counting via pose estimation and movement phase detection
* Workout session logging (exercise, sets, reps, timestamps)
* Basic dashboard displaying recent workouts and session summaries

### Phase 2: Performance & Analytics

* Movement tempo and time-under-tension tracking
* Weekly/monthly volume and consistency metrics
* Expanded exercise library (additional bodyweight and free-weight movements)
* Performance trend graphs and milestone tracking

### Phase 3: Real-Time Form Analysis

* Joint angle verification against defined kinematic thresholds (Range of Motion)
* Live visual/audio cues for common faults (e.g., knee valgus, spinal flexion)
* Per-set movement quality score
* Actionable post-set technique breakdowns

### Phase 4: Personalization

* Dynamic volume/intensity suggestions based on logged performance
* Custom goal setting and progressive overload tracking
* Video replay clips highlighting technique breakdowns across past sessions

---

## Tech Stack

### Fronetend - Mobile Client

* React Native Or react web app with capacitorJS
* Real-time camera feed integration and skeleton overlay rendering

### Computer Vision & Processing

* MediaPipe or OpenCV for pose estimation
* TensorFlow Lite / ONNX Runtime for on-device inference

### Backend - API

* Node.js Express
* REST API architecture for user management, sync, and processing offload

### Database & Storage

* mongodb for user and workout data

### Infrastructure & Tooling

* Docker containerization
