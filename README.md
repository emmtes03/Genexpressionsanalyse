# Genexpressionsanalyse 

Dieses Repository enthält die Dateien und Ergebnisse des Projekts zur Genexpressionsanalyse im Wintersemester 2023/24.

## Projektstruktur

- **`Projekt2_Teil_1.pdf`**: Enthält die Ergebnisse des ersten Teils des Projekts.
- **`Projekt2_Pipeline_drawio`**: Diagramm, das die Pipeline zur Verarbeitung der Daten darstellt.
- **`Projekt2_Teil_2.html`**: HTML-Dokument, das die Erklärungen, den Code und die Ergebnisse des 2. Teil des Projekts enthält.
- **`Projekt2_Teil_2.Rmd`**: RMarkdown-Skript, das den gesamten Analyseprozess des 2. Teils des Projekts dokumentiert.

## Aufgabenstellungen

### Teil 1 - Linux-basierte Analysen

1. **Datenursprung**: Bestimmung des Organismus und der Vergleichsgruppen anhand der RNA-Seq-Daten mit der Accession-Number SRS307298.

2. **Daten Download**: Installation des SRA-Toolkits und Herunterladen der relevanten Datensätze.

3. **FastQC**: Qualitätsüberprüfung der Daten mittels FastQC.

4. **Qualität verbessern**: Installation von `cutadapt` und `trim-galore` zur Verbesserung der Datenqualität und anschließende Qualitätsüberprüfung.

5. **Read Mapping**: Mapping der Reads auf das Referenzgenom der Hefe mittels Bowtie2.

6. **Von Alignments zu Genen**: Konvertierung und Verarbeitung der Mappings zu genbasierten Reads mit `samtools` und `bedtools`.

7. **Pipeline Darstellung**: Graphische Darstellung der gesamten Pipeline.

### Teil 2 - Datenanalyse in R

7. **Daten vorbereiten**: Einlesen der `Bedtools_out_all.bed` Datei in R und Erstellung eines Dataframes.

8. **DESeq2 Normalisierung**: Normalisierung der Daten mit DESeq2 und Durchführung verschiedener Analysen, einschließlich PCA und differentiell exprimierter Gene.

9. **PCA in R**: Durchführung einer Hauptkomponentenanalyse (PCA) zur Überprüfung der Datenverteilung.

10. **Differentiell exprimierte Gene**: Identifizierung und Analyse von differentiell exprimierten Genen.

11. **Heatmaps**: Erstellung von Heatmaps für die identifizierten Gene.

12. **Funktionale Analyse**: Durchführung einer GO Enrichment Analyse für die identifizierten Gene.

## Voraussetzungen

- **R** und **RStudio**
- **Bioconductor** Pakete: `DESeq2`, `ggplot2`
- **SRA-Toolkit**
- **FastQC**
- **cutadapt**
- **trim-galore**
- **Bowtie2**
- **samtools**
- **bedtools**

## Installation

1. Klone das Repository:
    ```bash
    git clone https://github.com/emmtes03/Genexpressionsanalyse.git
    ```

2. Installiere die notwendigen R-Pakete:
    ```r
    if (!requireNamespace("BiocManager", quietly = TRUE))
        install.packages("BiocManager")
    BiocManager::install("DESeq2")
    install.packages("ggplot2")
    ```

3. Folge den Anweisungen in der RMarkdown Datei `script.Rmd`, um die Analysen durchzuführen.

## Nutzung

- Die Dateien `Projekt2_Teil_1.pdf`, `Projekt2_Pipeline_drawio` und `script.Rmd`enthalten den vollständigen Code und/oder die Beschreibung des Analyseprozesses.
- Öffne `Projekt2_Teil_2.html`, um die Ergebnisse und Erklärungen der Analysen des 2. Teils zu betrachten.

## Autoren

- Erstellt von Emmelie für die THM im Rahmen des Wintersemesters 2023/24.

