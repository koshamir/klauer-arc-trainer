# Klauer ARC Trainer

Adult Klauer/Phye inductive reasoning trainer using ARC-AGI and Re-ARC-style tasks.

This project is not a generic ARC puzzle viewer.

The goal is to build a full Klauer/Phye inductive reasoning training system based on six operations:

1. Generalization
2. Discrimination
3. Cross-classification
4. Recognizing relationships
5. Differentiating relationships
6. System construction

Core task source:

- ARC-AGI JSON tasks from ARC-AGI-1.0.2/data/training
- ARC-AGI JSON tasks from ARC-AGI-1.0.2/data/evaluation
- Optional Re-ARC generated JSON packs later

Target:

- Single-file HTML/CSS/JS app
- Works locally in browser
- No server required
- Adult adaptive difficulty
- ARC grid renderer
- Manual output-grid editor
- Klauer/Phye operation modes
- Error journal
- LocalStorage progress
