---
name:          "SPEC.md"
description:   "MyTeleBot Mock Target 技術規格文件"
created_date:  "2026/06/18 10:00:00"
modified_date: "2026/06/18 10:00:00"
project_version: "0.2.1"
document_version: "1.0.0"
agent_sign: ['human/mimas', 'gemini cli']
---
# Specification

## 概述
MyTeleBot Mock Target 是一個基於 FastAPI 的 HTTP 伺服器，模擬 MyTeleBot 的目標端點。

## 核心功能
- 接收並記錄 HTTP 請求（Method, Path, Headers, Body）。
- 模擬多種回應模式：`success`, `business_error`, `http_error`, `timeout`。
- 支援多種認證方式：`none`, `bearer`, `header`, `query`, `hmac`。
- 提供管理端點以查看請求記錄及切換配置。

## 技術棧
- Python 3.9+
- FastAPI
- Uvicorn
- HTTPX (用於自喚醒任務)
