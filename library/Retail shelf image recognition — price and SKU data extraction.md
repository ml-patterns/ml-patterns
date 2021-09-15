# Retail shelf image recognition — price and SKU data extraction

**Solution by**: [Napoleon IT](https://www.napoleonit.com/about)

**Date**: September 2021

![Scheme](https://github.com/ml-patterns/ml-patterns/blob/main/library/images/retail-shelf-image-recognition-price-and-sku-data-extraction.jpeg)

### Challenge

Large retailers and specialized companies need to collect competitors’ prices to be able to offer the best price for their customers. In order to speed up and automate the price collection process and improve the quality of the data, one proposal is to take a photo of the grocery store shelf with the necessary items. Then, with the use of computer vision technology, the system recognizes the items and identifies their names and prices.
The difficulty of this process is related to:
1. A large variety of input data;
2. Complex customer business processes, e.g., the presence of very similar items from different manufacturers or adding/deleting new SKUs from the monitoring scope;
3. Items that have a similar appearance, but might be different;
4. Different packing volumes within the same item;
5. Different names of the same item in different stores.

### Solution

After a photo has been taken, a mobile app sends the image to S3 storage. Then, using the image address on S3, the mobile app sends a recognition request to the server. The server then creates a task for identification in the database and queues the image address. There are “identification workers” at the other side of the queue which download the image from the data storage and identify it.
The results are stored in a database, from which the mobile app retrieves the results. After that, the employee checks the identified positions. In case of error, the employee can enter the data manually. The corrected data can be used later to further train the models.
The identification pipeline works as follows:
Images are identified by a detector which finds the location and price tags of the items. The item locations are sent for product classification, and the price tags are sent for price reading. Identified items and price tags are further compared with each other using their spatial positioning in the image.
The found product-price pairs are further used in packing volume classification. Here, the theory is that a lower-capacity item costs less than a higher-capacity one. Finally, the identified product and its price are returned to the client.

### Technologies

- Programming languages: Python, GO
- Deep learning frameworks: Pytorch, Tensorflow
- Database: Postgres DB
- Queue: RabbitMQ
