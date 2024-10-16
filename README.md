## Steps to the run the GAN model
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

## Modify lambda_wgan inside `args.py` between 0-10 to tune the model