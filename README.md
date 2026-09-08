# Digit Recognizer PWA

A phone-friendly Progressive Web App that recognizes handwritten digits 0–9.

## Files

- index.html — UI, drawing, camera, TensorFlow.js inference
- manifest.json — makes the site installable as an app
- sw.js — caches the app shell
- icons/ — app icons

## Important

Camera access requires HTTPS (or localhost). GitHub Pages is a simple free way to host it.

The neural network is a public TensorFlow.js MNIST CNN:
https://huggingface.co/gaurangdave/mnist_cnn

The model already contains an input rescaling layer, so index.html deliberately feeds raw 0–255 grayscale values.

## GitHub Pages

1. Create a GitHub repository.
2. Upload all files and folders from this project.
3. Open Settings → Pages.
4. Deploy the main branch as the source.
5. Open the generated HTTPS URL on Android Chrome.
6. Use Chrome's "Add to Home screen" / install option.

After the first successful load, the PWA shell is cached. The TensorFlow.js library and neural-network model may still need network access unless you separately self-host/cache those assets.
