<div align="center">
<h2 align="center">
   <b>Less is More: Empowering GUI Agent with Context-Aware Simplification
   <br /> <font size=3>ICCV 2025 </font></b> 
</h2>
<div>
<a target="_blank" href="https://scholar.google.com/citations?user=Mpg0w3cAAAAJ&hl=en&oi=ao">Gongwei&#160;Chen</a><sup>1</sup>,
<a target="_blank">Xurui&#160;Zhou</a><sup>1</sup>,
<a target="_blank" href="https://scholar.google.com/citations?user=9Vc--XsAAAAJ&hl=en&oi=ao">Rui&#160;Shao</a><sup>1&#9993</sup>,
<a target="_blank">Yibo&#160;Lyu</a><sup>1</sup>,
<a target="_blank" href="https://jnhujnhu.github.io/">Kaiwen&#160;Zhou</a><sup>1</sup>,
<br>
<a target="_blank" >WenTao&#160;Li</a><sup>2</sup>,
<a target="_blank" href="https://yinchuanll.github.io/">Yinchuan&#160;Li</a><sup>2</sup>,
 <a target="_blank" href="https://scholar.google.com/citations?hl=en&user=yywVMhUAAAAJ">Zhongang&#160;Qi</a><sup>2&#9993</sup>,
 <a target="_blank" href="https://scholar.google.com/citations?hl=en&user=yywVMhUAAAAJ">Liqiang&#160;Nie</a><sup>1&#9993</sup>
</div>
<sup>1</sup>Harbin Institute of Technology, Shenzhen&#160&#160&#160</span>
<sup>2</sup>Huawei Noah’s Ark Lab</span>
<br />
<sup>&#9993&#160;</sup>Corresponding author&#160;&#160;</span>
<br/>
<div align="center">
    <a href="https://arxiv.org/abs/2408.03615" target="_blank">
    <img src="https://img.shields.io/badge/Paper-arXiv-deepgreen" alt="Paper arXiv"></a>
    <a href="https://cybertronagent.github.io/Optimus-1.github.io/" target="_blank">
    <img src="https://img.shields.io/badge/Project-Optimus--1-9cf" alt="Project Page"></a>
</div>
</div>

Xurui Zhou, Rui Shao, Yibo Lyu, Kaiwen Zhou, Shuai Wang, WenTao Li, Yinchuan Li, Zhongang Qi, Liqiang Nie


## :new: Updates
- [06/2025] :fire: We release the code. Enjoy it!
- [06/2025] :fire: SimpAgent is accepted to **ICCV 2025**!


## Install Dependencies
```shell
pip install -r requirement.txt
```

## How to run
```shell
bash scripts/finetune_lora.sh
```

## :balloon: SimpAgent Framework
We divide the structure of Optimus-1 into Knowledge-Guided Planner, Experience-Driven Reflector, and Action Controller. In a given game environment with a long-horizon task, the Knowledge-Guided Planner senses the environment, retrieves knowledge from HDKG, and decomposes the task into executable sub-goals. The action controller then sequentially executes these sub-goals. During execution, the Experience-Driven Reflector is activated periodically, leveraging historical experience from AMEP to assess whether Optimus-1 can complete the current sub-goal. If not, it instructs the Knowledge-Guided Planner to revise its plan. Through iterative interaction with the environment,Optimus-1 ultimately completes the task.
<img src="./assets/fig2.png" >

## :smile_cat: Evaluation results
We report the `average success rate (SR)`, `average number of steps (AS)`, and `average time (AT)` on each task group, the results of each task can be found in the Appendix experiment. Lower AS and AT metrics mean that the agent is more efficient at completing the task, while $∞$ indicates that the agent is unable to complete the task. Overall represents the average result on the five groups of Iron, Gold, Diamond, Redstone, and Armor.
<img src="./assets/table1.png" >

## Acknowledgement
- We built our code based on: [Qwen2-VL-Finetuning](https://github.com/2U1/Qwen2-VL-Finetune). Thanks 2U1!








