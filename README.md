# OwlLookup

GIS-first wildlife intelligence platform for spatiotemporal owl habitat analysis.
OwlLookup analyzes owl sightings alongside environmental stressors (land use, light pollution, weather) to surface habitat hotspots, decline zones, and long-term trends using PostGIS + PyQGIS.
This is a data product, not a visualization toy.

## Objective

Answer one question, unambiguously:
- Where are owl habitats changing, why, and since when?
- Success = reproducible, data-driven insights.

## Tech Stack

Backend: FastAPI
GIS Engine: PyQGIS
Database: PostgreSQL + PostGIS
Frontend: Leaflet.js, Plotly.js, TailwindCSS
Modeling: DBSCAN, ST-DBSCAN, Poisson / GAM
Formats: GeoJSON, CSV
Explainability beats novelty. No black boxes.

## Core Features (MVP)

Owl sightings analysis by species, season, night-hour
Habitat enrichment using:
- Land cover
- Light pollution
- Urban proximity
- Weather proxies
- Spatiotemporal hotspot detection
- Year-over-year habitat change tracking
- Exportable datasets and map layers

## PyQGIS as the Core

All spatial intelligence is computed via PyQGIS:
- Spatial joins and buffering
- Raster sampling
- Density estimation
- Seasonal slicing
- GeoJSON generation

If PyQGIS can’t derive it, it doesn’t ship.

## Modeling Philosophy

Clustering: DBSCAN / ST-DBSCAN
Regression: Poisson / GAM
Goal: signal detection, not prediction theater
Every metric must be traceable back to raw data.

## Non-Goals

- ❌ Mobile apps
- ❌ Social or crowdsourced features
- ❌ Manual labeling
- ❌ Generative narration

This is an analytical system, not content.

## Hosting Status

A hosted version of OwlLookup is planned for a later phase.
Current focus:
- data quality
- spatial rigor
- analytical signal strength

Deployment, scaling, and infrastructure hardening are intentionally deferred.

## Project Status

MVP in active development.
Expect rapid iteration and schema evolution.
Stability follows validated signal quality.