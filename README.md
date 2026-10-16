# KGEN — Genetic Algorithms for K-Anonymity

KGEN is a Java-based implementation of a **metaheuristic approach to k-anonymity**, designed to find a practical trade-off between privacy protection and data utility in structured datasets.

The project explores the use of **Genetic Algorithms (GAs)** to search for k-anonymous dataset transformations that preserve useful information while reducing re-identification risks.

KGEN was developed as part of the research presented in *Real-world K-Anonymity applications: The KGen approach and its evaluation in fraudulent transactions*, published in *Information Systems* in 2023.

---

## 🚀 Features

- **K-Anonymity:** Apply privacy-preserving transformations to structured datasets.
- **Genetic Algorithms:** Use metaheuristic search to explore candidate solutions to the de-identification problem.
- **Privacy–Utility Trade-off:** Seek k-anonymous solutions while preserving the information required for downstream data analysis.
- **Scalability:** Address de-identification scenarios involving datasets with many attributes and records.
- **Real-world Evaluation:** Support research into the practical application of k-anonymity to fraudulent transaction data.
- **Java Implementation:** Provide an implementation of the KGEN approach for experimentation and further development.

---

## 🧠 Approach

Traditional k-anonymization methods can become computationally expensive as the number of dataset attributes increases. This can limit their applicability to real-world, high-dimensional datasets.

KGEN addresses this challenge through a **Genetic Algorithm**, a population-based metaheuristic that explores candidate solutions to an optimization problem.

The approach searches for dataset transformations that satisfy k-anonymity constraints while retaining as much analytical utility as possible.

The main objectives are:

- **Privacy:** Ensure that records satisfy the required k-anonymity property with respect to the selected quasi-identifiers.
- **Utility:** Preserve information needed for subsequent analysis.
- **Efficiency:** Find suitable solutions within a practical computational budget.

Rather than relying exclusively on exhaustive search for a globally optimal solution, the metaheuristic approach aims to find high-quality, approximately optimal solutions within a reasonable time.

---

## 📊 Research and Evaluation

KGEN was evaluated in the context of real-world fraudulent transaction data.

The published study reports experiments involving datasets with different dimensionalities, including:

- A dataset with **47 attributes and more than 1,500 records**, based on data provided by the Dutch Tax Authority.
- A dataset with **97 attributes and more than 3,942 records**.

These experiments investigate the applicability of the proposed approach to datasets with a substantial number of attributes, focusing on the practical balance between anonymization, data utility, and computational efficiency.

For the complete methodology, experimental setup, and results, please refer to the original publication.

---

## 🛠️ Technology Stack

- **Java 8** — Core implementation.
- **Apache Maven** — Dependency management and build configuration.
- **Apache POI** — Spreadsheet processing.
- **Jackson** — JSON processing.
- **MySQL Connector/J** — MySQL connectivity.
- **Apache Commons DBCP** — Database connection pooling.

---

## 📋 Requirements

- Java Development Kit (JDK) 8 or a compatible environment.
- Apache Maven.
- Any external datasets or database resources required by the selected experiment.

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/jessicadp92/KGEN.git
cd KGEN
```

Verify the Java and Maven installations:

```bash
java -version
mvn -version
```

Compile the project and resolve its dependencies:

```bash
mvn clean compile
```

Build the project:

```bash
mvn package
```

The resulting build artifacts are generated in the `target/` directory.

The exact execution procedure depends on the selected entry point and the dataset or database configuration required by the experiment.

---

## 📚 Publication

**Real-world K-Anonymity applications: The KGen approach and its evaluation in fraudulent transactions**

Jessica De Pascale, Giuseppe Cascavilla, Damian A. Tamburri, and Willem-Jan Van Den Heuvel.

*Information Systems*, Volume 115, Article 102193, May 2023.

- **DOI:** [10.1016/j.is.2023.102193](https://doi.org/10.1016/j.is.2023.102193)
- **Publisher:** [ScienceDirect](https://www.sciencedirect.com/science/article/pii/S0306437923000297)
- **Open-access preprint:** [arXiv:2204.01533](https://arxiv.org/abs/2204.01533)

### Citation

```bibtex
@article{de2023real,
  title={Real-world K-Anonymity applications: The KGen approach and its evaluation in fraudulent transactions},
  author={De Pascale, Jessica and Cascavilla, Giuseppe and Tamburri, Damian A and Van Den Heuvel, Willem-Jan},
  journal={Information Systems},
  volume={115},
  pages={102193},
  year={2023},
  publisher={Elsevier}
}
```

---

## 🔗 Related Projects

- **[KGen-React](https://github.com/jessicadp92/KGen-React)** — Web frontend for dataset upload, attribute configuration, anonymization requests, and result export.
- **[kgen-api](https://github.com/jessicadp92/kgen-api)** — Python REST API implementing the OLA algorithm for k-anonymity.

These repositories explore complementary implementations and interfaces for dataset anonymization. The Python API uses OLA, whereas the original KGEN research described in the publication focuses on Genetic Algorithms.

---

## 👩‍💻 Author

**Jessica De Pascale**

[GitHub Profile](https://github.com/jessicadp92)
