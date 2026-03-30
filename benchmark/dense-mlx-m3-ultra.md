### mlx.benchmark cmd example
```bash
% conda activate mlx-playground
% mlx_lm.benchmark --model mlx-community/MiniMax-M2-8bit -p 1500 -g 1500 -n 2

% mlx_lm --version
0.31.2
```

### MacStudio M3Ultra 512Gb, macOS 15.6 (24G84)

#### 27B
* mlx-community/Qwen3.5-27B-8bit
```bash
% mlx_lm.benchmark --model mlx-community/Qwen3.5-27B-8bit -p 1500 -g 1500 -n 2
  Averages: prompt_tps=421.739, generation_tps=21.564, peak_memory=31.034
% mlx_lm.benchmark --model mlx-community/Qwen3.5-27B-8bit -p 15000 -g 1500 -n 2
  Averages: prompt_tps=411.172, generation_tps=20.507, peak_memory=33.796
% mlx_lm.benchmark --model mlx-community/Qwen3.5-27B-8bit -p 100000 -n 1
  Timing with prompt_tokens=100000, generation_tokens=1024, batch_size=1.
  Averages: prompt_tps=287.585, generation_tps=16.633, peak_memory=47.793
```

* mlx-community/Qwen3.5-27B-4bit
```bash
% mlx_lm.benchmark --model mlx-community/Qwen3.5-27B-4bit -p 1500 -g 1500 -n 2
  Averages: prompt_tps=430.756, generation_tps=36.297, peak_memory=17.588
% mlx_lm.benchmark --model mlx-community/Qwen3.5-27B-4bit -p 15000 -g 1500 -n 2
  Averages: prompt_tps=416.036, generation_tps=33.217, peak_memory=20.363
% mlx_lm.benchmark --model mlx-community/Qwen3.5-27B-4bit -p 100000 -n 1
  Averages: prompt_tps=289.364, generation_tps=23.954, peak_memory=34.347
```

#### 4B
* mlx-community/Qwen3-4B-8bit
```bash
% mlx_lm.benchmark --model mlx-community/Qwen3-4B-8bit -p 1500 -g 1500 -n 2
  Averages: prompt_tps=2695.631, generation_tps=104.934, peak_memory=5.278
% mlx_lm.benchmark --model mlx-community/Qwen3-4B-8bit -p 15000 -g 1500 -n 2
  Averages: prompt_tps=1855.621, generation_tps=77.759, peak_memory=7.062
```

* mlx-community/Qwen3-4B-4bit
```bash
% mlx_lm.benchmark --model mlx-community/Qwen3-4B-4bit -p 1500 -g 1500 -n 2
  Averages: prompt_tps=2742.216, generation_tps=150.983, peak_memory=3.267
% mlx_lm.benchmark --model mlx-community/Qwen3-4B-4bit -p 15000 -g 1500 -n 2
  Averages: prompt_tps=1872.776, generation_tps=99.210, peak_memory=5.185
```

* mlx-community/Qwen3.5-4B-bf16
```bash
% mlx_lm.benchmark --model mlx-community/Qwen3.5-4B-bf16 -p 1500 -g 1500 -n 2
  Averages: prompt_tps=2575.877, generation_tps=64.986, peak_memory=9.675
% mlx_lm.benchmark --model mlx-community/Qwen3.5-4B-bf16 -p 15000 -g 1500 -n 2
  Averages: prompt_tps=2481.945, generation_tps=61.660, peak_memory=11.271
```

* mlx-community/Qwen3.5-4B-8bit
```bash
% mlx_lm.benchmark --model mlx-community/Qwen3.5-4B-8bit -p 1500 -g 1500 -n 2
  Averages: prompt_tps=2643.412, generation_tps=105.393, peak_memory=5.929
% mlx_lm.benchmark --model mlx-community/Qwen3.5-4B-8bit -p 15000 -g 1500 -n 2
  Averages: prompt_tps=2456.495, generation_tps=96.357, peak_memory=7.505
```

* mlx-community/Qwen3.5-4B-4bit
```bash
% mlx_lm.benchmark --model mlx-community/Qwen3.5-4B-4bit -p 1500 -g 1500 -n 2
  Averages: prompt_tps=2676.000, generation_tps=156.123, peak_memory=3.827
% mlx_lm.benchmark --model mlx-community/Qwen3.5-4B-4bit -p 15000 -g 1500 -n 2
  Averages: prompt_tps=2478.334, generation_tps=136.378, peak_memory=5.523
```

#### <1B
* mlx-community/Qwen3.5-0.8B-bf16
```bash
% mlx_lm.benchmark --model mlx-community/Qwen3.5-0.8B-bf16 -p 1500 -g 1500 -n 2
  Averages: prompt_tps=13006.053, generation_tps=226.736, peak_memory=2.590
% mlx_lm.benchmark --model mlx-community/Qwen3.5-0.8B-bf16 -p 15000 -g 1500 -n 2
  Averages: prompt_tps=11199.870, generation_tps=204.298, peak_memory=3.775
```

* mlx-community/Qwen3.5-0.8B-8bit
```bash
% mlx_lm.benchmark --model mlx-community/Qwen3.5-0.8B-8bit -p 1500 -g 1500 -n 2
  Averages: prompt_tps=12305.366, generation_tps=304.667, peak_memory=2.122
% mlx_lm.benchmark --model mlx-community/Qwen3.5-0.8B-8bit -p 15000 -g 1500 -n 2
  Averages: prompt_tps=11042.824, generation_tps=267.038, peak_memory=3.100
```

* mlx-community/Qwen3.5-0.8B-4bit
```bash
% mlx_lm.benchmark --model mlx-community/Qwen3.5-0.8B-4bit -p 1500 -g 1500 -n 2
  Averages: prompt_tps=12452.667, generation_tps=366.617, peak_memory=1.765
% mlx_lm.benchmark --model mlx-community/Qwen3.5-0.8B-4bit -p 15000 -g 1500 -n 2
  Averages: prompt_tps=11042.864, generation_tps=314.840, peak_memory=2.724
```

* mlx-community/Qwen3-0.6B-bf16
```bash
% mlx_lm.benchmark --model mlx-community/Qwen3-0.6B-bf16 -p 1500 -g 1500 -n 2
  Averages: prompt_tps=15040.877, generation_tps=230.571, peak_memory=2.017
% mlx_lm.benchmark --model mlx-community/Qwen3-0.6B-bf16 -p 15000 -n 2
  Timing with prompt_tokens=15000, generation_tokens=1024, batch_size=1.
  Averages: prompt_tps=7499.008, generation_tps=142.386, peak_memory=3.402
```

