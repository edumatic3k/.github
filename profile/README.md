# Edumatic 3000 (Em3k)

**Create. Share. Learn. Anywhere.**

Edumatic 3000 (EM3K) is an open-source educational platform designed around self-contained course packages, a lightweight learner application, and tools that allow educators to create and distribute lessons and quizzes.

EM3K takes a different approach from traditional Learning Management Systems (LMS).  Learning content can be downloaded, installed, and used locally without requiring continuous internet connectivity, centralized student accounts, or an active connection to the publishing server.

The goal is simple: make educational content easy to create, distribute, and use.

## Project Goals

- **Offline-first learning:** Installed courses should remain usable without an internet connection.
- **No required learner accounts:** Students can install courses and learn anonymously.
- **Portable course packages:** Courses are self-contained and can be distributed as ZIP archives.
- **Local learner data:** Course installations and learning progress are stored on the learner's device.
- **Open content formats:** JSON Schema defines a documented contract between authoring tools, publishers, and viewers.
- **Independent components:** The viewer, teacher portal, and catalog have separate responsibilities.
- **Flexible distribution:** Courses can be shared through the official catalog or independently of EM3K's infrastructure.

## The EM3K Ecosystem

EM3K is organized into several independent components.

| Component | Purpose | Technology |
|---|---|---|
| [EM3K Viewer](https://github.com/edumatic3k/em3k-viewer) | Course installation, lessons, quizzes, and local progress | Preact PWA |
| [EM3K Server](https://github.com/edumatic3k/em3k-server) | Teacher accounts, course authoring, and publishing | Laravel, Filament, MariaDB |
| [EM3K Data](https://github.com/edumatic3k/em3k-data) | Published course packages and catalog data | Static files and JSON |

### Learner Viewer — em3k.org

The viewer is the primary student-facing application.

Learners can install courses, navigate lessons, answer practice quizzes, and maintain a personal course library.

Installed content and progress are stored locally in the browser using IndexedDB.  The viewer does not require a learner account or a connection to the Laravel backend for course playback.

The viewer is built with Preact and uses JSON Schema validation to check course packages before installation.

### Teacher Portal — teacher.em3k.org

The teacher portal is intended to provide a web-based environment where educators can create and manage courses without manually editing JSON files.

Laravel and Filament provide the foundation for authentication, database management, administrative interfaces, and future course-authoring tools.

Planned teacher workflows include creating courses, organizing lessons, adding content blocks and quizzes, and publishing completed courses.

The backend foundation exists, but the course-authoring and publishing workflows are still under development.

### Course Catalog — catalog.em3k.org

The catalog is intended to serve as a lightweight discovery and distribution service.

Published course packages and their associated catalog metadata will be available as static artifacts.  Learners will be able to discover courses and install them into the viewer.

The catalog is not required for independently distributed course ZIP files.

## Portable Course Packages

A course package contains a manifest, lessons, and any assets
