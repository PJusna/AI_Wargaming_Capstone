# Capstone Description

## Title: GenAI in Support of Wargaming

## Description

Creating believable, realistic, and immersive scenarios in support of wargaming objectives
requires significant time and subject matter expertise. This capstone project proposes developing a
software system that leverages Large Language Models (LLMs) to automate the creation of critical wargaming
artifacts, such as "Road to War" briefs, concepts of operations, intelligence summaries, operational plans,
and operations orders. By utilizing an LLM system capable of generating detailed, context-specific
scenarios and associated products, this project aims to greatly accelerate the wargaming process,
potentially enhance the quality of the generated outputs, and reduce the need for extensive human resources.
The project may explore LLM techniques such as Retrieval-Augmented Generation (RAG), fine-tuning, and
prompt engineering, while also developing a user-friendly interface and ensuring real-time adaptability
based on user feedback. The final product will serve as a proof of concept, demonstrating how LLMs can
be harnessed to enhance and expedite the wargaming process.

## Group Members

[Peter Asjes](mailto:m250228@usna.edu)

[William Robinson](mailto:m255334@usna.edu)

[Henry Frye](mailto:m251854@usna.edu)

[Caleb Koutrakos](mailto:m253300@usna.edu)

[Robert Ziman](mailto:m257074@usna.edu)

## POC

[LtCol Scotty Black](mailto:scotty.black@nps.edu )

## Installation

This project relies on several python packages. The easiest way to manage these is to create a Conda environment using the provided `.yml` files to create a Conda environment. If you are running the program on Windows or a *non* x86_64 system, you must use the `environment_cpu.yml` configuration. The GPU configuration requires a package that is only available on Linux x86_64 systems. If you are on a Linux x86_64 system with GPU support, you can use the `environment_gpu.yml` configuration. Either configuration will create a new Conda environment called **capstone_cpu** or **capstone_gpu**.

```bash
conda env create -f [environment_cpu.yml | environment_gpu.yml]
```

If you do not have Conda installed already, instructions can be found [here](https://docs.anaconda.com/miniconda/install/).

Once all of the necessary packages are installed and the environment is activated (`conda activate [capstone_gpu | capstone_cpu]`), the document generator script can be ran from the scripts directory.

```bash
cd scripts
python3 docGen.py
```

This project also requires that you have access to Meta's Llama 3.2 models via [Hugging Face](https://huggingface.co/). You must request access to the model before this project can be run. Follow these instructions to get access:

1. Visit the page for [Llama-3.2 (1B) on hugging face](https://huggingface.co/meta-llama/Llama-3.2-1B)
2. Create a free account and login.
3. Return to the Llama webpage (if not already there).
4. You should see a Community License Agreement at the top. Click the "Expand to review" button:
5. If you agree with the terms, fill out the form
6. Check email later.

Once you have received access to the models, visit your [tokens page](https://huggingface.co/settings/tokens) and click "Create new token". Choose the "Read" token type at the very top. Then click "Create token". Copy the generated string.

In the terminal, run the following command and paste in your access token when prompted:

`huggingface-cli login`

## Poster

![Capstone Poster](./proposal/USNA%20Capstone%20Posterv2.png)
