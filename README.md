# MolFlex
Download at [Releases](https://github.com/mikesha2/MolFlex/releases).

A simple Unity interface for [NeuralDock](https://doi.org/10.3389/fmolb.2022.867241).

Basic functionality. WASD movement, ZX for vertical movement, click and drag to turn camera.

1. Input PDB ID (e.g. 4fev) and click Load PDB
2. Enter SMILES for a small molecule, for example caffeine is: CN1C=NC2=C1C(=O)N(C(=O)N2C)C
3. Click outside of text box, and place the glowing orange sphere at a binding location.
4. Toggle Lock to keep the sphere in place.
5. Click Compute

# Unity packages
I use the [NCDK](kazuyaujihara.github.io/ncdk/) package to parse SMILES. Protein crystal structures are directly retrieved from the [RCSB Protein Data Bank](https://www.rcsb.org/). Proteins are rendered by the [Unity DOTS stack](https://unity.com/dots), and the neural network is run using [Unity ML-Agents](https://github.com/Unity-Technologies/ml-agents) with Barracuda. The neural network was designed and trained in TensorFlow 2 and exported to [ONNX format](https://github.com/onnx/tensorflow-onnx).


Note: Try not to click Compute too quickly. The Mac version is functional but more jittery than the Windows version. The neural network is a smaller version of the one found in our paper.

Please cite [NeuralDock](https://doi.org/10.3389/fmolb.2022.867241) if you find this useful!
`@article{Sha2022,
  doi = {10.3389/fmolb.2022.867241},
  url = {https://doi.org/10.3389/fmolb.2022.867241},
  year = {2022},
  month = mar,
  publisher = {Frontiers Media {SA}},
  volume = {9},
  author = {Congzhou M. Sha and Jian Wang and Nikolay V. Dokholyan},
  title = {{NeuralDock}: Rapid and Conformation-Agnostic Docking of Small Molecules},
  journal = {Frontiers in Molecular Biosciences}
}`
