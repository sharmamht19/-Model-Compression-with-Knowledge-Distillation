
# Two-stage Multi-teacher Knowledge Distillation (TMKD) for Web Question Answering System

This repository contains the implementation and experimentation of the Two-stage Multi-teacher Knowledge Distillation (TMKD) method for enhancing the efficiency and performance of web-based Question Answering (QA) systems. The TMKD method compresses large, complex models like BERT into smaller, more efficient student models, ensuring minimal information loss and significantly improving inference speed.

## Overview

The TMKD method employs a two-stage process where multiple teacher models guide the distillation of knowledge into the student model. This approach ensures comprehensive learning and robust performance, making it ideal for practical web applications requiring real-time responses.

### Key Features

- **Two-stage Knowledge Distillation**: Involves an initial stage with multiple teachers followed by fine-tuning to ensure high-quality knowledge transfer.
- **Multi-teacher Approach**: Utilizes multiple teacher models to capture a wider range of knowledge, resulting in a more accurate and reliable student model.
- **Enhanced Efficiency**: The student model is significantly smaller and faster, making it suitable for deployment in resource-constrained environments.
- **High Performance**: Achieves results comparable to the original teacher models, outperforming baseline models in various metrics.

## Project Structure

```
Project
│
├── Code
│   ├── Many_to_One_RTE_to_QNLI.ipynb
│   ├── MNLI_Experiments.ipynb
│   ├── QNLI_Experiments.ipynb
│   ├── RTE_Experiments.ipynb
│   └── SNLI_Experiments.ipynb
│
├── Research Papers
│   ├── Paper.pdf
├── LICENSE
├── PPT.pdf
├── Report.pdf
└── README.md
```

### .ipynb Files

1. **MNLI_Experiments.ipynb**: Contains initial experimentation on the student model with one-to-one (1-o-1) and many-to-many (m-o-m) experimentation on the MNLI dataset.
2. **SNLI_Experiments.ipynb**: Details 1-o-1 and m-o-m experimentation on the SNLI dataset.
3. **QNLI_Experiments.ipynb**: Documents 1-o-1 and m-o-m experimentation on the QNLI dataset.
4. **RTE_Experiments.ipynb**: Includes 1-o-1 and m-o-m experimentation on the RTE dataset.
5. **Many_to_One_RTE_to_QNLI.ipynb**: Implements many-to-one (m-o-1) distillation on the RTE dataset, followed by fine-tuning on the QNLI dataset.

### Checkpoints

Create a folder named `checkpoints` and organize subfolders to store various model checkpoints as referenced in the code.

- **Stage 1 student model trained on RTE dataset**: [Download here](https://drive.google.com/file/d/1-VKA25BDx-d14U8mpHQRtunwjea1CaQ2/view?usp=sharing)
- **Stage 2 finetuned student model on QNLI dataset**: [Download here](https://drive.google.com/file/d/107W-lc7bavkw2ARbhuZyqpk00MkQJiDj/view?usp=sharing)

## Getting Started

### Prerequisites

- Python 3.7 or later
- PyTorch
- Transformers (Hugging Face)
- Other dependencies listed in `requirements.txt`

### Installation

1. Clone this repository:

   ```bash
   git clone git@github.com:sharmamht19/Model-Compression-with-Knowledge-Distillation.git
   cd Model-Compression-with-Knowledge-Distillation
   ```

2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

### Usage

1. Prepare your dataset and pre-trained models as specified.
2. Use the provided notebooks (`.ipynb` files) to replicate the experiments and train your student model using the TMKD method.
3. Evaluate the performance of the student model using the provided evaluation scripts.

### Example Workflow

1. **Experimentation**: Use `MNLI_Experiments.ipynb`, `SNLI_Experiments.ipynb`, `QNLI_Experiments.ipynb`, and `RTE_Experiments.ipynb` for one-to-one and many-to-many knowledge distillation experiments.
2. **Many-to-One Distillation and Fine-Tuning**: Follow `Many_to_One_RTE_to_QNLI.ipynb` for implementing many-to-one distillation on the RTE dataset and fine-tuning on the QNLI dataset.
3. **Checkpoint Management**: Store model checkpoints in the `checkpoints` directory as specified in the notebooks.

## Contribution

We welcome contributions to enhance the functionality and performance of TMKD. Feel free to open issues and submit pull requests.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgements

We would like to thank the developers of the BERT model and the Hugging Face Transformers library for their invaluable contributions to the field of Natural Language Processing.

---
