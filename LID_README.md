# LID for memorization

We have included some LID functionalities to this repo.

Please run the following scripts:

```bash
# get the token attributions for a set of memorized prompts
python store_attributions.py attribution_method=<score_norm|cfg_norm|flipd>
```

You also have fine-grained control over the configuration with [hydra](https://hydra.cc/), please check `configs/` for more details.
