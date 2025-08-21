# Avaliação da Robustez de Modelos Visão-Linguagem Adversarialmente Treinados

Este repositório contém os experimentos e resultados do meu Trabalho de Conclusão de Curso (TCC), no qual investiguei **como o treinamento adversarial afeta simultaneamente a robustez e a interpretabilidade de modelos Visão-Linguagem (VLMs)**.

## ✨ Resumo do Trabalho

Modelos como o **CLIP** atingem resultados notáveis em zero-shot learning, mas permanecem vulneráveis a ataques adversariais quase imperceptíveis.  
Neste estudo, comparei o **CLIP ViT-B/32** com uma versão adversarialmente treinada (**Fare-CLIP**) usando 500 imagens do dataset **RIVAL-10**.

Principais achados:

- **Mapas mais focados:** +0,14 em *Sparsity*  
- **Menor dispersão:** −0,53 bits em *Entropia*  
- **Melhor localização:** +7,8 p.p. no *Pointing-Game*  
- **Maior estabilidade:** −0,65 no *Gradient L2-Shift*  

👉 Conclusão: O pré-treino adversarial melhora robustez **e** interpretabilidade sem necessidade de fine-tuning supervisionado adicional, corroborando o viés de forma (*shape bias*).

## 📂 Estrutura do Repositório

- `Adversarially_Trained_VLM.ipynb` → Notebook principal com pipeline de experimentos:
  - Geração de mapas de saliência
  - Avaliação quantitativa (sparsity, entropia, pointing-game, L2-shift)
  - Visualizações qualitativas
- `TCC.pdf` → Trabalho escrito com discussão completa dos resultados
- `requirements.txt` → Dependências para execução do notebook

## 🚀 Como Reproduzir

Clone o repositório:

```bash
git clone https://github.com/<SEU-USUARIO>/adversarial-vlm.git
cd adversarial-vlm
```

Crie o ambiente e instale dependências:
```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

Execute o notebook no Jupyter ou Google Colab:
```bash
jupyter notebook Adversarially_Trained_VLM.ipynb
```

## 📖 Referências

Zhang & Zhu (2019). Interpreting Adversarially Trained Convolutional Neural Networks

Radford et al. (2021). Learning Transferable Visual Models from Natural Language Supervision

Choi et al. (2024). Robust CLIP: Unsupervised Adversarial Fine-tuning of Vision Embeddings


## 👤 Autor

Ramon Ferreira Alencar Corrêa D’barssoles
