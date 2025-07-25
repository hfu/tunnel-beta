# 🇹🇱 S_0604-374 Dataset - PMTiles Viewer

A project to convert Esri File Geodatabase to PMTiles format vector tiles and display them interactively on the web using MapLibre GL JS.

## 📖 Overview

This project converts 20 layers contained in `S_0604-374.gdb` (Esri File Geodatabase) to PMTiles format and provides a web map viewer hosted on GitHub Pages. The conversion process is automated using a Makefile pipeline, with MapLibre GL styles generated from modular configuration files.

## 🚀 Quick Start

### 1. Check Dependencies

```bash
make check-deps
```

### 2. Generate PMTiles File

```bash
make build
```

### 3. Local Preview

```bash
make host
```

Access [localhost:8080](http://localhost:8080) in your browser.

## 🔧 Style Generation

The project uses modular configuration for MapLibre GL style generation. Key files include:

- `Colors.pkl`: Color definitions

- `Sources.pkl`: Data source configurations

- `LayerOrder.pkl`: Layer ordering rules

Run the following commands to validate and generate styles:

```bash
make validate-pkl
make generate-style
```

## 🎯 Makefile Commands

### Basic Commands

```bash
make                 # Execute PMTiles conversion + style generation
make host            # Host with Caddy server on localhost:8080
make clean           # Clean up generated files
```

### Development & Debug

```bash
make check-deps      # Check dependency tools
make validate-pkl    # Validate configuration syntax
make generate-style  # Generate style.json from configuration
```