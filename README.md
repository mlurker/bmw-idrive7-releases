# bmw-idrive7-releases

Public releases of the packages for the BMW iDrive 7 (MGU) **mgu Store**: Android Auto's map on the instrument
cluster and the HUD, and a few related tools. This repository holds **no source code**, only the published
packages. Its "Source code" archives on the release page contain just this README.

## What is in the release

The release named `catalog` holds `catalog.json` (the list the Store reads) and one package file per component:

| Package | Version | What |
|---|---|---|
| `cluster-render` | 10.10.10 | the renderer that draws on the cluster and the HUD |
| `waze-on-cluster` | 10.10.10 | captures the phone's map stream and feeds the renderer |
| `aa-on-cluster` | 0.11.0 | Android Auto's cluster map in the cluster's map area, or on the HUD |
| `hud-signals` | 0.0.9 | the car's turn signals, gear and ranges on the HUD |
| `aa_cluster_companion` | 0.9.0 | "AA Cluster Companion", the iDrive app that sets the above |

(Stable version of 2026-11-05. `catalog.json` is the authority for the current versions.)

## Add it to the car's Store

In the car's Store: Settings, Sources, add a GitHub source `mlurker/bmw-idrive7-releases`, channel **Releases**.
Install in this order: mgu-deploy (the Store's own), cluster-render, waze-on-cluster, aa-on-cluster, then the
companion app. hud-signals needs only cluster-render. Then restart the head unit.

## Read this first

- Tested only on a BMW X5 G05 (iDrive 7, MGU P18_23w44).
- These tools change files on the head unit and add services to it. Use them at your own risk, and keep a backup.
- Each tool package carries its own `LICENSE` file.
