### Alignedlayer-Testnet-Proof
Aligned works with EigenLayer to leverage ethereum consensus mechanism for ZK proof verification. Working outside the EVM, this allows for cheap verification of any proving system. This enables the usage of cutting edge algorithms, that may use new techniques to prove even faster. 

### ALIGNEDLAYER PUBLIC PROOF TASK  
![image](https://github.com/Freemandaily/Alignedlayer-Testnet-Proof/blob/main/photo.png)

## Getting Started

```
sudo apt update -y
sudo apt upgrade -y
```

### Install Curl
```
sudo apt-get install curl -y
```
Consider logining as root user  in your vps,ubuntu,etc
  
### Dowload AlignedProof
![image](https://github.com/Freemandaily/Alignedlayer-Testnet-Proof/blob/main/aligne-1.png)

```
curl -L https://raw.githubusercontent.com/yetanotherco/aligned_layer/main/batcher/aligned/install_aligned.sh | bash
```
### Run This To Use Aligne downloaded
```
source /root/.bashrc
```
### Download an example SP1 proof file with it's ELF file 
![image](https://github.com/Freemandaily/Alignedlayer-Testnet-Proof/blob/main/aligne-2.png)

```
curl -L https://raw.githubusercontent.com/yetanotherco/aligned_layer/main/batcher/aligned/get_proof_test_files.sh | bash
```


### Sending proof 
![immage](https://github.com/Freemandaily/Alignedlayer-Testnet-Proof/blob/main/aligne-3.png)

```
rm -rf ~/aligned_verification_data/ &&
aligned submit \
--proving_system SP1 \
--proof ~/.aligned/test_files/sp1_fibonacci.proof \
--vm_program ~/.aligned/test_files/sp1_fibonacci-elf \
--aligned_verification_data_path ~/aligned_verification_data \
--conn wss://batcher.alignedlayer.com
```
There is an Explorer link in the those output , Use it to check if its verified. see below 

![image](https://github.com/Freemandaily/Alignedlayer-Testnet-Proof/blob/main/aligne5.png)

### Check verification on terminal
![image](https://github.com/Freemandaily/Alignedlayer-Testnet-Proof/blob/main/aligne4.png)

```
aligned verify-proof-onchain \
--aligned-verification-data ~/aligned_verification_data/*.json \
--rpc https://ethereum-holesky-rpc.publicnode.com \
--chain holesky
```
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Tweet as show in the  image below, using your Explorer link and photo of the verification
![image](https://github.com/Freemandaily/Alignedlayer-Testnet-Proof/blob/main/tweet.png)

--------------------------------------

#### Join Their Discord From Their Profile
https://linktr.ee/AlignedLayer

### Submit tweet URL on Discord

![image](https://github.com/Freemandaily/Alignedlayer-Testnet-Proof/blob/main/alogne-testnet.png)



