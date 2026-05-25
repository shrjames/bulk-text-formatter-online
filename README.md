# Bulk Text Formatter & Data Normalization Utility

A high-performance, 100% client-side text processing tool built for developers, QA engineers, and data analysts. This utility simplifies the unglamorous work of sanitizing messy raw data inputs, adjusting delimiters, and normalizng string formats before running integration tests or software pipelines.

## 🚀 Core Transformations
- **O(n) Linear Deduplication:** Instantly filters out duplicate entries in bulk lists without blocking the browser rendering thread.
- **Advanced Trimming & Cleansing:** Strips surrounding single/double quotes, collapses irregular inner whitespaces, and drops empty rows.
- **Custom Input/Output Mapping:** Seamlessly splits inputs via custom delimiters (escaped characters like `\n`, `\t` supported) and joins them via custom outputs.

## 🛠️ Performance & Architecture
TextForge leverages native browser JavaScript memory allocation optimization. Strings are immutable in JS, meaning traditional iterative loops create unnecessary memory overhead. This tool aggregates structural arrays prior to executing a unified `.join()` call, allowing multi-megabyte string normalization sequences to run smoothly inside a single sandboxed tab.

## 🔒 100% Local Privacy Guarantee
Data compliance is critical. This tool executes entirely within your browser's local sandbox memory. 
- Zero tracking or backend network telemetry.
- Zero external database storage.
- Safe for enterprise QA environments handling sensitive software testing configurations.
