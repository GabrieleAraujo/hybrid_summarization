[![GitHub issues](https://img.shields.io/github/issues/GabrieleAraujo/hybrid_summarization)](https://github.com/GabrieleAraujo/hybrid_summarization/issues)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-blue.svg?style=flat-square)](https://github.com/GabrieleAraujo/hybrid_summarization/pulls)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![HitCount](https://views.whatilearened.today/views/github/GabrieleAraujo/hybrid_summarization.svg)](https://github.com/GabrieleAraujo/hybrid_summarization) 
[![website coderjojo.github.io](https://img.shields.io/website-up-down-yellow-red/http/coderjojo.github.io/creative-profile-readme.svg)](http://laca-ufopa.com.br/)



<h1 align="center">
  <img align="center" alt="SBSI" height="180" width="180" src="https://ppcomp-ifes.github.io/sbsi/src/assets/logo-sbsi-2026-removebg-preview.png"> <br>
  <br>
   Hybrid Summarization for Brazilian Judicial Decisions
  <br>
</h1>

<h4 align="center">
This repository contains the datasets and experimental results of the article submitted to a conference in the <br> XXII Brazilian Symposium on Information Systems (<a href="https://sbsi.sbc.org.br/2026//">SBSI 2026</a>)
</h4>


<p align="center">
  <a href="#abstract">Abstract</a> •
  <a href="#dataset">Dataset</a> •
  <a href="#results">Results</a> •
  <a href="#authors">Authors</a> •
  <a href="#citation">Citation</a>
</p>

## Abstract
Judicial decisions in Brazil are characterized by long documents, technical language, and dispersed argumentative structures, posing challenges for information systems that support legal analysis and decision-making. This study proposes and evaluates a **hybrid summarization pipeline** for Brazilian Supreme Court (STF) decisions, combining extractive and abstractive approaches to process long legal documents efficiently while preserving technical accuracy. Five methods were evaluated: (i) TF-IDF extractive baseline; (ii) BumbaBERT extractive with chunk-based processing; (iii) a purely abstractive approach using a large language model (Gemini-2.5); and (iv–v) two hybrid variants combining extractive selection and abstractive refinement. Experiments were conducted on the **RulingBR** corpus using ROUGE, BERTScore, and METEOR metrics. Results show that hybrid strategies balance summary quality and computational feasibility, while the abstractive approach achieves the highest ROUGE scores. The study contributes to scalable, transparent, and interoperable decision-support systems in the public sector.

---

## Dataset

- **RulingBR v1.2** – Brazilian Legal Summarization Corpus  
  Source: https://github.com/feijoa/RulingBR  

The dataset contains **10,574 decisions from the Brazilian Supreme Court (STF)**, structured into sections such as *relatório*, *voto*, *acórdão*, and *ementa*, enabling controlled evaluation of summarization methods.

---

## Results

### Performance of summarization methods on RulingBR

| Method                | ROUGE-1 | ROUGE-2 | ROUGE-L | BERTScore | METEOR |
|-----------------------|---------|---------|---------|-----------|--------|
| TF-IDF (baseline)     | 0.3582  | 0.1480  | 0.2023  | 0.1377    | 0.2387 |
| BumbaBERT             | 0.3579  | 0.1677  | 0.2070  | **0.1621**| **0.2730** |
| Gemini-2.5            | **0.4524** | **0.2315** | **0.2964** | 0.1418 | 0.2726 |
| TF-IDF + Gemini       | 0.4080  | 0.1871  | 0.2609  | 0.1236    | 0.2329 |
| BumbaBERT + Gemini    | 0.4053  | 0.1841  | 0.2584  | 0.1257    | 0.2267 |

Hybrid methods provide competitive performance while reducing computational cost and token usage, making them suitable for large-scale judicial information systems.

---

## License
This project is licensed under the MIT License.

---

## Authors

<table>
  <tr>
    <td align="center">
      <a href="https://orcid.org/0000-0003-1143-507X">
        <img src="https://avatars.githubusercontent.com/u/69174689?v=4&v=beta&t=w9ElVgj2tNOaCe4zkQ04e8WxDn42IXRvOZ-ZFYm0H5g" width="100px;" alt="Foto da Gabriele"/><br>
        <sub>
          <b>Gabriele S. Araújo</b><br>
          UEMA – São Luís, Brazil
        </sub>
      </a>
    </td>
    <td align="center">
      <a href="https://orcid.org/0000-0002-8894-5353">
        <img src="https://lablaps.vercel.app/static/media/prof.ewaldo.19f17a386c1b84815708.png" width="100px;" alt="Foto do Ewaldo"/><br>
        <sub>
          <b>Ewaldo Eder Carvalho Santana</b><br>
          UFMA – São Luís, Brazil
        </sub>
      </a>
    </td>
    <td align="center">
      <a href="https://orcid.org/0000-0002-6282-0368">
        <img src="https://avatars.githubusercontent.com/u/42838538?s=400&v=4" width="100px;" alt="Foto do Fábio"/><br>
        <sub>
          <b>Fábio M. F. Lobato</b><br>
          UFOPA – Santarém, Brazil
        </sub>
      </a>
    </td>
  </tr>
</table>

## Citation

```
@inproceedings{araujo2026hybrid,
  title={Hybrid Summarization for Brazilian Judicial Decisions},
  author={Ara{\'u}jo, Gabriele S and Santana, Ewaldo EC and Lobato, F{\'a}bio MF},
  booktitle={Simp{\'o}sio Brasileiro de Sistemas de Informa{\c{c}}{\~a}o (SBSI)},
  pages={910--929},
  year={2026},
  organization={SBC},
  doi={https://doi.org/10.5753/sbsi.2026.248671}
}
```
