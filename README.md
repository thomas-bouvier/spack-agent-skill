# spack-agent-skill

Generative-AI Assisted Generation of Spack Package Recipes

Duration: 6 months

Where: Maison de la Simulation, CEA Saclay, France

Supervisors:
- Benoît Martin, MdlS, bmartin@cea.fr
- Thomas Padioleau, MdlS, thomas.padioleau@cea.fr
- Thomas Bouvier, MdlS, thomas.bouvier@cea.fr

> [!IMPORTANT]
> The following is largely inspired by https://hepsoftwarefoundation.org/gsoc/2026/proposal_Spack_AIAssistedTesting.html.

## Description

Spack is a package manager for supercomputers. It is commonly used in high-performance computing (HPC) environments of all scales: examples include [kinetic and gyrokinetic problems on exascale architectures](https://gyselax.github.io/), AI inference stacks on smaller clusters or even local development environments.

Spack recipes are Python installation scripts defining how packages should be installed. They define properties and behaviors of the build, such as where to find and how to retrieve the software; its dependencies; and options for building from source. Recipes leverage declarative package directives named _specs_ to express all the
intersecting and disjoint compatibilities that one version of a package has with another.
This allows for the necessary flexibility in scientific stacks where we may want to keep some dependencies at older versions while upgrading other dependencies to newer versions (for reasons of reproducibility and stability).

However, this flexibility comes at the cost of increased complexity in writing Spack recipes, especially for the
numerous, complex dependencies of scientific stacks involving multiple languages and toolchains.
Based on recent advances in generative AI, it would appear to be feasible to develop agentic skills 1) to automate the
generation of such Spack recipes, and 2) to assist in the identification and creation of test scenarios to ensure the quality of the produced recipes. Such work implies developing a methodology to reuse existing Spack utilities, AI agentic frameworks and CI tooling. The effectiveness of the generative-AI assisted approach should be evaluated.

## Material

- A similar internship topic: https://hepsoftwarefoundation.org/gsoc/2026/proposal_Spack_AIAssistedTesting.html
- A repository streamlining agent skills: https://github.com/huggingface/skills
- PyPI to Spack package.py: https://github.com/spack/pypi-to-spack-package
- An agent example: https://github.com/karpathy/autoresearch
- https://github.com/danielmiessler/Fabric

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
