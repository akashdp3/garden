---
status: In Progress
tags:
  - project
  - git
  - ai
  - microservices
---
# Gittr

## Overview

Gittr is a local-first Git and release management tool with dual purposes:

1. **For Developers**: Manage Git operations through an intuitive GUI
2. **For Managers**: Gain visibility into code changes with AI analysis and coordinate release management

**Core Problem**: In microservice teams, even small features require changes across 3-4 repositories. Managers/leads need to ensure every required change is merged (not one less, not one more) while coordinating UAT � Pilot � Production deployments safely.

## Technical Architecture

Three-tier layered architecture:

### Layer 1: Git Foundation (Data Source)
- Working Changes - Unstaged/staged files
- Commits - Full commit history
- Branches - Branch management and switching
- File Changes - Detailed file-level diffs
- Stashes - Work-in-progress storage

### Layer 2: Analysis & Review (Intelligence Layer)
- AI Change Analysis - Primary view with commit analysis, risk detection
- Risk Assessment - Aggregated view of all detected risks across repos
- Code Review - Manager verification and approval workflow
- Diff Inspector - Deep-dive inspection of specific changes

### Layer 3: Release Coordination (Orchestration Layer)
- Release Planning - Create and manage releases
- Deployment Order - Dependency-based deployment sequencing
- Env Variables - Environment variable tracking and verification
- Cross-Repo Verify - Ensure all required changes are present across repos
- Tags & Versions - Version tagging and management

## Tech Stack

- React
- TypeScript
- Tailwind CSS
- Lucide icons

## Current Status

**In Progress:**
- UI for working changes (Git Foundation Layer)

**Placeholder/Todo:**
- Most navigation items
- Risk Assessment view
- Release Coordination features

## AI Analysis Capabilities

The AI identifies:
- Missing environment variables
- Database migration risks
- Deployment order dependencies
- Configuration changes requiring coordination
- Breaking changes across microservices
- Security vulnerabilities
- Performance regressions

## User Workflow

1. Manager receives alert (e.g., "AI detected high-risk config change")
2. Navigate to Analysis & Review � Risk Assessment
3. Review AI-flagged issue
4. Drill down to Git Foundation � Commits to verify
5. Inspect diffs to confirm AI assessment
6. Navigate to Release Coordination � Cross-Repo Verify
7. Approve release or request fixes

## Next Development Priorities

1. Complete AI Change Analysis features (Layer 2)
2. Build Risk Assessment aggregation view (Layer 2)
3. Implement basic Git Foundation views (Layer 1) � **Current focus**
4. Add Release Coordination features (Layer 3)

## Today's Goal

- [ ] Create UI for working changes in gittr (Layer 1: Git Foundation)

## Notes

- Located at: [[99-Meta/claude.md]] for detailed context
