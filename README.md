# MolGAN: Implicit Generative Model for Small Molecular Graphs

MolGAN is a deep generative model that generates molecular graphs using an implicit, likelihood-free generative adversarial network (GAN). It is designed to generate valid molecular structures efficiently without relying on expensive graph matching or ordering procedures. Additionally, MolGAN integrates a reinforcement learning (RL) objective to enhance the generation of molecules with desired chemical properties.

## Features
- Generates molecular graphs using GANs.
- Reinforcement learning objective to optimize chemical properties.
- Validity, novelty, and uniqueness in molecular generation.
- Utilizes a permutation-invariant discriminator and reward network based on graph convolutions.

## Model Architecture
1. **Generator**: Produces molecular graphs represented by adjacency tensors and annotation matrices.
2. **Discriminator**: Classifies graphs as real or fake.
3. **Reward Network**: Provides feedback based on chemical properties using an external software like RDKit.

## Dependencies
- Python 3.x
- TensorFlow or PyTorch
- RDKit for chemical property evaluation
- Adam optimizer for training

## Usage
1. Clone the repository and install dependencies.
2. Prepare a dataset of molecular graphs (e.g., QM9 dataset).
3. Run the training script:
    ```
    0. Create and activate a virtual environment
    ```

    ```
    1. pip install -r requirements.txt
    ```

    ```
    2. cd data
    ```

    ```
    3. bash download_dataset.sh
    ```

    ```
    4. python sparse_molecular_dataset.py
    ```

    ```
    5. cd ..
    ```

    ```
    6. python main_gan.py
    ```

## Molecule Generation Exhibition
These results are trained with the QM9 dataset. 
### Pure RL (WGAN-Lambda = 0.0)
<p align="center">
    <img width=15% height="auto" src="resources/rl_1.png" alt="rl_1" />
    <img width=15% height="auto" src="resources/rl_2.png" alt="rl_2" />
    <img width=15% height="auto" src="resources/rl_3.png" alt="rl_3" />
    <img width=15% height="auto" src="resources/rl_4.png" alt="rl_4" />
    <img width=15% height="auto" src="resources/rl_5.png" alt="rl_5" />
    <img width=15% height="auto" src="resources/rl_6.png" alt="rl_6" />
</p>

### Mixture of RL and GAN (WGAN-Lambda = 0.5)
<p align="center">
    <img width=15% height="auto" src="resources/wla_p5_1.png" alt="wla_p5_1" />
    <img width=15% height="auto" src="resources/wla_p5_2.png" alt="wla_p5_2" />
    <img width=15% height="auto" src="resources/wla_p5_3.png" alt="wla_p5_3" />
    <img width=15% height="auto" src="resources/wla_p5_4.png" alt="wla_p5_4" />
    <img width=15% height="auto" src="resources/wla_p5_5.png" alt="wla_p5_5" />
    <img width=15% height="auto" src="resources/wla_p5_6.png" alt="wla_p5_6" />
</p>

### Pure GAN (WGAN-Lambda = 1.0)
<p align="center">
    <img width=15% height="auto" src="resources/pure_gan_1.png" alt="pure_gan_1" />
    <img width=15% height="auto" src="resources/pure_gan_2.png" alt="pure_gan_2" />
    <img width=15% height="auto" src="resources/pure_gan_3.png" alt="pure_gan_3" />
    <img width=15% height="auto" src="resources/pure_gan_4.png" alt="pure_gan_4" />
    <img width=15% height="auto" src="resources/pure_gan_5.png" alt="pure_gan_5" />
    <img width=15% height="auto" src="resources/pure_gan_6.png" alt="pure_gan_6" />
</p>
