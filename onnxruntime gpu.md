# onnxruntime cuda cudnn
 见[*onnxruntime cuda*](https://onnxruntime.ai/docs/execution-providers/CUDA-ExecutionProvider.html#cuda-11x)

 | ONNX Runtime | CUDA | cuDNN |
 |-------- | -----|-----|
 | 1.20.x | 11.8/12.6 | 8.x/9.x | 
 | 1.19.x | 11.8/12.4 | 8.x/9.x | 
 | 1.18.x | 11.8 | 8.x | 
 | 1.17/1.16/1.15 | 11.8 | 8.2.4 (Linux)/8.5.0.96 (Windows) | 
 | 1.14/1.13 | 11.6 | 8.2.4 (Linux)/8.5.0.96 (Windows) | 
 | 1.12/1.11 | 11.4 | 8.2.4 (Linux)/8.2.2.26 (Windows) | 
 | 1.10 | 11.4 | 8.2.4 (Linux)/8.2.2.26 (Windows) | 
 | 1.9 | 11.4 | 8.2.4 (Linux)/8.2.2.26 (Windows) | 

| ONNX Runtime version	| ONNX version | ONNX opset version	|	ONNX ML opset version	| ONNX IR version 	| CUDA 	| CUDNN |
|-------- | -----|-----|-----|-----|-----|-----|
|1.20 |1.16.1	|**21**	|4	|10 |
|1.19 |1.16.1	|**21**	|4	|10 |
|1.18 |1.16	|**21**	|4	|10 |
|1.17	|1.15	|20	|4	|9 |
|1.16	|1.14.1	|**19**	|3	|9 |
|1.15	|1.14	|**19**	|3	|8 |
|1.14	|1.13	|18	|3	|8 |
|1.13	|1.12	|**17**	|3	|8           |11.6/11.4	   | **8.2.4.15**
|1.12	|1.12	|**17**	|3|	8 
|1.11	|1.11	|16	|2	|8 
|1.10	|1.10	|15	|2	|8 
|1.9	|1.10	|15	|2	|8           |11.4	   |8.2.2.26

onnxruntime gpu windows 1.13.1
cuda 11.6 对应的 cudnn是 8.2，用8.4 或8.5的cudnn都不行！！！
onnxruntime gpu windows 1.19.2
cuda 12.6 对应的 cudnn是 9.7，用9.11不行！！！ 
# TensorRT 

TensorRT 8.0 GA Update 1==tensorrt-8.0.3.4 	cuda-11.3~11.1  cudnn8.2 
 
TensorRT 8.2 GA Update 4	==TensorRT-8.2.5.1 cuda-11.4~11.1  cudnn8.2 

TensorRT 8.4 GA Update 2==TensorRT-8.4.3.1  cuda-11.6~11.1  cudnn8.4 

TensorRT 8.5 GA Update 2==TensorRT-8.5.3.1  cuda-11.8~11.1  cudnn8.6 

# onnx

导出onnx时，batch_size=1，dynamic=False