# Edumatic 3000 (em3k)

Welcome! Edumatic 3000 (em3k) is a self-contained linear-progression education app with basic quizzing functionality. Build your own lessons and quizzes using JSON files and modern web technologies. Edumatic 3000 allows you to focus on the content of your lessons and not worry about the mechanics of grading quizzes & answers, or dealing with navigation elements. The app (optionally) tracks the user's progress as they advance through the lessons and enforces linear progress so that the student can't skip ahead to more advanced lessons.

## Planned apps:

* Student front-end app for viewing the lessons
* Teacher back-end app for creating / editing / managing the lessons
* A "courses" marketplace where people can find, download, and share courses
* Community forums

## Tech Stack

* The student app is being created in Preact with a Tauri desktop wrapper
* The backend is being created with Laravel / Filament / Livewire / Blade
* The data files will be stored in JSON format for offline use and portability
* The focus for the student app is offline-first / cached data that can be used anywhere
* Support for IPFS is planned
