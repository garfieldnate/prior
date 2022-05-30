# Prior

 🐍 A Python package for distributing datasets from AI2's PRIOR team 

## Installation

Make sure you have [git-lfs](https://git-lfs.github.com/) installed, and then the `prior` package:

```bash
pip install prior
```

## Example Usage

To use a public Python dataset, simply run:

```python
import prior
dataset = prior.load_dataset(
    "test-dataset", entity="mattdeitke", revision="main"
)
```
Here, `revision` can be either a tag, branch, or commit hash.

## Private Datasets

If you want to use a private dataset, make sure you're either:
1. Already logged into GitHub from the command line, and able to pull a private repo.
2. Set the GITHUB_TOKEN environment variable to a GitHub authentication token with read access to private repositories (e.g., `export GITHUB_TOKEN=<token>`). You can generate a GitHub authentication token [here](https://github.com/settings/tokens).
3. Set the `gh_auth_token` global variable in the `prior` package with:
```python
import prior
prior.gh_auth_token = "<token>"
```
