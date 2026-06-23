# EM3K Viewer

EM3K (Edumatic 3000) is an offline-first educational content viewer built with Preact.

The project is part of a larger ecosystem designed around portable, self-contained course packages that can be distributed through traditional web services, local networks, removable media, and decentralized technologies such as IPFS.

Unlike traditional Learning Management Systems (LMS), EM3K is designed to function without requiring user accounts, constant connectivity, or centralized infrastructure.

## Project Goals

- Offline-first learning
- Self-contained course packages
- Privacy-focused student experience
- Optional progress tracking
- Portable content formats
- Open publishing ecosystem
- Support for decentralized distribution

## Current Status

This repository contains the student-facing viewer application.

The viewer is responsible for:

- Managing a local course library
- Validating course packages
- Activating and deactivating content
- Rendering lessons and quizzes
- Tracking learner progress
- Supporting offline usage

The project is currently undergoing a major architectural refactor focused on:

- Modular content structures
- JSON Schema validation
- Package-based course management
- Future support for desktop and mobile deployments

## Content Structure

Courses are self-contained packages.

```text
teacher/
└── course/
    ├── course.json
    ├── lessons/
    ├── images/
    ├── videos/
    └── assets/
```

Each course contains all content required to render lessons without relying on a server.

## Planned Ecosystem

### Viewer

Student-facing application for consuming educational content.

Platforms:

- PWA
- Tauri Desktop
- React Native Mobile

### Teacher Portal

Content authoring and management platform.

Planned stack:

- Laravel
- Filament
- MySQL

### Catalog

Course discovery and distribution service.

Features:

- Search
- Publishing
- Verification
- Package distribution
- Validation

EM3K uses JSON Schema validation (AJV) to ensure content packages conform to the expected structure before activation.

Future validation may include:

- Asset verification
- Digital signatures
- Integrity checks
- Schema migration support

## Future Features

- Package installation
- Local content sharing
- Bluetooth distribution
- Mesh networking
- Torrent support
- IPFS support
- Signed content packages
- White-label deployments
- Organization-managed catalogs

## Philosophy

Learning should not depend on centralized infrastructure.

Students should be able to download educational content once and continue learning regardless of connectivity, platform, or location.

EM3K aims to provide a lightweight, portable alternative to traditional server-centric LMS platforms.

## Long-Term Vision

EM3K is evolving beyond a traditional course viewer into an open educational content ecosystem.

The long-term goal is to create a platform where educators can:

- Create courses
- Publish courses
- Share courses
- Verify courses
- Distribute courses through multiple channels

Content should be portable and usable whether it is delivered through:

- The official EM3K catalog
- Private organizational catalogs
- Local networks
- USB drives
- IPFS
- Torrents
- Direct file sharing

The viewer, teacher portal, and catalog are intended to serve as reference implementations built on open schemas and content formats, allowing third parties to build compatible tools and services in the future.

EM3K's guiding principle is simple:

Learning should remain accessible even when the internet is not.
