# Targets — LLM

Pick **2 primaries + 2 secondaries**. Verify each repo's CONTRIBUTING and good-first-issue queue before starting.

| Repo | Why | First moves |
|---|---|---|
| **huggingface/transformers** ⭐ primary | #1 LLM repo, GSoC org, endless issue stream | docs fixes → model-image test fixes → small model additions |
| **vllm-project/vllm** ⭐ | Inference king; employers love it | issue triage, scheduler/attention tests |
| **ggml-org/llama.cpp** | C/C++, huge traffic | kitchen-sink list fixes, quantization edge cases |
| **stanfordnlp/dspy** ⭐ | Fast-rising, friendly maintainers | prompt-optimizer improvements, docs |
| pytorch/torchtune · torchao | Foundation credibility | recipe additions, benchmark entries |
| hiyouga/LLaMA-Factory | Finetuning, very active | chat-template fixes, backend patches |
| volcengine/verl | RL post-training, hottest 2026 area | rollout/FSDP fixes, config tests |
| EleutherAI/lm-evaluation-harness | Standard eval harness | new task adapters, docs |
| ml-explore/mlx | Apple silicon | kernel ops, example ports |
| allenai/OLMo · olmocr | Open science | data pipeline fixes |
| deepseek-ai/open-infra-index | CUDA elite track | DeepGEMM/FlashMLA-adjacent issues (hard mode) |
| openai/triton | Compiler track | tutorials, layout/typing tests |
| langchain-ai/langchain · langgraph | Agents | integration fixes, docs, middleware |
| microsoft/autogen | Multi-agent | bug fixes, example modernization |
| QwenLM/Qwen-Agent | Frontier-lab open source | cookbooks, tool-call fixes |
| zai-org/GLM repos · moonshotai/Kimi-K2 | Frontier labs | inference patches, docs |

**Progression path:** docs/tests → good-first-issue bugs → one owned module (e.g. a model family's tests) → a large feature (new model/backend support).

**Proof of depth for GSoC/Claude OSS:** one large merged PR per primary org by January — e.g. adding a new small model to transformers with tests + docs, or an optimization in vLLM with before/after benchmarks.
