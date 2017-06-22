---
title: \LaTeX
author: Auriza Akbar
institute: Ilmu Komputer IPB
date: 2017
header-includes:
- \usepackage{booktabs}
- \hypersetup{colorlinks=true,linkcolor=.}
- \renewcommand{\figurename}{Gambar}
- \renewcommand{\tablename}{Tabel}
---

# \TeX

## Pendahuluan

- \TeX = "technical text"
- bahasa untuk menyiapkan dokumen teks
- dibuat oleh Knuth (1978) untuk mencetak bukunya
- dikembangkan oleh Lamport (1985) menjadi \LaTeX


## Mengapa \LaTeX?

- *free* dan *open format*
- hasil profesional berkualitas tinggi
- mudah mengatur struktur yang kompleks
    - daftar isi, catatan kaki, bibliografi, indeks, ...
- banyak buku dan jurnal memakai \LaTeX


## Instalasi \LaTeX

Windows
:   [MikTeX](http://miktex.org/download)

Linux
:   `apt install texlive`

*Online*
:   [sharelatex.com](http://sharelatex.com)


## Kerangka Dasar

```latex
\documentclass{article}     % preamble

\begin{document}            % document

    Hello world!

\end{document}
```

### Kompilasi

Simpan dalam *file* `.tex`, lalu *compile* dengan `pdflatex`.
Hasil kompilasi berupa *file* PDF.

```bash
$ pdflatex file.tex
```

# Preamble

## Kelas Dokumen

`\documentclass[options]{class}`{.latex}

- `class`
    - `book`
    - `article`
    - `report`
    - `letter`
    - `beamer`
- `options`
    - `10pt`, `11pt`, `12pt`
    - `a4paper`, `letterpaper`
    - `twoside`, `twocolumn`


## Paket Tambahan

`\usepackage[options]{package}`{.latex}

- fungsi tambahan untuk dokumen
- contoh:
    - `\usepackage{graphicx}`{.latex}
    - `\usepackage{booktabs}`{.latex}
    - `\usepackage{amsmath}`{.latex}


## Metadata

~~~latex
\title{...}

\author{...}

\date{...}
~~~

# Document

## Judul dan Abstrak

~~~latex
\maketitle

\begin{abstract}        % khusus report dan article
    ...
\end{abstract}
~~~


## Bagian

~~~latex
\part{...}              % khusus book

\chapter{...}           % khusus book dan report

\section{...}

\subsection{...}

\subsubsection{...}

\paragraph{...}

\subparagraph{...}
~~~

## Paragraf

- paragraf ditulis langsung tanpa perintah khusus
- satu baris kosong memisahkan antar-paragraf

## Contoh

```latex
\documentclass[a4paper]{article}
\usepackage{graphicx}

\title{Pengenalan \LaTeX}
\author{Auriza Akbar}
\date{2017}

\begin{document}
  \maketitle

  \section{Pendahuluan}

    \LaTeX adalah bahasa untuk menyiapkan dokumen teks.

\end{document}
```

## Daftar Isi, Gambar, dan Tabel

~~~latex
\tableofcontents

\listoffigures

\listoftables
~~~


## Format Teks

Perintah                     Keluaran
-------                      ------
`\textnormal{...}`{.latex}   \textnormal{Normal}
`\emph{...}`{.latex}         \emph{Emphasis}
`\textrm{...}`{.latex}       \textrm{Roman family}
`\textsf{...}`{.latex}       \textsf{Sans-serif family}
`\texttt{...}`{.latex}       \texttt{Teletype family}
`\textbf{...}`{.latex}       \textbf{Bold face}
`\textit{...}`{.latex}       \textit{Italic}
`\textsc{...}`{.latex}       \textsc{SmallCaps}
`\underline{...}`{.latex}    \underline{Underline}
`\tiny{...}`{.latex}         \tiny{Tiny}
`\small{...}`{.latex}        \small{Small}
`\large{...}`{.latex}        \large{Large}


# List

## List Tanpa Nomor

~~~latex
\begin{itemize}
  \item The first item
  \item The second item
  \item The third
\end{itemize}
~~~

\begin{itemize}
  \item The first item
  \item The second item
  \item The third
\end{itemize}

## List Bernomor

~~~latex
\begin{enumerate}
  \item The first item
  \item The second item
  \item The third
\end{enumerate}
~~~

\begin{enumerate}
  \item The first item
  \item The second item
  \item The third
\end{enumerate}

## List Deskripsi

~~~latex
\begin{description}
  \item[First] The first item
  \item[Second] The second item
  \item[Third] The third
\end{description}
~~~

\begin{description}
  \item[First] The first item
  \item[Second] The second item
  \item[Third] The third
\end{description}


## List Bersarang

~~~latex
\begin{enumerate}
  \item The first item
    \begin{enumerate}
      \item Nested item 1
      \item Nested item 2
    \end{enumerate}
  \item The second item
  \item The third item
\end{enumerate}
~~~

\begin{enumerate}
  \item The first item
  \begin{enumerate}
    \item Nested item 1
    \item Nested item 2
  \end{enumerate}
  \item The second item
  \item The third item
\end{enumerate}

# Persamaan Matematika

## Cara Penulisan

- *inline*: diletakkan di dalam tubuh teks
    - `$...$`{.latex}

- *displayed*: diletakkan pada baris tersendiri
    - `$$...$$`{.latex}

- *numbered*: diletakkan pada baris tersendiri dan bernomor
    - `\begin{equation}...\end{equation}`{.latex}

- contoh:
    ```latex
    \begin{equation}
      \forall x \in X, \quad \exists y \le \epsilon
    \end{equation}
    ```

\begin{equation}
  \forall x \in X, \quad \exists y \le \epsilon
\end{equation}


## Huruf Yunani

Perintah                Keluaran
-------                 ------
`\alpha`{.latex}        $\alpha$
`\beta`{.latex}         $\beta$
`\delta`{.latex}        $\delta$
`\Delta`{.latex}        $\Delta$
`\gamma`{.latex}        $\gamma$
`\kappa`{.latex}        $\kappa$
`\lambda`{.latex}       $\lambda$
`\mu`{.latex}           $\mu$
`\phi`{.latex}          $\phi$
`\pi`{.latex}           $\pi$
`\rho`{.latex}          $\rho$
`\sigma`{.latex}        $\sigma$
`\theta`{.latex}        $\theta$
`\Theta`{.latex}        $\Theta$

## Himpunan

Perintah                Keluaran
-------                 ------
`\in`{.latex}           $\in$
`\not\in`{.latex}       $\not\in$
`\subset`{.latex}       $\subset$
`\subseteq`{.latex}     $\subseteq$
`\not\subset`{.latex}   $\not\subset$
`\supset`{.latex}       $\supset$
`\cup`{.latex}          $\cup$
`\cap`{.latex}          $\cap$
`\emptyset`{.latex}     $\emptyset$


## Indeks dan Pangkat

```latex
$$ k_{n+1} = n^2 + k_n^2 - k_{n-1} $$
```

$$k_{n+1} = n^2 + k_n^2 - k_{n-1}$$

```latex
$$ n^{22} $$
```

$$n^{22}$$


## Fungsi

```latex
$$ \cos (2\theta) = \cos^2 \theta - \sin^2 \theta $$
```

$$\cos (2\theta) = \cos^2 \theta - \sin^2 \theta$$

```latex
$$ \lim_{x \to \infty} \exp(-x) = 0 $$
```

$$\lim_{x \to \infty} \exp(-x) = 0$$


## Pecahan

```latex
$$ \frac{n!}{k!(n-k)!} = \binom{n}{k} $$
```

$$\frac{n!}{k!(n-k)!} = \binom{n}{k}$$

```latex
$$ \frac{\frac{1}{x} + \frac{1}{y}}
        {y-z} $$
```

$$\frac{\frac{1}{x} + \frac{1}{y}}
      {y-z}$$


## Akar

```latex
$$ \sqrt{\frac{a}{b}} $$
```

$$\sqrt{\frac{a}{b}}$$

```latex
$$ \sqrt[n]{1 + x + x^2 + x^3 + \cdots} $$
```

$$\sqrt[n]{1 + x + x^2 + x^3 + \cdots}$$


## *Sum*, *Product*, dan Integral

```latex
$$ \sum_{i=1}^{10} t_i $$
```

$$\sum_{i=1}^{10} t_i$$

```latex
$$ \prod_{n=1}^\infty a_n $$
```

$$\prod_{n=1}^\infty a_n$$

```latex
$$ \int_a^b e^{-x}\,dx $$
```

$$\int_a^b e^{-x}\,dx$$


## *Cases*

```latex
%\usepackage{amsmath}

\begin{equation}
  u(x) =
    \begin{cases}
      \exp{x} & \text{if } x \ge 0 \\
      1       & \text{if } x < 0
    \end{cases}
\end{equation}
```

\begin{equation}
  u(x) =
    \begin{cases}
      \exp{x} & \text{if } x \ge 0 \\
      1       & \text{if } x < 0
    \end{cases}
\end{equation}

## *Multiline Split*

```latex
%\usepackage{amsmath}

\begin{equation}
  \begin{split}
    A & = \frac{\pi r^2}{2}   \\
      & = \frac{1}{2} \pi r^2
  \end{split}
\end{equation}
```

\begin{equation}
  \begin{split}
    A & = \frac{\pi r^2}{2} \\
      & = \frac{1}{2} \pi r^2
  \end{split}
\end{equation}

## Matriks

```latex
$$ M = \left[
         \begin{array}{ccc}
           1 & 2 & 3 \\
           4 & 5 & 6 \\
           7 & 8 & 9
         \end{array}
       \right] $$
```

$$M = \left[
        \begin{array}{ccc}
          1 & 2 & 3 \\
          4 & 5 & 6 \\
          7 & 8 & 9
        \end{array}
      \right]$$


# Tabel dan Gambar

## Elemen *Float*

- tabel dan gambar: elemen *float*
    - tidak boleh terpotong beda halaman
- posisi dapat diberikan pilihan:
    - `h`: *here*
    - `b`: *bottom*
    - `t`: *top*
    - `p`: *page*
- dapat diberi *caption* bernomor
- dapat diberi label untuk referensi

## Tabel

```latex
%\usepackage{booktabs}

Nilai mahasiswa dapat dilihat pada Tabel \ref{tbl.nilai}.

\begin{table}[tb]
  \caption{Nilai AJK.}
  \label{tbl.nilai}
  \begin{tabular}{llc}            \toprule
    NIM       & Nama   & Nilai \\ \midrule
    G65114071 & Auriza & 75    \\
    G65114081 & Auzi   & 80    \\ \bottomrule
  \end{tabular}
\end{table}
```

---

Nilai mahasiswa dapat dilihat pada Tabel \ref{tbl.nilai}.

\begin{table}[tb]
  \caption{Nilai AJK.}
  \label{tbl.nilai}
  \begin{tabular}{llc}            \toprule
    NIM       & Nama   & Nilai \\ \midrule
    G65114071 & Auriza & 75    \\
    G65114081 & Auzi   & 80    \\ \bottomrule
  \end{tabular}
\end{table}

## Gambar

```latex
%\usepackage{graphicx}

Peta dengan proyeksi \textit{butterfly} dapat dilihat
pada Gambar \ref{fig.peta}.

\begin{figure}[tb]
  \centering
  \includegraphics[width=0.9\textwidth]{earth}
  \caption{Proyeksi \textit{butterfly}.}
  \label{fig.peta}
\end{figure}
```

---

Peta dengan proyeksi \textit{butterfly} dapat dilihat
pada Gambar \ref{fig.peta}.

\begin{figure}[tb]
  \centering
  \includegraphics[width=0.9\textwidth]{earth}
  \caption{Proyeksi \textit{butterfly}.}
  \label{fig.peta}
\end{figure}


# FIN
