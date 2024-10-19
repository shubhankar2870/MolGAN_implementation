### Steps to the run the MolGAN model
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