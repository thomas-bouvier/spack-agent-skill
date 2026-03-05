# spack-agent-skill

Generative-AI Assisted Generation and Testing of Spack Package Recipes

> [!IMPORTANT]
> The following is largely inspired by https://hepsoftwarefoundation.org/gsoc/2026/proposal_Spack_AIAssistedTesting.html.

## Description

Spack is a flexible package manager widely used in high-performance computing (HPC) to manage complex software stacks. It is commonly used in HPC environments, including kinetic and gyrokinetic problems on exascale architectures or AI inference services on smaller clusters. Spack is becoming the standard approach to manage complex software dependencies in complex scientific software stacks.

In contrast to traditional package managers, Spack is designed to support multiple versions with multiple variants at the same time. This allows for the necessary flexibility in scientific environments where for reasons of reproducibility and stability we may want to keep some dependencies at older versions while upgrading other dependencies to newer versions. However, this flexibility comes at the cost of increased complexity in testing the Spack packages, where the focus of testing is typically on the leading-edge configurations: the newest versions with the newest dependencies. This can lead to subtle and invisible breakages in configurations where older packages are combined with newer packages in user-defined configurations.

Based on recent advances in generative AI, it would appear to be feasible to compose specific test scenarios (away from the leading-edge of package versions already tested in CI) that are most likely to uncover breakages in Spack packages. For example, if a package has no upper limits on its dependency versions but other packages do typically have upper limits, then this may indicate that also here upper limits should be added.

This project will explore how generative AI can be used to assist in the identification and creation of such test scenarios for complex stacks of Spack packages, while at the same time developing a methodology to validate the effectiveness of the generated tests and reduce the probability of running large numbers of ineffective tests or repeated tests.

Once this is achieved, we would be confident to explore how Spack package recipes could be generated using AI.

## Material

- A similar internship topic: https://hepsoftwarefoundation.org/gsoc/2026/proposal_Spack_AIAssistedTesting.html
- A repository streamlining agent skills: https://github.com/huggingface/skills
- PyPI to Spack package.py https://github.com/spack/pypi-to-spack-package

## Task Ideas

- Develop a scalable method to summarize information from multiple Spack packages for input into generative AI models
- Develop a method to record and propagate past successful test scenarios to avoid generating duplicate tests
- Develop a strategy to schedule and run generated test scenarios in an efficient manner
- Develop a methodology to validate the effectiveness of generated test scenarios in uncovering breakages
- Develop a methodology to generate Spack recipes automatically

## Expected Results and Milestones

- Familiarization with Spack’s packaging practices and testing infrastructure
- Analyze classes of common off-leading-edge configurations that may lead to breakages
- Summarization of potential strategies for generative-AI assisted test generation
- Design of a solution for generative-AI assisted test generation
- Test the design in the context of Spack packages
- Try generated recipes for Python packages automatically, and validate them using the design solution

## Requirements

- Python programming skills
- Generative AI knowledge and experience
- Packaging and build system knowledge
- Interest in scientific software stacks

## AI Policy

AI assistance is allowed for this contribution. The applicant takes full responsibility for all code and results, disclosing AI use for non-routine tasks (algorithm design, architecture, complex problem-solving). Routine tasks (grammar, formatting, style) do not require disclosure.
