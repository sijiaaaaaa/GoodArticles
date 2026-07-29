
## Specification comparison: every GPU side by side

*Per-GPU dense (non-sparsity) specifications from official datasheets.*

| Spec | H100 SXM5 | H200 SXM | B200 | MI300X | MI325X | MI350X/355X |
|---|---:|---:|---:|---:|---:|---:|
| **Architecture** | Hopper | Hopper | Blackwell | CDNA 3 | CDNA 3 | CDNA 4 |
| **Process node** | TSMC 4N | TSMC 4N | TSMC 4NP | 5nm/6nm | 5nm/6nm | TSMC 3nm |
| **Transistors** | 80B | 80B | 208B (dual-die) | 153B (chiplets) | ~153B | 185B |
| **BF16 dense TFLOPs** | 989 | 989 | 2,250 | 1,307 | 1,307 | ~2,300 |
| **FP8 dense TFLOPs** | 1,979 | 1,979 | **4,500** | 2,615 | 2,615 | **~4,600** |
| **FP4 dense TFLOPs** | N/A | N/A | 9,000 | N/A | N/A | Supported |
| **HBM type** | HBM3 | HBM3e | HBM3e | HBM3 | HBM3E | HBM3E |
| **HBM capacity** | 80 GB | 141 GB | 192 GB | 192 GB | 256 GB | **288 GB** |
| **HBM bandwidth** | 3.35 TB/s | 4.8 TB/s | **8.0 TB/s** | 5.3 TB/s | 6.0 TB/s | **8.0 TB/s** |
| **Interconnect** | NVLink 4.0 | NVLink 4.0 | **NVLink 5.0** | Infinity Fabric | IF 4th Gen | IF 4th Gen |
| **Per-GPU link BW** | 900 GB/s | 900 GB/s | **1.8 TB/s** | ~128 GB/s p2p | ~128 GB/s p2p | TBD |
| **TDP** | 700W | 700W | 1,000W | 750W | 1,000W | 750–1,400W |
| **Launch date** | H1 2023 | Q2 2024 | 2025 | Dec 2023 | Oct 2024 | Mid-2025 |
| **Est. unit price** | $25–40K | $30–40K | $30–40K | **$10–15K** | ~$15–20K | ~$20–30K |
