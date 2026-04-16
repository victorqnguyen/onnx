# all-MiniLM-L6-v2 (ONNX)

Mirror of [Xenova/all-MiniLM-L6-v2](https://huggingface.co/Xenova/all-MiniLM-L6-v2) for fast pulls into ephemeral containers.

## Files

| File | Size | Notes |
|---|---|---|
| `model.onnx` | ~22 MB | int8-quantized — default |
| `model_fp32.onnx` | ~86 MB | full precision |
| `tokenizer.json` | ~695 KB | HF fast tokenizer |
| `tokenizer_config.json`, `config.json`, `special_tokens_map.json` | tiny | metadata |

## Model specs

- 384-dim sentence embeddings
- 256 max sequence length
- mean-pool + L2-normalize the last hidden state to get the sentence vector

## Session boot

```sh
curl -sL https://github.com/victorqnguyen/onnx/raw/main/model.onnx -o /home/claude/model.onnx
curl -sL https://github.com/victorqnguyen/onnx/raw/main/tokenizer.json -o /home/claude/tokenizer.json
```

Source: https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2 (Apache 2.0).
