# Dynamic AOT Resnet-18 Example

This example AOT-compiles a Resnet-18 module for performing inference on a dynamic number of input images.

Using the image dataset [cats_and_dogs](https://huggingface.co/datasets/cats_vs_dogs), we compare the results of applying the compiled module to the results of applying the standard forward pass in python.

To run this example (with Python3.11), you should clone the repository to your local device and install the requirements in a virtual environment.

```bash
git clone https://github.com/nod-ai/SHARK-Turbine.git
cd SHARK-Turbine/examples/resnet-18
python -m venv rn18_venv
source ./rn18_venv/bin/activate
pip install -r ../../requirements.txt
pip install -r requirements.txt
```

Once the requirements are installed, you should be able to run the example.

```bash
python resnet-18.py
```

The input images are pulled from the dataset at a randomized start index, so running the program multiple times will yield different results. 