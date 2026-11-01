# 3D Volume Slicing and Plane Projection

## What Is This Project About?

A 3D medical scan contains much more information than we can see in a single image. To explore different parts of the scanned volume, we need a way to extract 2D views from different positions and directions.

This project focuses on building a Python application that can generate these views from 3D volumetric data.

Instead of working only with fixed directions such as horizontal or vertical slices, the program will support planes defined by coordinates in 3D space.

The main challenge is to transform these plane definitions into accurate 2D images while keeping the implementation efficient, reliable, and easy to maintain.

## The Problem We Want to Solve

Our starting point is a three-dimensional matrix containing voxel values.

Each voxel has a position (x, y, z) and stores a numerical value representing the data at that location.

We are also given a plane defined by three or four points in 3D space.

The task is to determine which positions in the volume correspond to the selected plane, sample their values, and arrange the results into a 2D matrix.

This process must account for several challenges:

- Converting coordinates between 3D space and a 2D image.
- Determining the correct image dimensions.
- Handling sampling positions outside the volume.
- Checking whether the input points define a valid plane.
- Processing large volumes without unnecessary calculations.

The goal is not only to produce an image, but also to design an algorithm that behaves consistently across different inputs.

## What We Plan to Build

The application will be developed in Python and will support the following workflow:

1. Load volumetric data from an NRRD file.
2. Read a list of plane definitions from a CSV file.
3. Check the geometric validity of each plane.
4. Calculate the corresponding 2D image using voxel sampling.
5. Generate an error frame when a plane definition is invalid.
6. Combine all generated frames into an MP4 video, preserving the order of the CSV entries.

A valid plane should produce a projection image. An invalid plane should not prevent the remaining planes from being processed.

## Project Boundaries

The project focuses on extracting plane-based images from existing volumetric data.

It does not aim to perform medical diagnosis, recognize anatomical structures, or create new 3D scans.

The emphasis is on algorithm design, clean software structure, correctness, error handling, and runtime performance.

## Development Approach

We will build the application in small, testable parts.

The main responsibilities will include input handling, plane validation, coordinate calculations, voxel sampling, and video generation.

Separating these responsibilities will make the program easier to understand, test, and improve.

We will also evaluate the implementation using different inputs, including valid planes, invalid planes, and larger datasets.

## Tools and Formats

- **Language:** Python
- **Volume input:** NRRD
- **Plane definitions:** CSV
- **Generated output:** MP4
- **Version control:** Git and GitHub

## Current Progress

The project is currently in the planning stage.

The algorithm, tests, execution instructions, and experimental results will be documented as development continues.
