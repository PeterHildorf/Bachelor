# Diplomingeniørprojekt – LaTeX-projekt

## Opsætning på Overleaf

1. Gå til [overleaf.com](https://www.overleaf.com) og log ind
2. Klik **New Project → Upload Project**
3. Upload denne ZIP-fil
4. Overleaf åbner projektet automatisk
5. Sæt **compiler til pdfLaTeX** (Project Settings → Compiler)
6. Tryk **Recompile** – projektet skulle kompilere uden fejl

## Filstruktur

```
main.tex                    ← Hoveddokument (pakker, titelside, TOC)
references.bib              ← Alle litteraturhenvisninger (BibTeX)
chapters/
  01_introduction.tex       ← Kapitel 1: Introduktion  ✅
  02_analysis.tex           ← Kapitel 2: Analyse & krav ✅
  03_methodology.tex        ← Kapitel 3: Metodologi (kommer)
  04_architecture.tex       ← Kapitel 4: Systemdesign (kommer)
  05_ux_design.tex          ← Kapitel 5: UI/UX Design (kommer)
  06_implementation.tex     ← Kapitel 6: Implementering (kommer)
  07_testing.tex            ← Kapitel 7: Test & evaluering (kommer)
  08_discussion.tex         ← Kapitel 8: Diskussion (kommer)
  09_conclusion.tex         ← Kapitel 9: Konklusion (kommer)
figures/                    ← Gem alle billeder her (PNG/PDF anbefales)
```

## Tilføj figurer

Gem billeder i `figures/` og indsæt dem med:

```latex
\begin{figure}[H]
  \centering
  \includegraphics[width=0.8\textwidth]{figures/dit_billede}
  \caption{Din billedtekst}
  \label{fig:dit-label}
\end{figure}
```

## Kodelistings

Brug de definerede sprog i main.tex:

```latex
% Swift-kode
\begin{lstlisting}[language=Swift, caption={ChatViewModel – extract}]
func extractImage(_ imageData: Data) async {
    // din kode her
}
\end{lstlisting}

% Go-kode  
\begin{lstlisting}[language=Go, caption={extract.go handler}]
func NewExtractHandler(...) http.HandlerFunc {
    // din kode her
}
\end{lstlisting}
```

## Tilføj referencer

Tilføj nye kilder i `references.bib` og brug dem i teksten:

```latex
Som beskrevet i~\cite{google_vision} anvender systemet...
```

## DTU-logo

Gem `dtu_logo.png` i `figures/` og fjern kommentartegnet
på logo-linjen i `main.tex` for at vise DTU-logoet på titelsiden.
