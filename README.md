1/Interpreter interpreter = new Interpreter(loadModelFile(), new Interpreter.Options());

Bitmap inputBitmap = preprocessInputImage(inputImage);

 inference
float[][] output = new float[1][NUM_CLASSES];
interpreter.run(inputBitmap, output);

String result = postprocessOutput(output);
