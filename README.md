
# The Trickster 

This is a project to create a text-based attack on an LLM.

## Project Description 
The project uses adversarial attacks to manipulate large language models (LLMs). Adversarial attacks are a type of attack that uses carefully crafted input to cause an LLM to generate unintended or malicious output. In the case of this project, the goal is to use adversarial attacks to cause an LLM to generate text that is harmful or offensive.

## Project Goals 

The goals of the project are to:
* Develop a new method for attacking LLMs.
* Test the new method on a variety of LLMs. 
* Analyze the results of the attacks. 

## Project Status 

The project is still under development. The new method has been developed, and it has been tested on a few different LLMs. The results of the attacks are still being analyzed.

## Project Requirements 
The project requires Python 3.8 or higher.

## Project Installation Instructions 

To install the project, clone the repository from GitHub.

This is just a basic example, and you may need to add more information depending on the specific project. For example, you may need to include more details about the adversarial attacks that are used, or you may need to provide more instructions on how to use the project.

I hope this helps!

## Attack Models

According to the level of perturbations imposed on original input, textual adversarial attack models can be categorized into sentence-level, word-level, character-level attack models. 

According to the accessibility to the victim model, textual adversarial attack models can be categorized into `gradient`-based, `score`-based, `decision`-based and `blind` attack models.

