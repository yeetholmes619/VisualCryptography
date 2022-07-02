# Background
**Cryptography** is the study of secure communication techniques that only allow the sender and the recipient to view its contents. The term is derived from the greek word *kryptos*, which means hidden.

**Visual Cryptography** is a cryptographic technique where **images are distributed as shares**, and the **recovery of the final image** can be done using the **human visual system**, usually by having the shares be printed on transparencies and having them stacked on top of other.

The detailed report of the same can be found [here](DESIGNCREDITREPORT_B20CS006_B20CS074.pdf)
# Our Work
## Basic Visual Cryptography

We first implemented the original black and white Basic Visual Cryptography Scheme made by Moni Naor and Adi Shamir based on this [paper](https://link.springer.com/content/pdf/10.1007/BFb0053419.pdf)

The scheme involves a (n,k) secret sharing scheme, where the image is divided into n shares, such that any k-1 shares or fewer when stacked on top of each other must be unable to view the image. And any k or more images when stacked on each other should be able to view the image completely.

<img src="https://drive.google.com/uc?export=view&id=1vPAGHGvE3-lA4z4QC69thX6Np8VM0hDY" height="300" width = "500">  <img src="https://drive.google.com/uc?export=view&id=1BCYsCDPmuEUL4q6JbnvEGbAoSQMYauhH" height="300" width = "500">

## Visual Cryptography With Colored Images

### Method 1

The first method we employed had the following scheme. two-level security controlling practice.For example, as long as a manager of a company keeps the black mask of a secret image and gives the rest three shares to his subordinates, the content of the image will remain confidential, even though all his subordinates plot to steal the secret information. Thus, under these circumstances, the black mask share can be regarded as the signature of the manager.

<img src ="https://drive.google.com/uc?export=view&id=1fRKaYhrDPy3ILmAnqAWOum-Sgs15KDKx" height="300" width = "500">  <img src ="https://drive.google.com/uc?export=view&id=1BA01PHN9Kb0WGkPRAd-ttlrRf3IrbHu8" height="300" width ="500">
<p align = "center">
<img src="https://drive.google.com/uc?export=view&id=17PbLbWg_Envo3ONR9Ow9o0XQ90CdB1Ir" width = "500">
</p>

### Method 2
In this method we will create two seemingly similar looking shares unlike the previous method where four shares were created each representing four components of CMYK color scheme. This is similar to standard OTP scheme of cryptography.

The setting is as follows - We have a secret image and we want to create two shares out of it. Each share doesn't reveal any information about the image. Only when both shares are stacked together, the secret image is revealed. 

<img src="https://drive.google.com/uc?export=view&id=1hyAlmFHDjs8KNmXrwUo__edxNFyMoxCK" width="500" height="300"> <img src="https://drive.google.com/uc?export=view&id=1jPVnvxQ5NNjccK_Q-0W1cwnzG6UVwnkJ" width="500" height="300">

<img src="https://drive.google.com/uc?export=view&id=1hPzDVWfB_bpiHzBVpUronKteXoeF7BAf" width="500" height="300"> <img src="https://drive.google.com/uc?export=view&id=1062RVByoKsPGngUtkv7MYfwyQ5uVuoc6" width="500" height="300">


## Sidenotes
There are shortcomings to these algorithms. One being that if you want to more shares, your image size would increase quadratically. Hence handling images of sizes like this would not be practical.

Hence solving this problem, would perhaps one day encourage us to use visual cryptography, as its unique feature of not requiring computation for recovery opens up new possibilities.


## References
1. [https://fardapaper.ir/mohavaha/uploads/2018/12/Fardapaper-A-Comprehensive-Study-of-Visual-Cryptography.pdf](https://fardapaper.ir/mohavaha/uploads/2018/12/Fardapaper-A-Comprehensive-Study-of-Visual-Cryptography.pdf)
2. [https://link.springer.com/content/pdf/10.1007/BFb0053419.pdf](https://link.springer.com/content/pdf/10.1007/BFb0053419.pdf)
3. [https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.457.5077&rep=rep1&type=pdf](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.457.5077&rep=rep1&type=pdf)
4. [https://stackoverflow.com](https://stackoverflow.com)
5. [https://pillow.readthedocs.io](https://pillow.readthedocs.io)
6. [https://www.sciencedirect.com/science/article/abs/pii/S0031320302002583](https://www.sciencedirect.com/science/article/abs/pii/S0031320302002583)
