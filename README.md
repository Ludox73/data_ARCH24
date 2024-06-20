# Benchmark Proposal Archive

The following archive accompanies the benchmark proposal "**Stability Verification of an Industrial Switched PI Control Systems**", presented to ARCH 24.

It contains several `.mat` files to be read with MATLAB. Each `.mat` file contains the elements that describe the system as in Equation (12) in the accompanying paper. 

- The original benchmark is given in the file **data_size_18.mat**.
- Other files correspond to the systems obtained by Truncation Model Reduction or Truncation to Integer values; these are described in Section 5 of the paper.

To import the data, extract the archive in a folder and open it in MATLAB. Then, launch
```
load('data_size_18.mat')
```
substituting the name of the file with the one you are interested into.

Doing this, several variables will be uploaded in your workspace. They correspond to:

- `A_0, A_1, L, g_t_C, h` correspond to the variables in Equation (12);
- `A, B, C, KP_0, KP_1, KI_0, KI_1` describe the open-loop system as described in Section 4.2.

The versions trunceted to integer values contain variables with name that ends with `trunc`.

## Symbolic guarantees

In previous works on this benchmarks, the data was elaborated as the ground truth; in particular, the entries were considered as rational numbers. The symbolic (i.e. rational) version of each matrix can be obtained on MATLAB using the `sym` function, e.g.
```
A_0 = sym(A_0)
```