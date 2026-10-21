# Elk_Draw RDKit

Elk_Draw is an editor for chemical structures and reactions on Windows. **Elk_Draw RDKit** is its
light edition (ELG) together with QSAR/QSPR descriptors calculated by [RDKit](https://www.rdkit.org):
free for private use, teaching and non-commercial academic research (see [LICENSE.txt](LICENSE.txt)).

This repository only holds the downloads. Get the latest version under
**[Releases](../../releases)**.

## What Elk_Draw RDKit does

- Drawing structures, reactions, brackets, text and shapes; templates and a fragment library
  (rings, functional groups, protecting groups, reagents and solvents, macrocycles such as porphine
  and the cucurbit[n]urils, ferrocene).
- Properties panel: formula, molecular weight, exact mass, logP, TPSA, H-bond donors and acceptors,
  rotatable bonds, Fsp3, rule of five, SMILES; selected values can be inserted as text.
- **Analyze › Descriptors (RDKit)**: the 217 molecular descriptors of RDKit (as Python's
  `Descriptors.CalcMolDescriptors`; optionally the 192 AUTOCORR2D) for the selected structure or the whole
  drawing, by category, with search; copy the rows you see, or save them as a one-row CSV to build QSAR
  data sets.
- **Analyze › QSAR Data Set**: descriptors for every molecule of an SD file (its data fields, such as measured
  activities, become columns), a SMILES file or a CSV with a SMILES column, as one CSV table.
- **Analyze › QSAR Model**: multiple linear regression of a measured value on descriptors chosen stepwise by the
  cross-validated q² (leave-one-out): equation, R², q², RMSE, coefficients and a measured-vs-predicted plot;
  prediction for the drawn structure with an applicability-domain warning; models saved as `.qsar` files.
- Analyze menu: structure information, estimated physical properties (Joback), structure check, formula
  and geometry optimisation (force field).
- Structures in Microsoft Word: insert them, double-click to edit them in Elk_Draw.
- Files: Elk_Draw's own format and common chemistry formats (MOL/SDF, SMILES, CDXML and others);
  export as pictures.

The quantum-chemical calculations of the full edition (MOPAC, xtb, TD-DFT) and NMR prediction are
shown in the menus but are not part of this edition.

## Installing

Windows 10 or 11, 64-bit. Elk_Draw ELG and Elk_Draw RDKit can be installed side by side. Nothing else is needed: no .NET, no administrator rights.

- **Elk_Draw_RDKit.msi** – installer. Installs for your Windows user into
  `%LocalAppData%\Programs\Elk_Draw RDKit`, adds a Start menu and a desktop shortcut and registers
  Elk_Draw for Word. Remove it under *Settings › Apps*. A newer installer updates an older one.
  Settings are kept in `%APPDATA%\Elk_Draw`.
- **Elk_Draw_RDKit.zip** – portable copy. Unzip anywhere and start `Elk_Draw.exe`. Settings are kept in
  the `Data` folder next to the program. To use it with Word, run `Register in Word.cmd` once.

Windows may warn that the installer comes from an unknown publisher (it is not code-signed yet):
choose *More info › Run anyway*.

## Licence

Copyright © 2026 Oleksandr Karasyov. Free for private use, teaching and non-commercial academic
research; commercial use needs permission. The full terms (German, binding, and English) are in
[LICENSE.txt](LICENSE.txt). Components by others and their licences:
[THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md) and the [licenses](licenses) folder. RDKit (BSD 3-Clause),
RingDecomposerLib (BSD 3-Clause), Boost (Boost Software License) and Eigen (MPL-2.0) are inside
`rdkitcffi.dll`; Eigen's unmodified source is at https://gitlab.com/libeigen/eigen.

Contact: alexkarasyov0@gmail.com
