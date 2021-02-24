# Image Grabbing and Processing Pipeline

**Tags**: image_processing, nvidia_deepstream

**Committer**: German Suvorov, Data Monsters

![Scheme](https://github.com/ml-patterns/ml-patterns/blob/main/patterns/images/2.jpg)

### Challenge

Transfer and preprocess images generated at the edge device for use with deep learning models located on a GPU server.

### Solution

The data is transferred through GigE protocol from the cameras using separate containerized image grabber applications for each camera. 
Image grabbers operate at the edge computing nodes. They capture frames from the cameras, encode the frames into JPEG bitstream and transfer it to **DeepStream** Application using **ZeroMQ**, a high speed low profile message queue.
DeepStream pipeline is build up with a set of standard DeepStream plugins:
* The first one, **Nvjpegdec** decodes JPEG bitstream into RGBA bitmaps using CUDA toolkit with hardware acceleration.
* The second **Nvstreammux** plugin packs incoming bitmaps from multiple sources into a batch.
It waits for a given timeout before forming the batch.
If the complete batch is formed before the timeout is reached, the batch is pushed down the stream.
If the timeout is reached before the complete batch can be formed, it just packs the available input buffers and pushes them forward.
* The third one, **Nvinfer** performs batched inferencing using the segmentation model. This is where our defect detection magic happens. Nvinfer uses TensorRT inference to run optimized deep learning models.
* The fourth, **Nvmsgconv** generates the payload metadata based on the inference results.
* Finally, the fifth plugin, **Nvmsgbroker** sends payload messages to the server for further integration into BI applications and factory dashboards.
