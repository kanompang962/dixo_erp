# 🚀 Dixo Stack — ERP Platform

[![Build](https://img.shields.io/badge/build-pipeline-blue)]()
[![Coverage](https://img.shields.io/badge/coverage---yellow)]()
[![License](https://img.shields.io/badge/license-MIT-green)]()
[![Tech](https://img.shields.io/badge/frontend-Angular%2020-red)]()
[![Tech](https://img.shields.io/badge/backend-.NET%208-007ACC)]()

**Dixo Stack** คือระบบ ERP แบบโมดูลาร์ ออกแบบมาให้ใช้งานได้จริง (Inventory, Sales, Accounting, HR ฯลฯ) โดยใช้เทคโนโลยีสมัยใหม่ — Angular 20 (frontend), .NET 8 (backend), ใช้ TiDB Cloud เป็นฐานข้อมูลหลัก และมี observability + CI/CD เต็มรูปแบบ

---

## 📌 สารบัญ
- [Highlights](#-highlights)
- [Architecture](#-architecture)
- [Folder structure (ตัวอย่าง)](#-folder-structure-ตัวอย่าง)
- [Quick start (สำหรับ dev)](#-quick-start-สำหรับ-dev)
- [Environment & Configuration](#-environment--configuration)
- [CI / CD](#-ci--cd)
- [Monitoring & Logging](#-monitoring--logging)
- [Testing](#-testing)
- [Pre-commit / Lint (Husky)](#-pre-commit--lint-husky)
- [Deployment (Docker + Nginx + Ubuntu)](#-deployment-docker--nginx--ubuntu)
- [Contributing](#-contributing)
- [Roadmap](#-roadmap)
- [License](#-license)

---

## ✨ Highlights
- Modular ERP (โมดูลแยก: Inventory, Sales, Accounting, HR)
- SPA frontend ด้วย **Angular 20**
- Backend API ด้วย **ASP.NET Core 8**
- Database: **TiDB Cloud** (Postgres-compatible/MySQL-compatible config แล้วแต่เลือก)
- Containerized: **Docker** + Compose
- CI/CD: **GitHub Actions**
- Observability: **Prometheus** + **Grafana**
- Unit & E2E tests: **Jest** (frontend), **dotnet test** (backend)
- Pre-commit hooks: **Husky**

---
## 📄 Pre-commit / Lint (Husky)
| Type         | ใช้ทำอะไร                                                        | ตัวอย่าง                                     |
| ------------ | --------------------------------------------------------------- | ------------------------------------------ |
| **feat**     | เพิ่ม **feature ใหม่**                                             | `feat(auth): add JWT login`                |
| **fix**      | แก้ **bug**                                                      | `fix(api): correct HTTP status code`       |
| **docs**     | เปลี่ยน **documentation** (README, wiki)                          | `docs(readme): update setup instructions`  |
| **style**    | **รูปแบบ code** (formatting, spacing, semicolons) ไม่กระทบ logic  | `style(frontend): fix indentation`         |
| **refactor** | เปลี่ยน **โค้ดแต่ behavior ไม่เปลี่ยน**                                | `refactor(api): restructure user service`  |
| **test**     | เพิ่ม/แก้ **unit test / e2e test**                                 | `test(auth): add login unit tests`         |
| **chore**    | งานอื่น ๆ เช่น **config, package update**                          | `chore(frontend): upgrade Angular to 20.1` |

ตัวอย่าง scope:
- frontend → Angular UI
- backend → .NET API
- auth → ระบบ login / JWT
- api → service / endpoint
- ui → layout, component, style

## 🏗️ Architecture

