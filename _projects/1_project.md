---
layout: page
title: Self Hosted Apps, Tools & Home Automation
description: HomeLabbing
img: assets/img/12.jpg
importance: 1
category: work
related_publications: false

---



# My Budget Home Lab & Self-Hosted Server Rack Setup

Over the years I’ve slowly built up a small home server rack that now runs most of my self-hosted services. Almost all of the equipment was either rescued from eWaste, repaired, repurposed, or purchased second-hand for cheap.

I enjoy giving old enterprise hardware a second life rather than letting it end up in landfill, and honestly, you can build an incredibly capable home lab on a very small budget if you’re willing to tinker.
## Table of Contents

- [Why I Self-Host](#why-i-self-host)
- [Core Infrastructure](#core-infrastructure)
  - [Proxmox VE](#1-proxmox-ve)
  - [Proxmox Backup Server](#2-proxmox-backup-server)
  - [Synology RackStation RS815+](#3-synology-rackstation-rs815-4--8tb-hdd)
- [Compute Hosts](#compute-hosts)
  - [HP Mini PC Cluster](#hp-mini-pc-cluster)
- [Self-Hosted Applications & Services](#self-hosted-applications--services)
  - [Paperless-ngx](#paperless-ngx)
  - [Syncthing](#syncthing)
  - [Ubuntu](#ubuntu)
  - [OpenClaw](#openclaw)
  - [UniFi](#unifi)
  - [Pi-hole](#pi-hole)
  - [Docker](#docker)
  - [Caddy](#caddy)
  - [Home Assistant](#home-assistant)
  - [Portainer](#portainer)
---

# Why I Self-Host

For me, self-hosting is a combination of:

* learning
* experimentation
* sustainability
* privacy
* problem solving

There’s something incredibly satisfying about building useful infrastructure from recycled hardware and keeping older equipment out of landfill.

It also proves that you don’t need expensive enterprise servers to build a capable and reliable home lab. A few secondhand mini PCs, some patience, and a willingness to learn can go a long way.

---

## Core Infrastructure

### 1. Proxmox VE

My main virtualization platform. I run Proxmox across a couple of HP Mini PCs which host all of my containers and virtual machines.

Proxmox has been incredibly stable and gives me enterprise evel virtualization features like:

* VM and container management
* Snapshots
* Backups
* High flexibility for self-hosting
* Easy web-based management

For a home lab, it’s hard to beat.

---

### 2. Proxmox Backup Server

I run Proxmox Backup Server virtually on my Synology RackStation.

This handles:

* Scheduled VM backups
* Deduplication
* Fast restores
* Backup verification

Having proper backups completely changes the confidence level when experimenting with selfhosted services.


---

### 3. Synology RackStation RS815+ (4 × 8TB HDD)

This is my main storage array.

Interestingly, I managed to pick this unit from work when they were removing them due to failure and I managed to pick them up. The failure was due to the well known Synology hardware issue related to circuit degradation. I repaired it myself by soldering in a simple 100-ohm resistor — an $8 fix that brought the entire RackStation back to life.

Moments like this are why I enjoy homelabbing so much:

* learning new skills
* repairing hardware
* reducing eWaste
* saving thousands of dollars

The RS815+ now continues to run reliably as part of my infrastructure.
The synology backs up to another unit at my parents home overnight to provide some redundancy
---

## Compute Hosts

### HP Mini PC Cluster

My workloads currently run on a couple of simple HP Mini PCs with the following specs:

* 6 × Intel Core i5-8500T CPUs @ 2.10GHz
* 8GB RAM
* 256GB SSD storage

These tiny machines are:

* power efficient
* quiet
* cheap to acquire second-hand
* surprisingly capable for virtualization

For most home lab workloads, they’re more than enough.

---

# Self-Hosted Applications & Services

Below are some of the applications and services currently running in my Proxmox environment.

---

### Paperless-ngx

A document management system that digitizes and organizes paperwork.

I use it to:

* scan invoices and receipts
* store warranties
* archive important documents
* make everything searchable with OCR

It has basically become my personal digital filing cabinet.

---

### Syncthing

An open-source file synchronization platform.

It securely syncs files between devices without relying on cloud providers. I use it for:

* automatic phone backups
* document syncing
* transferring files between systems

---

### Ubuntu

A general-purpose Linux VM used for testing, development, and running miscellaneous workloads.

Ubuntu is usually my default environment whenever I want to experiment with something new.

---

### OpenClaw

This was a open source AI model recently released. Not fully operational yet but its close


---

### UniFi

I self-host the UniFi Controller to manage my home networking equipment.

This gives me centralized management for:

* Wi-Fi access points
* VLANs
* network monitoring
* guest networks
* traffic visibility

---

### Pi-hole

A network-wide DNS ad blocker.

Pi-hole blocks ads and trackers across all devices in the house, improving:

* privacy
* browsing speed
* overall network cleanliness

It’s one of those tools that becomes impossible to live without once installed.

---

### Docker

Docker allows me to quickly deploy and manage lightweight applications in containers.

It makes experimenting with new services incredibly easy and keeps applications isolated and portable.

---

### Caddy

A modern web server and reverse proxy with automatic HTTPS support.
Mainly it provides SSL certificates to my domain which I use internally to access services without having to remember the IP:Port 
For example, I can access Proxmox via https://proxmox.mywebsite.com internally on my LAN

Caddy handles:

* reverse proxying
* SSL certificates
* secure access to internal services

The automatic certificate management is especially nice.

---

### Home Assistant

My smart home automation platform.

It ties together various smart devices around the house and allows for:

* automation routines
* energy monitoring
* dashboards
* smart lighting
* notifications

Self hosting it keeps everything local and under my control.

---

### Portainer

Provides a useful containerised tool to manage docker containers. I have some minor containers installed via Portainer, its an abolute gem of a tool.

---



