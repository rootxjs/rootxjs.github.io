---
title: "gRPC Goat - An intentionally vulnerable gRPC Security Lab"
description: "A comprehensive Lab for learning and testing gRPC security vulnerabilities."
publishDate: 2025-09-17
tags: ["grpc-goat", "vulnerable-lab", "tutorial", "security-lab"]
draft: false
comment: true
---

# Launching gRPC Goat

Hi, I'm JS aka @rootxjs launching **gRPC Goat** - an intentionally vulnerable gRPC application for learning and testing gRPC security vulnerabilities.

## Background

gRPC has become increasingly popular in microservices architectures, but security testing approaches differ significantly from traditional REST APIs. The binary protocol format and HTTP/2 transport layer introduce specific challenges:

- Standard web testing tools require adaptation for Protocol Buffers
- HTTP/2 multiplexing creates different attack vectors than HTTP/1.1
- gRPC reflection services can inadvertently expose service definitions
- Authentication and authorization patterns vary across implementations

## Repository

https://github.com/rootxjs/grpc-goat/

## Documentation

https://rootxjs.github.io/docs/grpc_goat_docs/getting-started/

## Labs Overview

The project includes 9 labs covering common gRPC security vulnerabilities:

- gRPC Reflection Enabled
- Plaintext gRPC
- Insecure TLS
- Arbitrary mTLS
- mTLS Subject Validation
- Unix Socket World Writable
- SQL Injection
- Command Injection
- Server-Side Request Forgery

Each lab contains a realistic vulnerability with detailed exploitation documentation and mitigation guidance.

## Motivation

While excellent vulnerable applications exist for web security learning (DVWA, WebGoat), the gRPC ecosystem lacked a comprehensive security lab. During penetration testing engagements, I encountered gRPC services but had limited resources for practicing attack techniques specific to this protocol.

gRPC Goat addresses this gap by providing hands-on experience with vulnerabilities commonly found in production gRPC implementations - from basic misconfigurations to complex implementation flaws.

## Getting Started

```bash
git clone https://github.com/rootxjs/grpc-goat.git
cd grpc-goat
docker-compose up -d
```

Each lab runs on a dedicated port with comprehensive documentation covering exploitation techniques and defensive measures.

Whether you're conducting gRPC security assessments or exploring modern API security, gRPC Goat provides practical experience with real-world vulnerability scenarios.

Keep Learning!