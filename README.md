# 🧠 EEG Disorder Detector

A Python-based tool to analyze EEG signals and detect neurological disorders such as:

- **Alzheimer’s Disease**
- **Parkinson’s Disease**
- **Epilepsy**
- **Insomnia**

This tool uses MNE for signal processing, ICA artifact removal, and brainwave filtering (Delta to Gamma), along with power/coherence/spike analysis to assess neurological health.

---

## 📸 Sample Visualizations

### 1. Brain Wave Visualization (Delta to Gamma)
Shows filtered brainwave bands and annotated spike detection for seizure signs.

![Brainwave Plot](docs/brainwave_plot.png)

---

### 2. Spectral Power (Welch’s Method)
Power Spectral Density analysis across brainwave bands to assess power abnormalities.

![Spectral Power](docs/spectral_power_plot.png)

---

### 3. Spike Annotations (Epilepsy Detection)
Spikes in Beta band (red arrows) used to flag potential seizure activity.

![Spike Detection](docs/spike_annotation.png)

---

## 🔗 Dataset Source

Used and validated on [OpenNeuro ds004504](https://openneuro.org/datasets/ds004504/versions/1.0.8)  
> *Pasquale Bifulco et al. (2023)* — EEG Dataset for Studying Brain Rhythms Across Cognitive Tasks

📄 DOI: [10.18112/openneuro.ds004504.v1.0.8](https://doi.org/10.18112/openneuro.ds004504.v1.0.8)

---

## 🧪 Detection Criteria

| Disorder      | Criteria |
|---------------|----------|
| Alzheimer’s   | Alpha Power < `0.2` |
| Parkinson’s   | Beta Power > Gamma Power × 1.3 + Coherence > `0.5` |
| Epilepsy      | Spikes > 20 in Beta Band |
| Insomnia      | Delta Power < `0.3` |

---

## ▶️ How to Run

```bash
pip install -r requirements.txt
python gui_launcher.py
