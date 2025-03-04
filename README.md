# CSCE 421 Project

## Contributors

- Akilan Manivannan
- Alyan Tharani
- Ethan Tran

## Project Structure

We utilized Jupyter Notebooks to train our models. This was needed so that we could easily transfer our code between different environments (local, Google Colab, TAMU HPRC, etc).

The following tree shows how the project is structured:

```
¦   README.md
¦   tree
¦   
+---.ipynb_checkpoints
¦       README-checkpoint.md
¦       
+---data
¦       breastmnist.npz
¦       pneumoniamnist.npz
¦       
+---experiments
    ¦   Ensemble.ipynb
    ¦   
    +---Other Models
    ¦   ¦   roc_breast.png
    ¦   ¦   roc_pneumonia.jpg
    ¦   ¦   SKLearn Models.ipynb
    ¦   ¦   sklearn_models.joblib
    ¦   ¦   
    ¦           
    +---Resnet
            Resnet.ipynb
            resnet_breast.pt
            resnet_pneumonia.pt
            
```

In the `Other Models` folder the `sklearn_models.ipynb` notebook shows how to train and test the non-neural network models that we trained. The `sklearn_models.joblib` file contains trained versions of these models. These can be loaded with the `joblib.load` function. `joblib` comes with `sklearn` and should already be installed. The Jupyter notebook has instructions on how to load this to be used immediatly.

In the `Resnet` folder, the `Resnet.ipynb` notebook shows how to train and test the final, tuned version of Resnet that we selected for this project. The saved models `resnet_breast.pt` and `resnet_pneumonia.pt` can be loaded with Torch's `torch.load` function.

Our final notebook is contained in `Ensemble.ipynb`. This notebook loads all previously trained notebooks (using their saved checkpoints) and combines them into a single model and tests their accuracy. This notebook can be referenced for a minimimal guide on how to load and use each of our other models.
