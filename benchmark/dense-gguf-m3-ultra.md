### llama-bench
```bash
% llama-cli --version
version: 8500 (342d6125b)
built with AppleClang 17.0.0.17000604 for Darwin arm64
```

### MacStudio M3Ultra 512Gb, macOS 15.6 (24G84)

* unsloth/Qwen3.5-0.8B-GGUF
```bash
% llama-bench -hf unsloth/Qwen3.5-0.8B-GGUF:Q4_K_M -p 1500 -r 2
% llama-bench -hf unsloth/Qwen3.5-0.8B-GGUF:Q4_K_M -d 1500 -n 1500 -r 2
```

| model                          |       size |     params | backend    | threads |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | ------: | --------------: | -------------------: |
| qwen35 0.8B BF16               |   1.40 GiB |   752.39 M | BLAS,MTL   |      24 |          pp1500 |      11790.57 ± 6.58 |
| qwen35 0.8B BF16               |   1.40 GiB |   752.39 M | BLAS,MTL   |      24 |   pp512 @ d1500 |    10815.35 ± 425.92 |
| qwen35 0.8B BF16               |   1.40 GiB |   752.39 M | BLAS,MTL   |      24 |  tg1500 @ d1500 |        172.06 ± 0.37 |
| qwen35 0.8B BF16               |   1.40 GiB |   752.39 M | BLAS,MTL   |      24 |         pp15000 |       9195.09 ± 3.37 |
| qwen35 0.8B BF16               |   1.40 GiB |   752.39 M | BLAS,MTL   |      24 |  pp512 @ d15000 |      6862.80 ± 46.07 |
| qwen35 0.8B BF16               |   1.40 GiB |   752.39 M | BLAS,MTL   |      24 | tg1500 @ d15000 |        141.25 ± 0.51 |
|                                |            |            |            |         |                 |                    n |
| qwen35 0.8B Q8_0               | 763.78 MiB |   752.39 M | BLAS,MTL   |      24 |          pp1500 |      11692.94 ± 1.50 |
| qwen35 0.8B Q8_0               | 763.78 MiB |   752.39 M | BLAS,MTL   |      24 |   pp512 @ d1500 |    10918.38 ± 131.06 |
| qwen35 0.8B Q8_0               | 763.78 MiB |   752.39 M | BLAS,MTL   |      24 |  tg1500 @ d1500 |        203.88 ± 0.06 |
| qwen35 0.8B Q8_0               | 763.78 MiB |   752.39 M | BLAS,MTL   |      24 |         pp15000 |      9154.26 ± 16.29 |
| qwen35 0.8B Q8_0               | 763.78 MiB |   752.39 M | BLAS,MTL   |      24 |  pp512 @ d15000 |      6819.61 ± 76.88 |
| qwen35 0.8B Q8_0               | 763.78 MiB |   752.39 M | BLAS,MTL   |      24 | tg1500 @ d15000 |        160.30 ± 5.22 |
|                                |            |            |            |         |                 |                    n |
| qwen35 0.8B Q4_K - Medium      | 497.39 MiB |   752.39 M | BLAS,MTL   |      24 |          pp1500 |     11080.68 ± 18.47 |
| qwen35 0.8B Q4_K - Medium      | 497.39 MiB |   752.39 M | BLAS,MTL   |      24 |   pp512 @ d1500 |     10277.49 ± 50.20 |
| qwen35 0.8B Q4_K - Medium      | 497.39 MiB |   752.39 M | BLAS,MTL   |      24 |  tg1500 @ d1500 |        209.27 ± 0.59 |
| qwen35 0.8B Q4_K - Medium      | 497.39 MiB |   752.39 M | BLAS,MTL   |      24 |         pp15000 |      8800.21 ± 10.27 |
| qwen35 0.8B Q4_K - Medium      | 497.39 MiB |   752.39 M | BLAS,MTL   |      24 |  pp512 @ d15000 |      6646.87 ± 71.60 |
| qwen35 0.8B Q4_K - Medium      | 497.39 MiB |   752.39 M | BLAS,MTL   |      24 | tg1500 @ d15000 |        165.89 ± 0.48 |

