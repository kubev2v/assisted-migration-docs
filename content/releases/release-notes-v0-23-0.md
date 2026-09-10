---
title: "release notes v0.23.0"
linkTitle: "release notes v0.23.0"
date: 2026-09-09
type: docs
---

# OpenShift Migration Advisor — release notes — `v0.23.0`

Compare: `v0.22.0` → `v0.23.0`

## Appliance changes

### Features
- Added RVTools standalone mode with direct .xlsx file upload and offline report generation
- Added support for downloading and uploading complete inventory bundles with group subsets for disconnected environments

### API changes (not yet available in the UI)
- Added vmCount field to groups list API to eliminate redundant per-group lookups

### Fixes
- Improved vCenter permission error messages with actionable guidance when credentials lack sufficient access
- Fixed Fault Tolerance status incorrectly reporting as enabled for all VMs
- Fixed active tab not persisting when switching between clusters in VM and Group detail pages
- Fixed issue counts in the Virtual Machines table not being clickable to drill down into issues
- Fixed inventory status prematurely showing as collected before database writes completed
- Fixed stale group counts and agent status due to manual state synchronization issues
- Added select-all checkbox to application VM drawer for bulk selection

## Console changes

### Features
- Added support for downloading and uploading complete inventory bundles with group subsets for disconnected environments

### API changes (not yet available in the UI)
- Added vCenter-level complexity and migration time estimation endpoints (clusterId now optional)
- Added totalWithRDM field to inventory VMs for tracking Raw Device Mapping disk usage

### Fixes
- Fixed Fault Tolerance status incorrectly reporting as enabled for all VMs
- Fixed OS support tier classification inconsistencies for Windows 10/11 in example reports
