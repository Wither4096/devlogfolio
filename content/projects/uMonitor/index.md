---
date: 2026-05-29T11:29:49+03:00
title: "μMonitor"
description: "A university project improved"
tags: ["project"]
summary: "Real Time ESP32 Room Monitoring System"
---

## Project Info

- **Status:** wip
- **Tech:** `C++`, `ESP32`, `Arduino`, `Firebase RTDB`, `Flutter`
- **Repo:** [GitHub](https://github.com/wither4096/uMonitor)

## Overview

A real-time room monitoring system built around an ESP32. Originally developed for a university final project, it evolved into a learning project in embedded systems, software architecture, and IoT integrations.

## Goals

- Develop a project that feels and functions as a real product
- Develop a robust system architecture
- Learn embedded system design closer to industry work
- Experiment with cloud and IoT integration
- Tolerate Flutter and front-end development *(failed miserably)*

## Design

- Modular architecture split into multiple header, source files
- Software abstractions of hardware
- Event driven alert system using state transitions
- Firebase RTDB integration for remote data-point monitoring
- Mobile Flutter app for remote viewing
- Naive redundancy and fallback mechanisms for sensors

## Implementation

- ESP32 program written in C++ using Arduino IDE
- Non-blocking delays using `millis()` timestamps
- Firebase sync using JSON
- Alert system using pre-defined thresholds

## Features

- Temperature monitoring
- Humidity monitoring
- Air quality monitoring
- Ambient light monitoring
- Redundant sensors
- Physical feedback through buzzer, RGB LED, and OLED display
- Historical Data viewer

## What I Learned

- How embedded systems are built from scratch, including design considerations, refactoring, architectural design, etc.
- Clean separation of hardware, business, cloud logic
- Practical design and implementation with engineering constraints
- Basic JSON serialisation
- Designing with an evolving design in mind