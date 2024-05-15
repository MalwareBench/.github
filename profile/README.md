# MalwareBench: Benchmark Dataset for Software Supply Chain Security

The prevalence of third-party components in modern software development, along with rapid digitization, has significantly amplified the risk of software supply chain security attacks. Popular registries like npm and PyPI serve as highly targeted channels for malware distribution due to their extensive growth and reliance on third-party components. Industry and academia are working towards building tools to detect malware in the software supply chain. However, a lack of benchmark datasets containing both malware and neutral packages hampers the evaluation of the performance of these malware detection tools. The goal of our study is to aid researchers and tool developers in evaluating and improving malware detection tools by contributing a benchmark dataset built by systematically collecting malicious and neutral packages from the npm and PyPI ecosystems. 

## Overview

MalwareBench is a labeled dataset aimed at aiding researchers and tool developers in evaluating and improving malware detection tools. It comprises 20,792 packages (of which 6,659 are malicious) collected systematically from the npm and PyPI ecosystems. The dataset is constructed by amalgamating pre-existing malware datasets with Socket's internal benchmark data and incorporating both popular and newly released packages.

## Data Description and File Structure

MalwareBench includes malicious and neutral packages, each annotated with package names, versions, release types, and ground truth labels. Ground truth labels categorize packages into two groups: 
- **Malware**: Packages designed to carry out harmful actions, posing threats to system confidentiality, integrity, or availability.
- **Neutral**: Packages have no known malware.

Additional metadata such as file paths, file sizes, total number of files, package sizes, file extensions, and package groups are provided for each package.

## Overview of the CSV dataset

| Field Name      | Description                                             | Data Type |
|-----------------|---------------------------------------------------------|-----------|
| id              | Unique Identified of each package                       | Integer   |
| ecosystem       | Name of the ecosystem                                   | String    |
| scoped          | npm Scoped name ($@$)                                  | String    |
| name            | Packages name                                           | String    |
| version         | Package version                                         | String    |
| releases_type   | Package releases type                                   | String    |
| total_files     | Total number of files in a package                      | Integer   |
| package_size    | Total package size in KB                                 | Integer   |
| label           | Ground truth label of packages                          | String    |
| file_path       | Path of a specific file within the package              | String    |
| file_extension  | File's extension of a specific file within the package  | String    |
| file_size       | Size of the file within the package in KB               | Integer   |



## Access Information

Due to the presence of real-world malware, certain packages may contain sensitive information. Access to the dataset is available upon reasonable request, considering ethical considerations for usage. To request access, please fill out the [Google form](https://forms.gle/A5h73BrxS1qsxfaU9). For further questions or assistance, please reach out to the authors.

## Sources

- [Backstabber’s Knife Collection: A Review of Open Source Software Supply Chain Attacks](https://link.springer.com/chapter/10.1007/978-3-030-52683-2_2)
- [Towards Measuring Supply Chain Attacks on Package Managers for Interpreted Languages](https://arxiv.org/pdf/2002.01139.pdf)
- [An Empirical Study of Malicious Code in PyPI Ecosystem](https://arxiv.org/abs/2309.11021)
- [Open-Source Dataset of Malicious Software Packages](https://github.com/datadog/malicious-software-packages-dataset)
- [Socket Internal Benchmark Dataset](https://socket.dev/)

