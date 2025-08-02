
# 🔍 IUPAC Motif Search in FASTA Sequences

This repository contains a Python script to search for motifs using IUPAC degenerate nucleotide codes in a FASTA-formatted sequence. It translates the IUPAC motif into a regular expression and identifies all occurrences with their approximate line positions.

---

## 🧬 Key Features

- Supports all IUPAC codes (`R`, `Y`, `S`, `W`, `K`, `M`, `B`, `D`, `H`, `V`)
- Converts motif into Python regex
- Parses raw FASTA and searches across the entire sequence
- Reports match locations and counts


## ▶️ Usage

### 1. 📥 Prepare Your FASTA File

Save your DNA sequence in a plain text FASTA format:

```

> ExampleSequence
> AGCTAGCTGATCGTACGTAGCTAGCTAGCTGATCG...

````

Ensure it is saved as `sequence.fasta` or modify the filename in the script.

---

### 2. ⚙️ Customize the Motif

Edit the `motif_search.py` script and replace the motif of interest:

```python
pattern = translate("ARVTCA.ARKTCA")  # Replace with your IUPAC motif
````

---

### 3. 🚀 Run the Script

```bash
python motif_search.py
```

---

## 📋 Sample Output

```text
Number of sequences pre-processed: 1
ARATCAAGKTCA found at line 35
ARCTCACGKTCA found at line 68
Total Matches: 2
```

> Line number is calculated assuming \~72 bases per line (FASTA convention)

---

## 📘 IUPAC Code Reference

| Code | Meaning    |
| ---- | ---------- |
| R    | A or G     |
| Y    | C or T     |
| S    | G or C     |
| W    | A or T     |
| K    | G or T     |
| M    | A or C     |
| B    | C, G, or T |
| D    | A, G, or T |
| H    | A, C, or T |
| V    | A, C, or G |

---

## 📎 Notes

* Assumes single sequence in FASTA file without headers or newlines between sequences.
* Works well for scanning long DNA sequences with degenerate motifs.
* You can adjust the line-length assumption in the script (default: 72) for different formats.



Let me know if you also want a `.gitignore`, sample FASTA file, or the Python script saved as a downloadable file.
```
