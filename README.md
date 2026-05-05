# ChirpR

**An R package for analyzing and visualizing ecological audio monitoring data.**

---

## Background

During the development of [Ecomon](https://github.com/MfN-Berlin/ecomon/tree/ecomon_validate), a web platform for analyzing and visualizing 
ecological audio monitoring data, the question arose as to whether an R package providing similar functionality could serve as a viable alternative.

Ecomon provides extensive functionality for handling multiple recording sites, large volumes of audio recordings, multiple bird identification models, 
parallel processing, storing large amounts of inferences in high-performance databases, and automating these tasks. 
These extended features are outside the scope of the present project.

Instead, **ChirpR shall concentrate** on the core functionalities of handling single or manageable amounts of audio files and visualizing the results.

---

## Core Functionalities

The ChirpR package **shall provide** the following core functionalities:

- Apply a bird identification model to a single audio file, storing the results as a table (e.g., a compressed pickle file).
- Apply a bird identification model to an input folder containing audio files, storing the results as multiple files in an output folder.
- Load and display the identifications for a single audio file.
- Retrieve a list of all species identifiable by a model.

---

## Visualizations

The following visualizations **shall be provided** for a given combination of species, year, and confidence threshold, 
for the combined identifications in an output folder:

- **Heatmap**: Visualization of the maximum confidence values per time unit (e.g., per minute).
- **Bin size distribution**: Minutes with activity by confidence value, filtered by species, year, and confidence threshold.
- **Acoustic activity over time**: Minutes above the threshold by date (daily, 5-day, 10-day, or monthly intervals), filtered by species, year, and confidence threshold.
- **Diel acoustic activity**: Minutes of acoustic activity above the threshold by time of day, accounting for sunrise and sunset times.
