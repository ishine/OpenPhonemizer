# OpenPhonemizer

A permissively licensed, open sourced, local IPA Phonemizer (G2P) powered by deep learning. This Phonemizer attempts to replicate the `espeak` Phonemizer while remaining permissively-licensed.

## Project

* Project status: Alpha
* Supported languages: English (more coming soon!)

## Installation


```bash
pip install "openphonemizer @ git+https://github.com/NeuralVox/OpenPhonemizer"
```

## Usage

### OpenPhonemizer

```python
from openphonemizer import OpenPhonemizer
phonemizer = OpenPhonemizer()
# Or specify a custom checkpoint path: OpenPhonemizer('model.pt')
phonemizer('test')
phonemizer('hello this is a test')
```

## Evaluation

We introduce PhonemizerBench, a benchmark to evaluate the similarity of alternate Phonemizers to `espeak`.

**Run 1**

| Phonemizer | Score |
| --- | --- |
| Gruut | 75.08 |
| Deep Phonemizer | 85.24 |

**Run 2**

| Phonemizer | Score |
| --- | --- |
| Gruut | 75.54 |
| Deep Phonemizer | 85.03 |

**Run 3**

| Phonemizer | Score |
| --- | --- |
| Gruut | 73.72 |
| Deep Phonemizer | 84.64 |

## License

OpenPhonemizer is open source software. You may use it under the BSD-3-Clause Clear license found in the LICENSE file.

**Please note** that certain tools provided with OpenPhonemizer are licensed under the GNU General Public License, version 3.0, as certain parts of OpenPhonemizer rely on the `phonemizer` library. These components have been isolated and are not linked by the rest of the software. Unless otherwise specified in a README file, all other components of OpenPhonemizer are licensed under the BSD-3-Clause Clear license.

*By contributing to this repository, you grant the author the permission to change the license in the future at their sole discretion.*

**NOTE:** Model weights may be licensed under different licenses. Please make sure to check all model weights for licenses.

## Credits

OpenPhonemizer is heavily based on [Deep Phonemizer](https://github.com/as-ideas/DeepPhonemizer). Special thanks to [Christian Schäfer](https://github.com/cschaefer26), who created Deep Phonemizer.