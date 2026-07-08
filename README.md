# EOS -- Enlightened Operating System v21.0.0

[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

A prompt engineering framework that shapes Claude's behavior through structured context displacement. v21 adds compaction-surviving state persistence via hooks and an architecturally forked slim kernel.

---

## What is EOS?

Large language models generate from training priors by default. Every response pattern-completes from the statistical distribution the model learned during training. Rules and system instructions attempt to filter this output after the fact -- but the generation frame is already set before any rule fires.

EOS takes a different approach: **context-staging**. Instead of filtering outputs, EOS displaces the generation frame itself by loading specific user context into the attention window before anything else. The model's causal attention is unidirectional -- each token attends only to tokens before it. By positioning user-specific context (domain expertise, methodology, vocabulary, project state) ahead of identity declarations and rules, the weights pattern-complete from that context rather than from generic training priors.

The result: responses that reflect the user's actual operating environment instead of the model's parametric defaults.