* Qwen/Qwen3-4B-GGUF:Q8_0
```bash
% llama-bench -hf Qwen/Qwen3-4B-GGUF:Q8_0 -p 1500 -r 2
% llama-bench -hf Qwen/Qwen3-4B-GGUF:Q8_0 -d 1500 -n 1500 -r 2
```

| model                          |       size |     params | backend    | threads |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | ------: | --------------: | -------------------: |
| qwen3 4B Q8_0                  |   3.98 GiB |     4.02 B | BLAS,MTL   |      24 |          pp1500 |       2476.80 ± 3.44 |
| qwen3 4B Q8_0                  |   3.98 GiB |     4.02 B | BLAS,MTL   |      24 |   pp512 @ d1500 |       2208.19 ± 6.90 |
| qwen3 4B Q8_0                  |   3.98 GiB |     4.02 B | BLAS,MTL   |      24 |  tg1500 @ d1500 |         76.60 ± 0.03 |
| qwen3 4B Q8_0                  |   3.98 GiB |     4.02 B | BLAS,MTL   |      24 |         pp15000 |       1216.27 ± 1.95 |
| qwen3 4B Q8_0                  |   3.98 GiB |     4.02 B | BLAS,MTL   |      24 |  pp512 @ d15000 |        728.15 ± 1.75 |
| qwen3 4B Q8_0                  |   3.98 GiB |     4.02 B | BLAS,MTL   |      24 | tg1500 @ d15000 |         34.62 ± 0.01 |
|                                |            |            |            |         |                 |                    n |
| qwen3 4B Q6_K                  |   3.07 GiB |     4.02 B | BLAS,MTL   |      24 |          pp1500 |       2343.49 ± 0.87 |
| qwen3 4B Q6_K                  |   3.07 GiB |     4.02 B | BLAS,MTL   |      24 |          tg1500 |         98.93 ± 0.05 |
|                                |            |            |            |         |                 |                    n |
| qwen3 4B Q4_K - Medium         |   2.32 GiB |     4.02 B | BLAS,MTL   |      24 |          pp1500 |       2379.32 ± 2.17 |
| qwen3 4B Q4_K - Medium         |   2.32 GiB |     4.02 B | BLAS,MTL   |      24 |   pp512 @ d1500 |       2100.79 ± 5.50 |
| qwen3 4B Q4_K - Medium         |   2.32 GiB |     4.02 B | BLAS,MTL   |      24 |  tg1500 @ d1500 |         93.05 ± 0.05 |
| qwen3 4B Q4_K - Medium         |   2.32 GiB |     4.02 B | BLAS,MTL   |      24 |         pp15000 |       1192.56 ± 1.68 |
| qwen3 4B Q4_K - Medium         |   2.32 GiB |     4.02 B | BLAS,MTL   |      24 |  pp512 @ d15000 |        718.98 ± 0.39 |
| qwen3 4B Q4_K - Medium         |   2.32 GiB |     4.02 B | BLAS,MTL   |      24 | tg1500 @ d15000 |         37.43 ± 0.01 |

* unsloth/Qwen3.5-4B-GGUF
```bash
% llama-bench -hf unsloth/Qwen3.5-4B-GGUF:Q8_0 -p 1500 -r 2
% llama-bench -hf unsloth/Qwen3.5-4B-GGUF:Q8_0 -d 1500 -n 1500 -r 2
```

