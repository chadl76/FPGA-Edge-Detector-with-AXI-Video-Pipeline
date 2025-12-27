# FPGA Edge Detector with AXI Video Pipeline

## Overview
This project implements a **real-time edge detection system** on an FPGA using a **Sobel filter**, integrated into an **AXI4-Stream video processing pipeline**.

The design uses Xilinx video IP cores such as the **Test Pattern Generator (TPG)** and **Video Timing Controller (VTC)** along with a **custom AXI-based Sobel edge detector**. Video data is streamed through the pipeline and processed in hardware.

---

## System Architecture

![Block Diagram](Media/Block%20Diagram.png)

### Video Pipeline
```text
Test Pattern Generator (TPG)
        ↓ AXI4-Stream
Custom Sobel Edge Detector
        ↓ AXI4-Stream
Video Timing Controller (VTC)
        ↓
Video Output
