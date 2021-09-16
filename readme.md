# eveindustrytools

eveindustrytools is a python module based on [evemarkettools](https://github.com/SustainedCruelty/evemarkettools) providing useful functions for doing industry in EvE Online.
This includes formulas for material efficiency, invention probabilities, input materials needed for manufacturing
and converting type ids. (see usage below) 

## Installation

Use the package manager [pip](https://pypi.org/project/eveindustrytools/) to install eveindustrytools.

```bash
pip install eveindustrytools
```

## Usage

```python
import eveindustrytools as eit
import evemarkettools as emt

emt.typeNameToID('Sabre') # returns 22456
eit.productToBP(22456) # returns 22457 (Sabre Blueprint)
eit.T2ItemToT1BPC(22456) # returns 16243 (Thrasher Blueprint)
eit.bpToProduct(16243) # returns  16242 (Thrasher)

eit.invention_probability(16243, rem = 5, science1 = 5, science2 = 5, decryptor = 1) # returns 0.4375
eit.me_formula(quantity = 10000, me = 5) # returns 9500
eit.me_formula(quantity = 10, me = 9) # returns 9
```
Check out this [colab-notebook](https://colab.research.google.com/drive/1WChiEPMLYVgRfsBJ9PHuHU673wa0sq-t?usp=sharing) to see what other functions the library provides and how to use them.
## License
[MIT](https://choosealicense.com/licenses/mit/)
