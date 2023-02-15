# TextMaster

Current function:  
- Extract meta data of scientific literature from savedrecs files of Web of Science (`meta_wos.ipynb`).  
- Automated opinion extraction and classification for scientific literature in materials science and related fields (`demo.ipynb`).  
  
This is the source code of our proposed SSCNN system (demo version) of our Nature Nanotechnology submission "Opinion Mining by Deep Learning Methods for Maximizing Discoverability of Nanomaterials". We use `.ipynb` to show the running results directly (Click the `.ipynb` file and you will see running results of each cell. You can also set up environment in your local machine and try out our functions with your own data). We will develop a more packaged api version of this project later.

Thanks for your attention. 

## Set up
1. Make sure you have python3.8 and the pip module installed. We recommend using conda environments.  
2. After git clone this repository to local machine (if you don't have git, you can also create a folder in local machine and download the files), navigate to the root folder of this repository and run `pip install --ignore-installed -r requirements.txt`. Note: if any packages fail to be installed, you may need to install those packages manually by `pip install package_name`.  
3. Stay in the root folder, manually download the models and data [test_demo.zip](https://drive.google.com/file/d/1e0OCbzQ6GjN_yDYxNhy8ynRx2I16eaCU/view?usp=sharing) and unzipped. 

## Introduction of code file meta_wos.ipynb  
The analysis is based on savedrecs files from Web of Science. The running results shown in this file are based on 22752 perovskite related publications. To get your own savedrecs files, you can search papers on [Web of Science](https://www.webofscience.com/wos/woscc/basic-search) by keywords and the search results should be exported as plain text files.  

We provide following functions:  
- Extract meta data as a json file 
- Visualization of publishers, journal names, publishment by year, data types, categories

## Introduction of code file demo.ipynb
The demo of our opinion mining system is composed of two parts: 
- Reproduce the results of opinion extraction and classification models
- Run opinion mining on a tiny text sample 

The two models were trained on mixed-topic dataset (EoL, perovskite, ALD).  
CNN model for opinion extraction obtained 94.21% f1-score on test set and for each category: 
| Category | F1-score |
| :--------: | :---: |
|   non-opinion   | 95.05% |
|   opinion    | 93.03% |

CNN-Attention model for opinion classification obtained 91.58% f1-score on test set and for each category: 
| Category | F1-score |
| :--------: | :---: |
|   challenge   | 77.27% |
|   opportunity    | 94.83% |

If you want to try opinion mining on your own data, please replace the content in `data/text.txt`.

## Contact  
If you have any problems, please email: yuweiwan2-c@my.cityu.edu.hk 
