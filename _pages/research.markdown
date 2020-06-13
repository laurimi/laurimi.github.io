---
title: Research
permalink: /research/
classes: single
toc: true
toc_label: "Research areas"
toc_icon: "file-alt"
mathjax: true
---

My research focuses on sequential decision-making under uncertainty, active perception, and deep learning for robot vision.
These focus areas along with key references are described below.
For a full list of my research works, you can see [my complete publication list](/publications).

# Sequential decision-making under uncertainty
<figure class="half">
    <a href="/assets/images/research/pomdp.png"><img src="/assets/images/research/pomdp.png"></a>
    <a href="/assets/images/research/decpomdp.png"><img src="/assets/images/research/decpomdp.png"></a>
    <figcaption>Left: Single-agent decision-making. Right: Multi-agent decision-making.</figcaption>
</figure>

Sequential decision-making under uncertainty involves a single agent or a team of agents.
Each agent takes an action $$ a $$, and then perceives an observation $$ z $$ that reveals something about the underlying hidden state $$ s $$ of the system.
When actions are taken, the hidden state undergoes a stochastic state transition.
The observations are also noisy, and provide only partial knowledge about the state.
A *control policy* $$ \pi $$ instructs an agent how it should select its next action given the past actions and observations.
The objective is to find a control policy for each agent that maximizes a utility over a horizon of multiple decisions.
This problem may be formalized as a partially observable Markov decision process (POMDP) in the single agent case, and as a decentralized POMDP (Dec-POMDP) in the multi-agent case.

In particular, I am interested in tasks involving *active information gathering*, where the objective is to maximize the amount of information about the hidden state.
The amount of information can be quantified by using information-theoretic quantities such as entropy or mutual information on the *belief state* $$ b $$, which is a probability distribution over the hidden state.
I have developed theory and algorithms for multi-agent active information gathering in Dec-POMDPs {% cite Lauri_JAAMAS2020 Lauri_AAMAS2019 %} and applied the same methodology to multi-robot target tracking {% cite Lauri_ICRA2017 %}.
I also formulated robotic exploration as a POMDP and applied it to a real robot exploring an unknown environment {% cite Lauri_RAS2016 %}.

# Active perception
<figure class="third">
	<a href="/assets/images/research/subtasks.png"><img src="/assets/images/research/subtasks.png"></a>
	<a href="/assets/images/research/online_scene1.png"><img src="/assets/images/research/online_scene1.png"></a>
	<a href="/assets/images/research/exploration.png"><img src="/assets/images/research/exploration.png"></a>
	<figcaption>Left: Active visual object search. Middle: Scene reconstruction using multiple cameras (Image courtesy of Joni Pajarinen). Right: Robotic exploration.</figcaption>
</figure>

An agent capable of observing the world around it can select when, where, and how to use its sensors to obtain more information about its environment or to explore it.
This process of planning how to use perception resources is known as active perception.

I am especially interested in applications of active perception in mobile robotics.
In our research work on active perception, we have applied deep reinforcement learning to help a robot locate a target object by searching in different types of apartments {% cite Schmid_IROS2019 %}, and greedy submodular maximization to find next-best-views for scene reconstruction using multiple cameras {% cite Lauri_WIPPAS2019a %}.

We used simulation-based planning to find trajectories for environment exploration {% cite Lauri_RAS2016 %}, and found it to outperform classical frontier exploration techniques in certain environments.
The video below summarizes this work.
{% include video id="-7c_RaZ-KTU" provider="youtube" %}

# Robot vision
<figure class="half">
    <a href="/assets/images/research/cloudpose.png"><img src="/assets/images/research/cloudpose.png"></a>
    <a href="/assets/images/research/ssv.png"><img src="/assets/images/research/ssv.png"></a>
    <figcaption>Left: Object pose estimation. Right: Attention-based RGBD segmentation. Images courtesy of Ge Gao.</figcaption>
</figure>
Robots equipped with cameras face a variety of challenging conditions that affect their visual perception.
Adverse environmental conditions in uncontrolled environments affect the quality of captured images.
Unconventional viewpoints, high spatio-temporal dependency between captured images, and the opportunity for interaction with the environment also distinguish robotic vision from conventional computer vision applications.

I am interested in the active perception and interaction aspects of robotic vision, using multiple sensing modalities such as RGB and depth perception, and the role of uncertainty in robot vision.
We have developed a deep learning method for estimation of object poses from point cloud data {% cite Gao_ICRA2020 %}, attention-based segmentation of RGBD data {% cite Gao_IROS2017 %}, and a segmentation method for object discovery applying non-parametric Bayesian techniques for uncertainty quantification {% cite Lauri_SCIA2017 %}.

# References
{% bibliography --cited %}