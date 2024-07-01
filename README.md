# Watermarking-DNN


White Box Watermark Methodology

## Table of Contents

- [Prerequisites](#Prerequisites)
- [Usage](#usage)
- [Algorithm](#Algorithm)
- [Notes](#Notes)
- [License](#license)
- [Contact](#contact)


### Prerequisites

- Google colab
- python 3.10.12


### Usage

To protect the ownership of the model


###Algorithm

## White Box Watermark Methodology


1. Train baseline task for N iterations and profile the parameter distribution (M1)

2. Train baseline+OOD input for more k iteration and profile parameter distribution (M2)

3. measure the perturbation by M2-M1

4. Quantize the perturbation (i.e., M2-M1 >= β then set 1 or M2-M1 >= -β then set -1) and store it in watermark_keys array W

5. Find out the best β by ablation study

6. Finally, match the extracted keys with W

## Notes


1. WaterMark is a combination of  {-1, 1 } in each layer

2. Generate the Watermark keys using β, M1 and M2 

3. Deploy the model M2 

4. Prove the ownership using β, M1 and M2

(Note that the attacker does not have access to β and M1 but only M2)


### License

This project is licensed under the [MIT License](https://github.com/Mamun5011/watermarking-DNN/blob/main/LICENSE).


### Contact

For any questions or concerns, contact mmamu003@ucr.edu
