# AI Radiology — Chest X-ray Screening System for Medical Organizations

**Solution by**: [Artificial Intelligence Institute of Innopolis University](https://innopolis.university/en/)

**Date**: March 2021

![Scheme](https://github.com/ml-patterns/ml-patterns/blob/main/library/images/AI_Radiology—Chest_X-ray_Screening_System_for_Medical_Organizations.jpg)

### Challenge

Chest X-ray images differ from one vendor to another. The same machine can have different configurations, and thus produce different pixel intensity distributions, making it harder to produce a generalized model. Additionally, labels may vary between datasets (Cohen, J.P., Hashir, M., Brooks, R. & Bertrand, H.. [2020]. On the limits of cross-domain generalization in automated X-ray prediction. Proceedings of the Third Conference on Medical Imaging with Deep Learning, in PMLR 121:136–155). The number of medical organizations that currently or will potentially use the system is huge, and thus it should be able to work under a heavy load.

### Solution

Screening is based on a binary classification model, and visualization is based on GradCAM and saliency maps. Images are captured by X-ray machines and then transferred to the PACS of the medical organization. Then, the PACS sends anonymized images to a DICOM-adapter, which distributes data and initiates new pipelines (DAGs) for data processing. After pre-processing, data is submitted to the NVIDIA Triton inference server and then post-processed to produce valid DICOM files with visualization and a structured report. These new files are then submitted back to the PACS of a medical organization, where doctors can see the results in the tools they already use. Each medical organization can have its own set of post-processing functions to have the reports they want. The model highlights potential pathological regions in lungs.

### Technologies

PyTorch, NVIDIA Triton Inference Server, Apache Airflow, Kafka
