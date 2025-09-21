# Face Detection & Recognition 🧑‍💻

Este projeto demonstra um fluxo básico de **detecção de rostos** e **reconhecimento facial** usando:

* **MTCNN** para localizar faces em imagens.
* **VGGFace (ResNet50)** para gerar embeddings faciais.
* **SVM (Support Vector Machine)** para classificar os rostos.

---

## 🚀 Como funciona

1. **Detectar rostos** na imagem usando o MTCNN.
2. **Extrair embeddings** de cada rosto com a VGGFace (sem a camada de classificação).
3. **Treinar um classificador SVM** com embeddings de imagens de referência.
4. **Testar em novas imagens**, classificando o rosto detectado.

---

## 📦 Dependências

O ambiente pode ser configurado com:

```bash
pip install mtcnn keras-vggface keras-applications scikit-learn opencv-python matplotlib
```

---

## 📂 Estrutura esperada

Coloque imagens de referência para cada pessoa no dataset. Exemplo:

```
pessoa1.jpg
pessoa2.jpg
teste.jpg
```

---

## ▶️ Executar

* Adicione imagens de treino (`pessoa1.jpg`, `pessoa2.jpg` etc.).
* Rode o notebook/script.
* O modelo treina o **SVM** e reconhece rostos em `teste.jpg`.

---

## 📌 Observações

* Este é um **exemplo didático**. Para uso em produção, recomenda-se:

  * Ampliar o dataset por pessoa.
  * Normalizar e balancear os dados.
  * Explorar arquiteturas mais modernas (ex.: [DeepFace](https://github.com/serengil/deepface)).
