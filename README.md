# 🧠 EEG Disorder Detector

An open-source Python-based EEG signal analysis pipeline that uses advanced signal processing techniques to detect neurological disorders. This tool preprocesses EEG signals (ICA, filtering, artifact rejection), extracts brainwave bands (Delta to Gamma), and applies detection heuristics for disorders such as:

- **Alzheimer’s** (low alpha power)
- **Parkinson’s Disease** (abnormal beta-gamma coherence)
- **Epilepsy** (seizure-like spikes)
- **Insomnia** (low delta power)

> Built with [MNE-Python](https://mne.tools/stable/index.html), `scipy`, and `matplotlib`.

---

## 📊 Features

- ✅ ICA-based artifact removal (EOG, ECG)
- ✅ Bandpass filtering into Delta, Theta, Alpha, Beta, Gamma bands
- ✅ Spike detection using `find_peaks` for seizure analysis
- ✅ Welch PSD for power analysis
- ✅ Coherence computation for Parkinson’s markers
- ✅ Clean visualizations of EEG bands and spectral power
- ✅ GUI-based file selection (Tkinter)

---

## 📂 Dataset

This tool was validated and tested using the publicly available EEG dataset:

> **OpenNeuro Dataset:** [ds004504 v1.0.8](https://openneuro.org/datasets/ds004504/versions/1.0.8)  
> "EEG Dataset for Studying Brain Rhythms Across Cognitive Tasks"  
> Citation:
> > Pasquale Bifulco et al., 2023. EEG Dataset for Studying Brain Rhythms Across Cognitive Tasks. OpenNeuro. [https://doi.org/10.18112/openneuro.ds004504.v1.0.8](https://doi.org/10.18112/openneuro.ds004504.v1.0.8)

---

## 🚀 Installation

```bash
git clone https://github.com/yourusername/eeg-disorder-detector.git
cd eeg-disorder-detector
pip install -r requirements.txt
