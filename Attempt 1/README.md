running code:

python3 classify_picamera.py \
  --model /tmp/mobilenet_v1_1.0_224_quant.tflite \
  --labels /tmp/labels_mobilenet_quant_v1_224.txt
  
  
You'll need to issue the source tflite1-env/bin/activate command from inside the /home/pi/tflite1 directory to reactivate the environment every time you open a new terminal window. You can tell when the environment is active by checking if (tflite1-env) appears before the path in your command prompt, as shown in the screenshot below.

     camera.annotate_text = '%s %.2f\n%.1fms' % (labels[label_id], prob,
                                                    elapsed_ms)
- Possibly create another venv
- Incorporate the tflite model into rest of code 
- Install tflite on the actual raspberry pi: https://www.tensorflow.org/lite/guide/python#install_tensorflow_lite_for_python 

Running a model
Running a TensorFlow Lite model involves a few simple steps:
1. Load the model into memory.
2. Build an Interpreter based on an existing model.
3. Set input tensor values. (Optionally resize input tensors if the predefined sizes are not desired.)
4. Invoke inference.
5. Read output tensor values.

https://www.tensorflow.org/lite/guide/inference#load_and_run_a_model_in_python  - loading and running a tf model


