# Big Data Handling Comparison - Datify

A comparative study of big data handling techniques using Pandas, Polars, and Dask on a Spotify dataset with 550,000+ songs. This project was developed for SECP3133 High Performance Data Processing course at Universiti Teknologi Malaysia (UTM).

## Team Members

| Member Name | Role |
|-------------|------|
| Camily Tang Jia Lei | Developer |
| Ng Shu Yu | Developer |

## Dataset

The dataset used is "500K+ Spotify Songs with Lyrics, Emotions and More" from Kaggle.

| Property | Value |
|----------|-------|
| Source | Kaggle |
| File Format | CSV |
| File Size | 1,122 MB (uncompressed) |
| Total Records | 551,440 entries |
| Domain | Music Streaming and Audio Analysis |

Key features include song title, artist, genre, release date, popularity, tempo, energy, acousticness, and danceability.

## Libraries Compared

| Library | Approach |
|---------|----------|
| Pandas | In-memory, single-threaded (baseline) |
| Polars | Multi-threaded, Rust-based |
| Dask | Parallel computing, lazy evaluation |

## Big Data Techniques Applied

- Column filtering (load only 10 required columns)
- Data type optimization (category, float32)
- Chunking (5,000 rows per chunk)
- Sampling (10% random sample)
- Missing value removal

## Results Summary

| Library | Execution Time | Memory Usage |
|---------|---------------|--------------|
| Pandas | 16.49 seconds | 22.42 MB |
| Polars | 1.57 seconds | 10.00 MB |
| Dask | 0.03 seconds | 84.11 MB |

## Key Findings

- **Dask** is fastest (0.03s) but uses most memory (84.11 MB)
- **Polars** has best memory efficiency (10 MB) and good speed (1.57s)
- **Pandas** is slowest (16.49s) but most familiar for small to medium datasets
