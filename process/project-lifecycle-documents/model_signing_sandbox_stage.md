## Application for creating a new project at Sandbox stage

### List of project maintainers

The project has 4 maintainers from 3 different organizations:

*  Laurent Simon, Google, @laurentsimon
*  Daniel Major, NVidia,
*  Eoin Wickens, HiddenLayer, @EWickens
*  Mihai Maruseac, Google, @mihaimaruseac

### Mission of the project

The project must be aligned with the OpenSSF mission and either be a novel
approach for existing areas, address an unfulfilled need, or be initial code
needed for OpenSSF WG work. It is preferred that extensions of existing OpenSSF
projects collaborate with the existing project rather than seek a new project.

> Create a cryptographic signing specification for artificial intelligence and
> machine learning models, addressing challenges such as very large models that
> can be used separately, and the signing of multiple disparate file formats
> held within a directory. This specification may have wider applicability to
> signing directories of multiple arbitrary file formats. This specification may
> later be proposed as a formal standard.

#### Specific Goals Include:

* Develop standards for efficient hashing of large models
* Develop standards for efficient verification of models that contain multiple
  formats in the same place
* Develop standards for efficient verification of models at inference time.

To achieve these goals, we work on developing
https://github.com/sigstore/model-transparency library as an OSS standard for ML
models signing and verification. The aim of this project is to guide the
`model-transparency` development and help in standardizing hashing,
verification, and deployment (e.g., model signature format).

#### Non-Goals Include:

* Developing a new model format
* Handling security of ML outputs

### OpenSSF Mission Alignment

We believe our mission aligns with the OpenSSF mission in the following ways:

> make it easier to sustainably secure the development, maintenance, and
> consumption of the open source software

The model signing project aims to reduce the complexity of signing and verifying
the integrity of models, making it easier to be adopted by the industry at
large.

> fostering collaboration

The library is developed by a cohort of independent companies working together
to solve common problems. The goal is to integrate the library with most tools
that ML practitioners use, to uplift the entire ecosystem.

> establishing best practices

The model signing library must be strongly tested. It should define standards
for efficiently hashing and verifying integrity of models.

### AI/ML Security WG Alignment

This project started in parallel with the AI/ML Security WG. During one meeting
of the WG, it was decided to spin up a SIG for model signing
(https://github.com/ossf/ai-ml-security/issues/10). Since the output of this SIG
is in code for this library and associated standards and specs, we need to make
this a project.

### IP policy and licensing due diligence

When contributing an existing Project to the OpenSSF, the contribution must
undergo license and IP due diligence by the Linux Foundation (LF).

* Yes:
  * Library code under
    [`model_transparency`](https://github.com/sigstore/model-transparency) is
    part of Sigstore, which is already an OpenSSF (thus, LF) member
  * Standardization work, etc. will occur under a new repository to be created
    under OpenSSF

### Project References

The project should provide a list of existing resources with links to the repository, and if available, website, a roadmap, contributing guide, demos and walkthroughs, and any other material to showcase the existing breadth, maturity, and direction of the project.

| Reference          | URL |
|--------------------|-----|
| Main Repository    | TODO |
| Contributing guide | TODO |
| Security.md        | TODO |
| Roadmap            | TODO |
| Demos              | TODO |
| Other              | TODO |
