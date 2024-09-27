# LID for memorization

We have included some LID functionalities to this repo.

## Prompt attribution

Please run the following scripts:

```bash
# get the token attributions for a set of memorized prompts
python store_attributions.py attribution_method=<score_norm|cfg_norm|flipd>
```

This will store a json file in `outputs/attributions` that contains all the token attributions obtained via any of the metrics above!

### Perturbation

Prompt perturbation is done through our `perturb_gpt.py` script. Before that, you have to store your `OPENAI_API_KEY` in a `.env` file in the root directory of this repo, meaning, you should have a file `.env` with the following content:

```bash
OPENAI_API_KEY='<your-key>'
```

You can then run the following script:

```bash
python perturb_gpt.py attribution_method=<score_norm|cfg_norm|flipd>
```

Note that you would have to store the attributions in the appropriate json files in `outputs/attributions` before running this script (there should be some default ones already there).

## Prompt Optimization

You also have fine-grained control over the configuration with [hydra](https://hydra.cc/), please check `configs/` for more details.
