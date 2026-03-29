### llama-bench
```bash
% llama-cli --version
version: 8500 (342d6125b)
built with AppleClang 17.0.0.17000604 for Darwin arm64
```

### MacBook Pro, Apple M4 Pro 24Gb, macOS 15.7.3 (24G419)

* unsloth/Qwen3.5-0.8B-GGUF
```bash
llama-bench -hf unsloth/Qwen3.5-0.8B-GGUF:Q4_K_M -p 1500 -r 2
llama-bench -hf unsloth/Qwen3.5-0.8B-GGUF:Q4_K_M -d 1500 -n 1500 -r 2
```

| model                          |       size |     params | backend    | threads |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | ------: | --------------: | -------------------: |
| qwen35 0.8B Q8_0               | 763.78 MiB |   752.39 M | BLAS,MTL   |       8 |          pp1500 |       3403.16 ± 7.75 |
| qwen35 0.8B Q8_0               | 763.78 MiB |   752.39 M | BLAS,MTL   |       8 |   pp512 @ d1500 |       3232.40 ± 4.89 |
| qwen35 0.8B Q8_0               | 763.78 MiB |   752.39 M | BLAS,MTL   |       8 |  tg1500 @ d1500 |        108.53 ± 0.27 |
| qwen35 0.8B Q8_0               | 763.78 MiB |   752.39 M | BLAS,MTL   |       8 |         pp15000 |       2793.11 ± 3.83 |
| qwen35 0.8B Q8_0               | 763.78 MiB |   752.39 M | BLAS,MTL   |       8 |  pp512 @ d15000 |       2129.47 ± 1.41 |
| qwen35 0.8B Q8_0               | 763.78 MiB |   752.39 M | BLAS,MTL   |       8 | tg1500 @ d15000 |         83.29 ± 0.13 |
|                                |            |            |            |         |                 |                    n |
| qwen35 0.8B Q4_K - Medium      | 497.39 MiB |   752.39 M | BLAS,MTL   |       8 |          pp1500 |      3399.52 ± 10.27 |
| qwen35 0.8B Q4_K - Medium      | 497.39 MiB |   752.39 M | BLAS,MTL   |       8 |   pp512 @ d1500 |      3257.37 ± 13.42 |
| qwen35 0.8B Q4_K - Medium      | 497.39 MiB |   752.39 M | BLAS,MTL   |       8 |  tg1500 @ d1500 |        134.12 ± 0.13 |
| qwen35 0.8B Q4_K - Medium      | 497.39 MiB |   752.39 M | BLAS,MTL   |       8 |         pp15000 |       2673.47 ± 0.18 |
| qwen35 0.8B Q4_K - Medium      | 497.39 MiB |   752.39 M | BLAS,MTL   |       8 |  pp512 @ d15000 |       2065.77 ± 7.95 |
| qwen35 0.8B Q4_K - Medium      | 497.39 MiB |   752.39 M | BLAS,MTL   |       8 | tg1500 @ d15000 |         97.40 ± 0.02 |

* unsloth/Qwen3.5-0.8B-GGUF
```bash
llama-bench -hf unsloth/Qwen3.5-4B-GGUF:Q4_K_M -p 1500 -r 2
llama-bench -hf unsloth/Qwen3.5-4B-GGUF:Q4_K_M -d 1500 -n 1500 -r 2
```

| model                          |       size |     params | backend    | threads |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | ------: | --------------: | -------------------: |
| qwen35 4B Q8_0                 |   4.16 GiB |     4.21 B | BLAS,MTL   |       8 |          pp1500 |        648.64 ± 0.30 |
| qwen35 4B Q8_0                 |   4.16 GiB |     4.21 B | BLAS,MTL   |       8 |   pp512 @ d1500 |        636.70 ± 0.39 |
| qwen35 4B Q8_0                 |   4.16 GiB |     4.21 B | BLAS,MTL   |       8 |  tg1500 @ d1500 |         37.86 ± 0.02 |
| qwen35 4B Q8_0                 |   4.16 GiB |     4.21 B | BLAS,MTL   |       8 |         pp15000 |        556.32 ± 6.20 |
| qwen35 4B Q8_0                 |   4.16 GiB |     4.21 B | BLAS,MTL   |       8 |  pp512 @ d15000 |        491.57 ± 0.89 |
| qwen35 4B Q8_0                 |   4.16 GiB |     4.21 B | BLAS,MTL   |       8 | tg1500 @ d15000 |         30.04 ± 0.03 |
|                                |            |            |            |         |                 |                    n |
| qwen35 4B Q4_K - Medium        |   2.54 GiB |     4.21 B | BLAS,MTL   |       8 |          pp1500 |        611.94 ± 0.71 |
| qwen35 4B Q4_K - Medium        |   2.54 GiB |     4.21 B | BLAS,MTL   |       8 |   pp512 @ d1500 |        600.03 ± 0.39 |
| qwen35 4B Q4_K - Medium        |   2.54 GiB |     4.21 B | BLAS,MTL   |       8 |  tg1500 @ d1500 |         45.55 ± 0.05 |
| qwen35 4B Q4_K - Medium        |   2.54 GiB |     4.21 B | BLAS,MTL   |       8 |         pp15000 |        542.80 ± 0.26 |
| qwen35 4B Q4_K - Medium        |   2.54 GiB |     4.21 B | BLAS,MTL   |       8 |  pp512 @ d15000 |        468.70 ± 0.15 |
| qwen35 4B Q4_K - Medium        |   2.54 GiB |     4.21 B | BLAS,MTL   |       8 | tg1500 @ d15000 |         34.49 ± 0.08 |
