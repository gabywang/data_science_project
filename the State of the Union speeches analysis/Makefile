## Create a notebooks variable made from all ipynb files:
notebooks=$(wildcard *.ipynb)

## Reproduce Notebook with environment packages provided.
.PHONY: env
env:
	conda env create -f environment.yml

## Run all the notebooks.
.PHONY: all
all: $(notebooks)
	jupyter nbconvert --ExecutePreprocessor.timeout=600 --to notebook --execute $^