| model                          |       size |     params | backend    | threads |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | ------: | --------------: | -------------------: |
| qwen35 4B BF16                 |   7.84 GiB |     4.21 B | BLAS,MTL   |      24 |          pp1500 |       2500.38 ± 4.51 |
| qwen35 4B BF16                 |   7.84 GiB |     4.21 B | BLAS,MTL   |      24 |   pp512 @ d1500 |      2412.19 ± 10.70 |
| qwen35 4B BF16                 |   7.84 GiB |     4.21 B | BLAS,MTL   |      24 |  tg1500 @ d1500 |         57.25 ± 0.05 |
| qwen35 4B BF16                 |   7.84 GiB |     4.21 B | BLAS,MTL   |      24 |         pp15000 |       2145.97 ± 3.66 |
| qwen35 4B BF16                 |   7.84 GiB |     4.21 B | BLAS,MTL   |      24 |  pp512 @ d15000 |       1791.84 ± 3.85 |
| qwen35 4B BF16                 |   7.84 GiB |     4.21 B | BLAS,MTL   |      24 | tg1500 @ d15000 |         50.03 ± 0.04 |
|                                |            |            |            |         |                 |                    n |
| qwen35 4B Q8_0                 |   4.16 GiB |     4.21 B | BLAS,MTL   |      24 |          pp1500 |       2505.23 ± 8.99 |
| qwen35 4B Q8_0                 |   4.16 GiB |     4.21 B | BLAS,MTL   |      24 |   pp512 @ d1500 |       2434.79 ± 9.12 |
| qwen35 4B Q8_0                 |   4.16 GiB |     4.21 B | BLAS,MTL   |      24 |  tg1500 @ d1500 |         82.30 ± 0.12 |
| qwen35 4B Q8_0                 |   4.16 GiB |     4.21 B | BLAS,MTL   |      24 |         pp15000 |       2152.25 ± 2.26 |
| qwen35 4B Q8_0                 |   4.16 GiB |     4.21 B | BLAS,MTL   |      24 |  pp512 @ d15000 |       1795.83 ± 4.94 |
| qwen35 4B Q8_0                 |   4.16 GiB |     4.21 B | BLAS,MTL   |      24 | tg1500 @ d15000 |         67.98 ± 0.06 |
|                                |            |            |            |         |                 |                    n |
| qwen35 4B Q4_K - Medium        |   2.54 GiB |     4.21 B | BLAS,MTL   |      24 |          pp1500 |       2365.25 ± 0.40 |
| qwen35 4B Q4_K - Medium        |   2.54 GiB |     4.21 B | BLAS,MTL   |      24 |   pp512 @ d1500 |       2290.02 ± 5.62 |
| qwen35 4B Q4_K - Medium        |   2.54 GiB |     4.21 B | BLAS,MTL   |      24 |  tg1500 @ d1500 |         98.73 ± 0.01 |
| qwen35 4B Q4_K - Medium        |   2.54 GiB |     4.21 B | BLAS,MTL   |      24 |         pp15000 |       2054.96 ± 0.94 |
| qwen35 4B Q4_K - Medium        |   2.54 GiB |     4.21 B | BLAS,MTL   |      24 |  pp512 @ d15000 |       1719.39 ± 4.49 |
| qwen35 4B Q4_K - Medium        |   2.54 GiB |     4.21 B | BLAS,MTL   |      24 | tg1500 @ d15000 |         79.33 ± 0.04 |
|                                |            |            |            |         |                 |                    n |
| qwen35 4B Q4_0                 |   2.40 GiB |     4.21 B | BLAS,MTL   |      24 |          pp1500 |       2501.44 ± 0.54 |
| qwen35 4B Q4_0                 |   2.40 GiB |     4.21 B | BLAS,MTL   |      24 |   pp512 @ d1500 |      2411.61 ± 12.93 |
| qwen35 4B Q4_0                 |   2.40 GiB |     4.21 B | BLAS,MTL   |      24 |  tg1500 @ d1500 |        103.26 ± 0.09 |
| qwen35 4B Q4_0                 |   2.40 GiB |     4.21 B | BLAS,MTL   |      24 |         pp15000 |       2145.97 ± 0.99 |
| qwen35 4B Q4_0                 |   2.40 GiB |     4.21 B | BLAS,MTL   |      24 |  pp512 @ d15000 |       1786.90 ± 4.51 |
| qwen35 4B Q4_0                 |   2.40 GiB |     4.21 B | BLAS,MTL   |      24 | tg1500 @ d15000 |         82.18 ± 0.05 |

