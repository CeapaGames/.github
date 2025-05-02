# CeapaGames

CeapaGames is a modular game platform built for browser-based games with account-based access control, custom game instances, and isolated subdomains per title. The infrastructure emphasizes containerization, clean separation of frontend/backend concerns, and minimalistic, purposeful design.

## Repositories Overview

### 🧾 user-management
[![Spring Boot CI](https://github.com/CeapaGames/user-management/actions/workflows/ci.yml/badge.svg)](https://github.com/CeapaGames/user-management/actions/workflows/ci.yml)

Spring Boot service for authentication, registration, and token management.  
Handles user storage via MongoDB and supports login-based access to game subdomains.

### 🖥 main-page
[![Vite CI](https://github.com/CeapaGames/main-site/actions/workflows/ci.yml/badge.svg)](https://github.com/CeapaGames/main-site/actions/workflows/ci.yml)

React frontend (using Vite) for user login, registration, and access control.  
Acts as the entry point to the CeapaGames ecosystem.

### ⚙ infrastructure

Containerized setup for reverse proxy (Nginx), Cloudflare Tunnel, and service orchestration.  
Manages all routing between frontend and backend containers and ensures secure external access.  
Designed to run locally or deploy on lightweight devices like a Raspberry Pi.

## Architecture Highlights

- 🧩 **Frontend**: Vite + React, per-game containerization
- 🔒 **Backend**: Spring Boot, JWT security, user verification
- 🗃 **Database**: MongoDB (users, game state), Redis (future real-time support)
- 📦 **Containers**: Docker-managed services, with per-project builds
- 🌐 **Routing**: Nginx reverse proxy + Cloudflare Tunnel for secure access
- 🔁 **Access Control**: Auth-gated game subdomains (`gamea.ceapagames.com`, etc.)

---

Want to explore or contribute?  
Browse each repo or start at [ceapagames.com](https://ceapagames.com) (when live).
