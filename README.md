# FEVER Shared Task 2018

The First Workshop on Fact Extraction and Verification

## Reproduce retrieval result

`python3 pipeline.py --config configs/submission_config.json --model [arbitrary name]`

Output files will be generated under `results/[arbitrary name]`.
`submission.json` and `test_submission.json` correspond to the output for development and test set for each.

## Natural language understanding (using Bert)

Check bert_model*.ipynb

## Train a retrieval model with new data

### Use the same wiki data

1. create new configuration file `configs/config.json` and reflect your directory structure
2. run `python3 pipeline.py --config configs/config.json --model [arbitrary name]`

### Use a new/different wiki-pages data

1. remove index files in `data` directory
2. run `python3 doc_ir_model.py` to create a document index and retrieval model
3. run `python3 line_ir_model.py` to create a line index and retrieval model

### `*.sh`

Setting up environment or Run pipeline script

### `pipeline.py`

Main entrance

### `get_evidence.py`, `*_ir*.py`

Information Retrieval module.

### `bert_model*.ipynb`

NLU module with Bert (TPU necessary)

### `config_parser.py`, `fever_io.py`, `util.py`, `stoplist`

Helper modules
