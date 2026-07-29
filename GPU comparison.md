\documentclass[10pt]{article}

\usepackage[margin=0.55in]{geometry}
\usepackage{booktabs}
\usepackage{array}
\usepackage{adjustbox}
\usepackage[table]{xcolor}
\usepackage{caption}
\usepackage{pdflscape}
\usepackage[T1]{fontenc}
\usepackage{lmodern}

\definecolor{headerblue}{HTML}{EAF1F8}
\definecolor{rowgray}{HTML}{F7F9FC}
\definecolor{highlightblue}{HTML}{0B57D0}

\newcommand{\best}[1]{\textbf{\textcolor{highlightblue}{#1}}}
\newcommand{\gpurow}[1]{\textbf{#1}}

\begin{document}

\begin{landscape}

\begin{table}[htbp]
\centering

\caption{Specification comparison: every GPU side by side}
\label{tab:gpu-spec-comparison}

\caption*{
\footnotesize
Per-GPU dense (non-sparsity) specifications from official datasheets.
}

\small
\setlength{\tabcolsep}{5pt}
\renewcommand{\arraystretch}{1.35}

\begin{adjustbox}{max width=\linewidth}
\begin{tabular}{
    >{\raggedright\arraybackslash}p{2.9cm}
    *{6}{>{\centering\arraybackslash}p{2.15cm}}
}
\toprule

\rowcolor{headerblue}
\textbf{Spec}
& \textbf{H100 SXM5}
& \textbf{H200 SXM}
& \textbf{B200}
& \textbf{MI300X}
& \textbf{MI325X}
& \textbf{MI350X/355X} \\

\midrule

\gpurow{Architecture}
& Hopper
& Hopper
& Blackwell
& CDNA 3
& CDNA 3
& CDNA 4 \\

\rowcolor{rowgray}
\gpurow{Process node}
& TSMC 4N
& TSMC 4N
& TSMC 4NP
& 5nm/6nm
& 5nm/6nm
& TSMC 3nm \\

\gpurow{Transistors}
& 80B
& 80B
& 208B (dual-die)
& 153B (chiplets)
& $\sim$153B
& 185B \\

\rowcolor{rowgray}
\gpurow{BF16 dense TFLOPs}
& 989
& 989
& 2,250
& 1,307
& 1,307
& $\sim$2,300 \\

\gpurow{FP8 dense TFLOPs}
& 1,979
& 1,979
& \best{4,500}
& 2,615
& 2,615
& \textbf{$\sim$4,600} \\

\rowcolor{rowgray}
\gpurow{FP4 dense TFLOPs}
& N/A
& N/A
& 9,000
& N/A
& N/A
& Supported \\

\gpurow{HBM type}
& HBM3
& HBM3e
& HBM3e
& HBM3
& HBM3E
& HBM3E \\

\rowcolor{rowgray}
\gpurow{HBM capacity}
& 80 GB
& 141 GB
& 192 GB
& 192 GB
& 256 GB
& \best{288 GB} \\

\gpurow{HBM bandwidth}
& 3.35 TB/s
& 4.8 TB/s
& \best{8.0 TB/s}
& 5.3 TB/s
& 6.0 TB/s
& \best{8.0 TB/s} \\

\rowcolor{rowgray}
\gpurow{Interconnect}
& NVLink 4.0
& NVLink 4.0
& \textbf{NVLink 5.0}
& Infinity Fabric
& IF 4th Gen
& IF 4th Gen \\

\gpurow{Per-GPU link BW}
& 900 GB/s
& 900 GB/s
& \best{1.8 TB/s}
& $\sim$128 GB/s p2p
& $\sim$128 GB/s p2p
& TBD \\

\rowcolor{rowgray}
\gpurow{TDP}
& 700W
& 700W
& 1,000W
& 750W
& 1,000W
& 750--1,400W \\

\gpurow{Launch date}
& H1 2023
& Q2 2024
& 2025
& Dec 2023
& Oct 2024
& Mid-2025 \\

\rowcolor{rowgray}
\gpurow{Est. unit price}
& \$25--40K
& \$30--40K
& \$30--40K
& \best{\$10--15K}
& $\sim$\$15--20K
& $\sim$\$20--30K \\

\bottomrule
\end{tabular}
\end{adjustbox}

\end{table}

\end{landscape}

\end{document}