> [TAADPapers](https://github.com/thunlp/TAADpapers) is a paper list which summarizes almost all the papers concerning textual adversarial attack and defense. You can have a look at this list to find more attack models.

Currently The Trickster includes 15 typical attack models against text classification models that cover **all** attack types. 

Here is the list of currently involved attack models.

- Sentence-level
  - (SEA) **Semantically Equivalent Adversarial Rules for Debugging NLP Models**. *Marco Tulio Ribeiro, Sameer Singh, Carlos Guestrin*. ACL 2018. `decision` [[pdf](https://aclweb.org/anthology/P18-1079)] [[code](https://github.com/marcotcr/sears)]
  - (SCPN) **Adversarial Example Generation with Syntactically Controlled Paraphrase Networks**. *Mohit Iyyer, John Wieting, Kevin Gimpel, Luke Zettlemoyer*. NAACL-HLT 2018. `blind` [[pdf](https://www.aclweb.org/anthology/N18-1170)] [[code&data](https://github.com/miyyer/scpn)]
  - (GAN) **Generating Natural Adversarial Examples**. *Zhengli Zhao, Dheeru Dua, Sameer Singh*. ICLR 2018. `decision` [[pdf](https://arxiv.org/pdf/1710.11342.pdf)] [[code](https://github.com/zhengliz/natural-adversary)]
- Word-level
  - (TextFooler) **Is BERT Really Robust? A Strong Baseline for Natural Language Attack on Text Classification and Entailment**. *Di Jin, Zhijing Jin, Joey Tianyi Zhou, Peter Szolovits*. AAAI-20. `score` [[pdf](https://arxiv.org/pdf/1907.11932v4)] [[code](https://github.com/wqj111186/TextFooler)]
  - (PWWS) **Generating Natural Language Adversarial Examples through Probability Weighted Word Saliency**. *Shuhuai Ren, Yihe Deng, Kun He, Wanxiang Che*. ACL 2019. `score` [[pdf](https://www.aclweb.org/anthology/P19-1103.pdf)] [[code](https://github.com/JHL-HUST/PWWS/)]
  - (Genetic) **Generating Natural Language Adversarial Examples**. *Moustafa Alzantot, Yash Sharma, Ahmed Elgohary, Bo-Jhang Ho, Mani Srivastava, Kai-Wei Chang*. EMNLP 2018. `score` [[pdf](https://www.aclweb.org/anthology/D18-1316)] [[code](https://github.com/nesl/nlp_adversarial_examples)]
  - (SememePSO) **Word-level Textual Adversarial Attacking as Combinatorial Optimization**. *Yuan Zang, Fanchao Qi, Chenghao Yang, Zhiyuan Liu, Meng Zhang, Qun Liu and Maosong Sun*. ACL 2020. `score` [[pdf](https://www.aclweb.org/anthology/2020.acl-main.540.pdf)] [[code](https://github.com/thunlp/SememePSO-Attack)]
  - (BERT-ATTACK) **BERT-ATTACK: Adversarial Attack Against BERT Using BERT**. *Linyang Li, Ruotian Ma, Qipeng Guo, Xiangyang Xue, Xipeng Qiu*. EMNLP 2020. `score` [[pdf](https://www.aclweb.org/anthology/2020.emnlp-main.500.pdf)] [[code](https://github.com/LinyangLee/BERT-Attack)]
  - (BAE) **BAE: BERT-based Adversarial Examples for Text Classification**. *Siddhant Garg, Goutham Ramakrishnan. EMNLP 2020*. `score` [[pdf](https://www.aclweb.org/anthology/2020.emnlp-main.498.pdf)] [[code](https://github.com/QData/TextAttack/blob/master/textattack/attack_recipes/bae_garg_2019.py)]
  - (FD) **Crafting Adversarial Input Sequences For Recurrent Neural Networks**. *Nicolas Papernot, Patrick McDaniel, Ananthram Swami, Richard Harang*. MILCOM 2016. `gradient` [[pdf](https://arxiv.org/pdf/1604.08275.pdf)]
- Word/Char-level
  - (TextBugger) **TEXTBUGGER: Generating Adversarial Text Against Real-world Applications**. *Jinfeng Li, Shouling Ji, Tianyu Du, Bo Li, Ting Wang*. NDSS 2019. `gradient` `score` [[pdf](https://arxiv.org/pdf/1812.05271.pdf)]
  - (UAT) **Universal Adversarial Triggers for Attacking and Analyzing NLP.** *Eric Wallace, Shi Feng, Nikhil Kandpal, Matt Gardner, Sameer Singh*. EMNLP-IJCNLP 2019. `gradient` [[pdf](https://arxiv.org/pdf/1908.07125.pdf)] [[code](https://github.com/Eric-Wallace/universal-triggers)] [[website](http://www.ericswallace.com/triggers)]
  - (HotFlip) **HotFlip: White-Box Adversarial Examples for Text Classification**. *Javid Ebrahimi, Anyi Rao, Daniel Lowd, Dejing Dou*. ACL 2018. `gradient` [[pdf](https://www.aclweb.org/anthology/P18-2006)] [[code](https://github.com/AnyiRao/WordAdver)]
- Char-level
  - (VIPER) **Text Processing Like Humans Do: Visually Attacking and Shielding NLP Systems**. *Steffen Eger, Gözde Gül ¸Sahin, Andreas Rücklé, Ji-Ung Lee, Claudia Schulz, Mohsen Mesgar, Krishnkant Swarnkar, Edwin Simpson, Iryna Gurevych*. NAACL-HLT 2019. `score` [[pdf](https://www.aclweb.org/anthology/N19-1165)] [[code&data](https://github.com/UKPLab/naacl2019-like-humans-visual-attacks)]
  - (DeepWordBug) **Black-box Generation of Adversarial Text Sequences to Evade Deep Learning Classifiers**. *Ji Gao, Jack Lanchantin, Mary Lou Soffa, Yanjun Qi*. IEEE SPW 2018. `score` [[pdf](https://ieeexplore.ieee.org/document/8424632)] [[code](https://github.com/QData/deepWordBug)]

The following table illustrates the comparison of the attack models.

|    Model    |  Accessibility  | Perturbation | Main Idea                                           |
| :---------: | :-------------: | :----------: | :-------------------------------------------------- |
|     SEA     |    Decision     |   Sentence   | Rule-based paraphrasing                             |
|    SCPN     |      Blind      |   Sentence   | Paraphrasing                                        |
|     GAN     |    Decision     |   Sentence   | Text generation by encoder-decoder                  |
| TextFooler  |      Score      |     Word     | Greedy word substitution                            |
|    PWWS     |      Score      |     Word     | Greedy word substitution                            |
|   Genetic   |      Score      |     Word     | Genetic algorithm-based word substitution           |
|  SememePSO  |      Score      |     Word     | Particle Swarm Optimization-based word substitution |
|  BERT-ATTACK  |      Score      |     Word     | Greedy contextualized word substitution |
|  BAE  |      Score      |     Word     | Greedy contextualized word substitution and insertion |
|     FD      |    Gradient     |     Word     | Gradient-based word substitution                    |
| TextBugger  | Gradient, Score |  Word+Char   | Greedy word substitution and character manipulation |
|     UAT     |    Gradient     |  Word, Char  | Gradient-based word or character manipulation       |
|   HotFlip   |    Gradient     |  Word, Char  | Gradient-based word or character substitution       |
|    VIPER    |      Blind      |     Char     | Visually similar character substitution             |
| DeepWordBug |      Score      |     Char     | Greedy character manipulation                       |

## Toolkit Design

Considering the significant distinctions among different attack models, we leave considerable freedom for the skeleton design of attack models, and focus more on streamlining the general processing of adversarial attacking and the common components used in attack models.

The Trickster has 7 main modules: 

<img src="./docs/source/images/toolkit_framework.png" alt="toolkit_framework" style="zoom:40%;" />

* **TextProcessor**: processing the original text sequence to assist attack models in generating adversarial examples;
* **Victim**: wrapping victim models;
* **Attacker**: comprising various attack models;
* **AttackAssist**: packing different word/character substitution methods that are used in word-/character-level attack models and some other components used in sentence-level attack models like the paraphrasing model;
* **Metric**: providing several adversarial example quality metrics that can serve as either the constraints on the adversarial examples during attacking or evaluation metrics for evaluating adversarial attacks;
* **AttackEval**: evaluating textual adversarial attacks from attack effectiveness, adversarial example quality and attack efficiency;
* **DataManager**: managing all data and saved models that are used in other modules.

## Citation

Please cite our [paper](https://aclanthology.org/2021.acl-demo.43.pdf) if you use this toolkit:

```
@inproceedings{zeng2020The Trickster,
  title={{The Trickster: An open-source textual adversarial attack toolkit}},
  author={Zeng, Guoyang and Qi, Fanchao and Zhou, Qianrui and Zhang, Tingji and Hou, Bairu and Zang, Yuan and Liu, Zhiyuan and Sun, Maosong},
  booktitle={Proceedings of the 59th Annual Meeting of the Association for Computational Linguistics and the 11th International Joint Conference on Natural Language Processing: System Demonstrations},
  pages={363--371},
  year={2021},
  url={https://aclanthology.org/2021.acl-demo.43},
  doi={10.18653/v1/2021.acl-demo.43}
}
```

## Authors

- [@vishwanathakuthota](https://github.com/vishwachintu/)
    
