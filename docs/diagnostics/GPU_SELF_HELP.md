Got it 👍
Below is a **clean, product-focused self-help guide** with **no references to LM Studio or any other product**.
This is suitable to post **directly in your repo**.

---

# 🚑 GPU / CUDA Quick Self-Help (Windows)

If GPU acceleration is not working, follow this checklist **in order**.
Most GPU issues on Windows are caused by **missing CUDA runtime libraries**, not by the GPU itself.

---

## ✅ Step 1: Verify NVIDIA GPU & driver

Open **Command Prompt** and run:

```bat
nvidia-smi
```

### Expected

* NVIDIA GPU is listed
* No error message

### If this fails

* NVIDIA driver is missing or not working
* GPU acceleration is **not possible**

👉 Install or update the NVIDIA driver before continuing.

---

## ✅ Step 2: Check required CUDA runtime libraries

Our runtime requires the following CUDA libraries to be available on Windows:

```
cudart64_*.dll
cublas64_*.dll
cublasLt64_*.dll
```

Run:

```bat
where cudart64_*.dll
where cublas64_*.dll
where cublasLt64_*.dll
```

### Expected

All commands return paths similar to:

```
C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v12.x\bin\...
```

### Common failure

* `cudart64_*.dll` is found
* `cublas64_*.dll` and `cublasLt64_*.dll` are **missing**

This means **CUDA Toolkit is not installed**.

> NVIDIA drivers alone do NOT install these libraries on Windows.

---

## ✅ Step 3: Install NVIDIA CUDA Toolkit (Required)

Download and install **CUDA Toolkit 12.x** from the official NVIDIA site:

👉 [https://developer.nvidia.com/cuda-downloads](https://developer.nvidia.com/cuda-downloads)

Select:

* **Operating System**: Windows
* **Architecture**: x86_64
* **Version**: Windows 10 / 11
* **Installer Type**: exe (local)

After installation:

1. Restart your terminal
2. Re-run Step 2

---

## ✅ Step 4: Verify CUDA Toolkit installation

Run:

```bat
nvcc --version
```

### Expected

* CUDA version (12.x) is printed

If `nvcc` is not recognized, CUDA Toolkit is not installed correctly.

---

## ✅ Step 5: Verify GPU support in our runtime

From the directory containing `llama-server.exe`, run:

```bat
llama-server.exe --version
```

### Expected

Output mentions:

```
CUDA
ggml-cuda
loaded CUDA backend
```

If only CPU backends are shown, GPU acceleration **will not be used**.

---

## 🛠️ Automated diagnosis (recommended)

If GPU is still not working, run:

```bat
python diagnose_gpu.py
```

This script will:

* Detect GPU availability
* Check CUDA runtime libraries
* Tell you **exactly what is missing**
* Provide clear next steps

---

## 🧠 Summary

GPU acceleration requires **all** of the following:

| Requirement                | Status   |
| -------------------------- | -------- |
| NVIDIA GPU                 | Required |
| NVIDIA Driver              | Required |
| CUDA Toolkit (12.x)        | Required |
| `cublas64_*.dll`           | Required |
| Runtime loads CUDA backend | Required |

If **any** item is missing, GPU acceleration cannot be enabled.

---

This resolves the majority of GPU issues on Windows.
If problems persist, please include the output of `diagnose_gpu.py` when opening an issue.
