### FIDDLER: CPU-GPU ORCHESTRATION FOR FAST  INFERENCE OF MIXTURE-OF-EXPERTS MODELS
- 仅将CPU资源用于MoE层，GPU资源用于非MoE层
- 24GB内存的单一GPU上运行超过90GB参数的Mixtral-8x7B模型
---
### SwapMoE: Serving Off-the-shelf MoE-based Large Language Models with  Tunable Memory Budget
- 通过动态虚拟专家选择与异步更新机制，结合离线遗传算法优化内存分配
- 在无需修改预训练模型的前提下，显著降低混合专家（MoE）模型的内存占用（如从14.2 GiB降至4.7 GiB）和推理延迟（减少50%）
---
### DAOP: Data-Aware Offloading and Predictive  Pre-Calculation for Efficient MoE Inference
- 将非关键专家卸载到CPU并根据预测选择性预计算，优化了GPU和CPU的并行执行，
---
### AdapMoE: Adaptive Sensitivity-based Expert Gating  and Management for Efficient MoE Inference
- 自适应专家预取：利用层间激活相似性，通过前一层的门控决策预测后续层所需的专家，提前加载。
- 缓存分配建模为背包问题，目标是最小化按需加载开销。通过离线分析层的敏感性和预取准确性，分配不同层的缓存大小，优先满足高敏感性或低预取准确性的层。
---
### VLLM
