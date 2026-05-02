# OpenBIM.work

> **The definitive Job Analyzer for the OpenBIM and Construction Technology sector.**

![OpenBIM.work](https://img.shields.io/badge/Status-Under%20Development-00bcd4.svg)
![MkDocs](https://img.shields.io/badge/Powered%20by-MkDocs%20Material-526CFE.svg)

**OpenBIM.work** is a specialized platform designed to analyze, validate, and standardize job descriptions and professional profiles within the architecture, engineering, and construction (AEC) industries, with a strong focus on OpenBIM methodologies.

Our primary tool—the **OpenBIM Job Analyzer**—allows users to paste job links or text descriptions to receive comprehensive insights into the required profiles, ensuring alignment with industry standards and reducing the gap between employer expectations and professional qualifications.

## 🚀 Features

- **Job Description Parsing:** Automatically extract key requirements, software proficiency, and BIM maturity levels from any job posting.
- **Multilingual Support:** The platform is available in English, Portuguese, and Spanish to serve the global AEC community.
- **Database Integration:** Opt-in mechanism allowing users to anonymously contribute job data to help build a centralized, open database of global BIM employment trends.
- **Modern, Accessible UI:** Built on top of MkDocs Material, providing a lightning-fast, responsive, and dark-mode compatible experience.

## 🛠️ Local Development

This project is built using [MkDocs](https://www.mkdocs.org/) and the [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) theme.

### Prerequisites

Ensure you have Python 3.x installed. Then, install the required dependencies:

```bash
pip install -r requirements.txt
```

### Running the Local Server

To preview the website locally with live-reload enabled:

```bash
mkdocs serve
```

The site will be accessible at `http://127.0.0.1:8000/`.

### Building for Production

To generate the static HTML files for deployment:

```bash
mkdocs build
```

This will output the compiled site into the `../site` directory, as configured in the `mkdocs.yml`.

## 🤝 Contributing

This project is currently under active development. Contributions, feature requests, and bug reports are welcome. Feel free to open an issue or submit a pull request.

## 📄 License

© 2026 OpenBIM.work. All rights reserved.