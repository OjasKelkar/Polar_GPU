# Polars GPU Engine 🚀  

Polars is a high-performance DataFrame library designed for single-machine use and powered by an OLAP Query Engine. Starting from version **v1.3**, Polars introduces **GPU acceleration** through the NVIDIA RAPIDS cuDF engine, enabling interactive data processing for datasets ranging from 10–100+ GB with just a single GPU.

---

## 🔑 **Key Features**  

- **GPU Acceleration**: Leverage NVIDIA GPUs for significantly faster data processing.  
- **Interactive Large Data Handling**: Process large datasets (10–100+ GB) seamlessly and interactively.  
- **Seamless Integration**: Use `engine="gpu"` in the Polars Lazy API's `collect` operation to enable GPU acceleration.  
- **Optimized Execution**: Powered by Polars’ optimizer for efficient computation and minimal memory usage.  
- **Ecosystem Compatibility**: Fully compatible with existing Polars tools and libraries.  
- **Graceful Fallback**: Queries not supported on GPUs will automatically fall back to CPU execution.

---

## 🛠️ **Getting Started**  

1. Install Polars with GPU support:  
   ```bash  
   pip install polars[cudf]  
   ```  

2. Enable the GPU engine:  
   ```python  
   import polars as pl  

   df = pl.DataFrame({  
       "a": [1, 2, 3],  
       "b": [4, 5, 6]  
   }).lazy()  

   result = df.collect(engine="gpu")  # Enable GPU acceleration  
   print(result)  
   ```  

---

## 📚 **Documentation and Resources**  

- [Polars Documentation](https://pola.rs)  
- [RAPIDS cuDF](https://rapids.ai)  

---

## 🛡️ **Support and Contributions**  

Feel free to open issues or contribute to the project! We welcome feedback and feature requests.  

---

**Get ready to unlock the power of GPUs with Polars v1.3!** 🎉
