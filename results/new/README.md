# New Experiment: Prompt Length Shift Analysis

## 1. Motivation

The original Prompt-DT experiment evaluates few-shot policy generalization with a fixed trajectory prompt length.

In this additional experiment, we investigate the influence of changing the test-time prompt length while keeping the trained model unchanged.

The purpose is to observe whether Prompt-DT maintains stable performance when the number of demonstration trajectories provided during inference changes.

---

## 2. Experimental Design

### Model

- Algorithm: Prompt-DT
- Environment: MuJoCo HalfCheetahDir
- Dataset mode: Expert
- Training iterations: 500

### Training Setting

| Parameter | Value |
|---|---|
| Training prompt length | 5 |
| Training tasks | cheetah_dir |
| Training model | Prompt-DT |

### Testing Setting

The trained model is directly loaded and evaluated with different test prompt lengths.

| Experiment | Train Prompt Length | Test Prompt Length | Evaluation Episodes |
|---|---|---|---|
| Exp1 | 5 | 5 | 5 |
| Exp2 | 5 | 2 | 10 |
| Exp3 | 5 | 10 | 10 |

---

## 3. Evaluation Metrics

The experiments report:

- Return Mean: average episode reward
- Return Std: standard deviation of evaluation performance

Higher Return Mean indicates better task completion performance.

Lower Std indicates more stable behavior.

---

## 4. Results

The obtained results are stored in:
summary.xlsx

The experiments evaluate two target tasks:

- cheetah_dir-0
- cheetah_dir-1

---


