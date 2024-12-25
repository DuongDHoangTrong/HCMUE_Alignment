# Simulating Molecular Nonadiabatic Alignment

## Overview
This repository provides source code for simulating molecular nonadiabatic alignment. The program numerically solves the time-dependent Schrödinger equation (TDSE) to calculate the temporal evolution of a molecular rotational wave packet. It supports simulations for both polar and nonpolar linear molecules, offering versatility and reliability in studying laser-matter interactions.

## Features
- Simulates the alignment process for both polar and nonpolar molecules.
- Handles user-defined molecular parameters.
- Verified against reliable theoretical studies.

## Methodology
The simulation involves:
1. **Laser Field Interaction**: The molecular wave packet evolves under the influence of a linearly polarized laser field, modeled using a Gaussian pulse envelope.
2. **Field-Free Evolution**: After the laser pulse ends, the wave packet propagates in the absence of a field, allowing for the calculation of molecular alignment over time.

## Dependencies
- Python 3.x
- NumPy
- SciPy
- Pandas
- Matplotlib


## Usage
1. Modify `input.json` to define custom molecular parameters or laser settings.
  *`"laser"`: define laser parameters
    -`"intensity"`: laser intensity ($10^{13}$ W/cm$^2$);
    -`"fwhm"`: 'full width height max' of laser duration (fs);
    -`"step"`: number of steps for laser duration
  },

  "molecules": {
    "name": "OCS",
    "B": 0.2029,
    "delta_alpha": 4.04,
    "jMax": 60,
    "mMax": 50,
    "deg": 91,
    "g_even": 1,
    "g_odd": 1
  },

  "temperature": 100,
  "t_start": 0,
  "t_end": 150000,
  "t_step": 500
}
```   
2. Run `hcmue_alignment.exe`


## Results
The simulation outputs include:
- `degree_of_alignment.csv` data of $\langle \cos^2 \theta \rangle(t)$ as a function of time.
- `degree_of_alignment.png` figure of $\langle \cos^2 \theta \rangle(t)$ as a function of time.
- `distribution.png` distribution of $J_{max}$ states.


## Acknowledgments
- Author: Bui Van Nguyen
- Corresponding Author: Hoang Trong Dai Duong (hoangtrongdaiduong00@gmail.com)
- Supervisor: Phan Thi Ngoc Loan

## Contact
For any inquiries or issues, please contact the corresponding author at hoangtrongdaiduong00@gmail.com.

