# macOS for IT Support Troubleshooting

## Introduction

Welcome to my macOS documentation.

As an IT Support Professional with a strong foundation in Windows environments, I built this section to document my hands-on learning of Apple's macOS operating system.

My goal is simple: to broaden my technical skill set and demonstrate my ability to support users across multiple platforms.

I am currently building this portfolio and will continue updating it with step-by-step configurations, troubleshooting workflows, and screenshots as I explore macOS.

> **Note:** Some configurations are being tested in a local environment without a primary Apple ID.

---
## Cross-Platform Troubleshooting

Understanding how macOS handles local networking, permissions, and file systems makes me a more adaptable and effective IT Support professional and problem solver.

---
## Portfolio Objective

This repository serves as my living documentation as I expand beyond a Windows-only environment and continue developing my cross-platform IT support capabilities.

The goal is to build practical experience supporting both Windows and macOS environments through hands-on configuration, troubleshooting, and documentation.

# Case Study 1: User Having Performance Issues with a Mac Device

## Scenario

A user contacted IT Support reporting slow performance on their macOS device.

I reached out to the user via email and performed basic troubleshooting, such as asking the user to restart the system. However, the issue still persisted.

---
# Troubleshooting Sluggish macOS Performance

## Step 1: Isolate the Resource Hog (Activity Monitor)

The macOS equivalent of **Task Manager** in Windows is **Activity Monitor**. It is the primary diagnostic tool used to identify processes consuming excessive system resources.

### Open Activity Monitor

1. Press:

```text
Command (⌘) + Space
```

2. Type:

```text
Activity Monitor
```

3. Press **Enter**.

---
## Check CPU Usage

1. Open the **CPU** tab.
2. Sort processes by **% CPU** in descending order.
3. Look for:
   - Third-party applications consuming excessive CPU.
   - Stuck system processes.
   - Any process consistently using more than **80% CPU**.

---

## Check Memory Usage

1. Open the **Memory** tab.
2. Review the **Memory Pressure** graph located at the bottom of the window.

### Memory Pressure Colors

- **Green** – RAM usage is healthy and the system has sufficient available memory.
- **Yellow/Red** – The Mac is under memory pressure and is actively using storage (swap memory), which can significantly reduce system performance.