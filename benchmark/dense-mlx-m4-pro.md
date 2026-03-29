### mlx.benchmark cmd example
```bash
% mlx_lm.benchmark --model mlx-community/MiniMax-M2-8bit -p 1500 -g 1500 -n 2

% mlx_lm --version
0.31.1
```

### MacBook Pro, Apple M4 Pro 24Gb, macOS 15.7.3 (24G419)

#### 4B

* mlx-community/Qwen3.5-4B-8bit
```bash
mlx_lm.benchmark  --model mlx-community/Qwen3.5-4B-8bit -p 1500 -g 1500 -n 2
  Averages: prompt_tps=658.436, generation_tps=49.029, peak_memory=5.900
mlx_lm.benchmark  --model mlx-community/Qwen3.5-4B-8bit -p 15000 -g 1500 -n 2
  Averages: prompt_tps=604.370, generation_tps=43.903, peak_memory=7.477
```

* mlx-community/Qwen3.5-4B-4bit
```bash
mlx_lm.benchmark  --model mlx-community/Qwen3.5-4B-4bit -p 1500 -g 1500 -n 2
  Averages: prompt_tps=663.588, generation_tps=83.285, peak_memory=3.798
mlx_lm.benchmark  --model mlx-community/Qwen3.5-4B-4bit -p 15000 -g 1500 -n 2
  Averages: prompt_tps=609.229, generation_tps=70.144, peak_memory=5.495
```

#### <1B
* mlx-community/Qwen3.5-0.8B-8bit
```bash
mlx_lm.benchmark  --model mlx-community/Qwen3.5-0.8B-8bit -p 1500 -g 1500 -n 2
  Averages: prompt_tps=3874.724, generation_tps=219.631, peak_memory=2.108
mlx_lm.benchmark  --model mlx-community/Qwen3.5-0.8B-8bit -p 15000 -g 1500 -n 2
  Averages: prompt_tps=3264.349, generation_tps=186.421, peak_memory=3.088
```

* mlx-community/Qwen3.5-0.8B-4bit
```bash
mlx_lm.benchmark  --model mlx-community/Qwen3.5-0.8B-4bit -p 1500 -g 1500 -n 2
  Averages: prompt_tps=3872.238, generation_tps=320.337, peak_memory=1.751
mlx_lm.benchmark  --model mlx-community/Qwen3.5-0.8B-4bit -p 15000 -g 1500 -n 2
  Averages: prompt_tps=3271.095, generation_tps=251.475, peak_memory=2.712
```