* unsloth/Qwen3.5-27B-GGUF
```bash
% llama-bench -hf unsloth/Qwen3.5-27B-GGUF:Q8_0 -p 1500 -r 2
% llama-bench -hf unsloth/Qwen3.5-27B-GGUF:Q8_0 -d 1500 -n 1500 -r 2
```

| model                          |       size |     params | backend    | threads |            test |                  t/s |
| ------------------------------ | ---------: | ---------: | ---------- | ------: | --------------: | -------------------: |
| qwen35 27B Q8_0                |  26.62 GiB |    26.90 B | BLAS,MTL   |      24 |          pp1500 |        419.97 ± 0.12 |
| qwen35 27B Q8_0                |  26.62 GiB |    26.90 B | BLAS,MTL   |      24 |   pp512 @ d1500 |        417.58 ± 0.38 |
| qwen35 27B Q8_0                |  26.62 GiB |    26.90 B | BLAS,MTL   |      24 |  tg1500 @ d1500 |         19.34 ± 0.03 |
| qwen35 27B Q8_0                |  26.62 GiB |    26.90 B | BLAS,MTL   |      24 |         pp15000 |        388.51 ± 0.12 |
| qwen35 27B Q8_0                |  26.62 GiB |    26.90 B | BLAS,MTL   |      24 |  pp512 @ d15000 |        350.30 ± 0.50 |
| qwen35 27B Q8_0                |  26.62 GiB |    26.90 B | BLAS,MTL   |      24 | tg1500 @ d15000 |         17.22 ± 0.03 |
| qwen35 27B Q8_0                |  26.62 GiB |    26.90 B | BLAS,MTL   |      24 |        pp100000 |        231.88 ± 0.00 |
| qwen35 27B Q8_0                |  26.62 GiB |    26.90 B | BLAS,MTL   |      24 | pp512 @ d100000 |        154.90 ± 0.00 |
| qwen35 27B Q8_0                |  26.62 GiB |    26.90 B | BLAS,MTL   |      24 |tg1000 @ d100000 |          9.10 ± 0.00 |
|                                |            |            |            |         |                 |                    n |
| qwen35 27B Q4_K - Medium       |  15.58 GiB |    26.90 B | BLAS,MTL   |      24 |          pp1500 |        397.94 ± 0.22 |
| qwen35 27B Q4_K - Medium       |  15.58 GiB |    26.90 B | BLAS,MTL   |      24 |   pp512 @ d1500 |        393.24 ± 0.86 |
| qwen35 27B Q4_K - Medium       |  15.58 GiB |    26.90 B | BLAS,MTL   |      24 |  tg1500 @ d1500 |         26.76 ± 0.01 |
| qwen35 27B Q4_K - Medium       |  15.58 GiB |    26.90 B | BLAS,MTL   |      24 |         pp15000 |        368.43 ± 0.03 |
| qwen35 27B Q4_K - Medium       |  15.58 GiB |    26.90 B | BLAS,MTL   |      24 |  pp512 @ d15000 |        335.74 ± 0.14 |
| qwen35 27B Q4_K - Medium       |  15.58 GiB |    26.90 B | BLAS,MTL   |      24 | tg1500 @ d15000 |         22.54 ± 0.00 |
| qwen35 27B Q4_K - Medium       |  15.58 GiB |    26.90 B | BLAS,MTL   |      24 |        pp100000 |        224.76 ± 0.00 |
| qwen35 27B Q4_K - Medium       |  15.58 GiB |    26.90 B | BLAS,MTL   |      24 | pp512 @ d100000 |        151.89 ± 0.00 |
| qwen35 27B Q4_K - Medium       |  15.58 GiB |    26.90 B | BLAS,MTL   |      24 |tg1000 @ d100000 |         10.44 ± 0.00 |
