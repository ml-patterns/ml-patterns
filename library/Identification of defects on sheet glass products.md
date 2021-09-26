# Identification of defects on sheet glass products

**Solution by**: [Forest Valley](https://fv.dev/)

**Date**: September 2021

![Scheme](https://github.com/ml-patterns/ml-patterns/blob/main/library/images/Identification_of_defects_on_sheet_glass_products.jpeg)

### Challenge

Identification of external and internal defects of glass blank sheets (scratches, abrasions, bubbles, chips, fingerprints, and traces of glue) at each stage of production.

### Solution

The technology is mounted directly on the production equipment in the factory. It consists of a line of cameras with a total resolution of 16 pixels per square mm of surface and a specialized illumination system (end illumination with a powerful local focused spotlight, indirect illumination, and translucent illumination from various angles). The cameras and server are connected via industrial Ethernet 10Gbps. The software complex consists of two main parts. First, a neural network unit of computer vision. Second, service software for storing an archive of digital samples, their labeling, and training modules.

### Technologies

- PyTorch
- Scikit-learn
- Spark
- Kafka
