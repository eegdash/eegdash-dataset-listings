# EEGDash Dataset Listings

This repository contains JSON listings of EEG datasets from various sources that are processed by the [EEGDash](https://github.com/eegdash/EEGDash) pipeline.

## Structure

- `consolidated/` - Consolidated dataset listings from all sources
  - `openneuro_datasets.json` - All OpenNeuro datasets
  - `nemardatasets_repos.json` - All NEMAR GitHub repositories
  - `eegmanylabs_datasets.json` - All EEGManyLabs datasets
  - `zenodo_datasets.json` - All Zenodo datasets
  - `figshare_datasets.json` - All Figshare datasets
  - `osf_datasets.json` - All OSF datasets
  - `to_digest_*.json` - Filtered datasets ready for ingestion

## Update Frequency

These files are automatically updated by GitHub Actions workflows in the main EEGDash repository:
- Weekly on Mondays at 00:00 UTC
- Can also be triggered manually via workflow dispatch

## Usage

These JSON files are consumed by the EEGDash ingestion pipeline to:
1. Track available datasets across multiple sources
2. Filter new datasets that haven't been processed yet
3. Clone and digest dataset metadata for MongoDB ingestion

## Related Repositories

- [EEGDash](https://github.com/eegdash/EEGDash) - Main EEGDash repository with ingestion scripts
