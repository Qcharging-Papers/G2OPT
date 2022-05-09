[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)


# A G2OPT based charging strategy on Wireless Rechargeable Sensor Network


## About the Project 
 This Project is an implementation of a G2OPT based charging strategy running on a WRSN Simulator with multiple mobile chargers.

## Prerequisites:

- `pandas>=1.1.3`  
- `scipy>=1.5.2`    
- `numpy>=1.19.2`
- `scikit_learn>=0.24.2`

## Installation:
1. Clone the repo:
```bash
$ git clone https://github.com/Qcharging-Papers/G2OPT.git
```
2. Install Prerequisites:
```bash
$ pip install -r requirements.txt
```

## Usage:

1. Build Experiments:
- There are several built experiments in `./data`. However, new experiments can be built in the same format
```bash
data
├── MC.csv
├── cluster.csv
├── node.csv
├── package.csv
├── prob.csv
├── q_alpha.csv
├── q_gamma.csv
└── target.csv
```
2. Run:

```bash
python3 Simulate.py
```
- You can choose to `RESUME` unfinished experiments or to `START` new experiments
- Experiment type and index must be input

| Experiment_type      Experiment_index|    0    |    1    |    2    |    3     |    4   |
|--------------------------------------|---------|---------|---------|----------|--------|
| **node**                             |   700   |   800   | __900__ |   1000   |   1100 |
| **target**                           |   500   |   550   | __600__ |   650    |   700  |
| **MC**                               |   2     | __3__   |   4     |   5      |   6    |
| **prob**                             |   0.5   | __0.6__ |   0.7   |   0.8    |   0.9  |
| **package**                          | __500__ |   550   |   600   |   650    |   700  |
| **cluster**                          |   40    |   50    |   60    |   70     | __80__ |

- __Notes__: `Target` experiments must be *reconstructed* to match `node` experiments range if modified 


## License:
Distributed under the MIT License. See `LICENSE` for more information.
