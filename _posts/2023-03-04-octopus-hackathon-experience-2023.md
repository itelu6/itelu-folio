---
layout: post
title: "My Experience at the OCTOPUS Hackathon"
date: 2023-03-04 00:00:00
description: a participant's experience at the OCTOPUS hackathon, highlighting the challenges, rewards, and networking opportunities involved
tags: hackathon coding-experience
categories: personal-experience
---

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/hackathon/hackathon-AI-picture.jpeg" class="img-fluid rounded z-depth-1 center" %}
    </div>
</div>
<div class="caption">
    An illustation of the hackathon event.
</div>

# Introduction 
The OCTOPUS hackathon occurs bi-annually and is primarily organized by the group leaders and senior researchers in Prof. Angel Rubio's group at the Max Planck Institute for the Structure and Dynamics of Matter (MPSD) in Hamburg, Germany.

Are you curious about what it's like to participate in a real-space time-dependent functional theory (RT-TDDFT) code hackathon? Join me as I recount my thrilling experience and learned lessons during the 5-day OCTOPUS hackathon (February 6th-10th, 2023), where we improved and added new features to the OCTOPUS code.

> 📘 More about OCTOPUS
>
> [OCTOPUS](https://www.octopus-code.org/documentation/12/) is a software package that utilizes time-dependent density functional theory to simulate electron dynamics in complex systems, including both extended and finite systems. It is written in Fortran and C++, and uses a real-space grid to solve the Khon-Sham and Maxwell equations. OCTOPUS is frequently updated and developed by a community of researchers, making it a widely used tool for exploring light-driven phenomena and quantum dynamics in molecules and materials.
> 
> Interested? Please refer to the latest article ["Octopus, a computational framework for exploring light-driven phenomena and quantum dynamics in extended and finite systems"](https://aip.scitation.org/doi/10.1063/1.5142502), N. Tancogne-Dejean et al., _The Journal of Chemical Physics_ 152 124119 (2020). 


# The Hackathon Experience

The hackathon is structured as follows: on the first day, participants learn about the main tasks and who is involved in each part. Over the next few days, participants give a brief update on what they accomplished the day before, and then spend the day working to solve any issues. If someone finishes his or her task, (s)he can request more tasks from the organizers. In addition, the hackathon provides free coffee, drinks, cookies, and dinner, which is my favorite part.

On the first day of the hackathon, one of the main organizers (Nicolas) provided a short overview of OCTOPUS and identified the main tasks and issues that needed to be resolved during the hackathon. Participants were then assigned a task, which could be changed with others if desired. These tasks were grouped and hosted by organizers with more experience in the code structure. 

I teamed up with a group leader (Hannes), an expert in solid-state materials with light-matter interactions. we swiftly narrowed our focus to three achievable projects for the 5-day hackathon: 1) implementing the Wannier interpolation method using the selected columns of the density matrix (SCDM) technique; 2) extending OCTOPUS' SCDM method for spinors (currently only for nonspinors); and 3) computing the spread of Wannier functions with the SCDM method over time propagation. After weighing the challenges and timeframes of each project, I decided to work on the second one.

Hannes recommended that I read [a 2018 paper on the SCDM method](https://arxiv.org/abs/1703.06958), as it was new to me. I spent Monday to Wednesday reading three papers on the topic - the 2018 SCDM paper, [the 2017 SCDM-k paper](https://doi.org/10.1021/ct500985f), and [the original 2015 SCDM paper](https://www.sciencedirect.com/science/article/pii/S0021999116307215) by the developers of the technique - and also studied the subroutines in OCTOPUS for the nonspinor version of the method implemented by Hannes. 

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/hackathon/reading-notes.png" class="img-fluid rounded z-depth-1 center" %}
    </div>
</div>
<div class="caption">
    my notes for reading the papers and the hilights for the main equations used in the SCDM method.
</div>


To avoid reinventing the wheel in code development, I explored the implementation of the SCDM-k method for spinors in Wannier90 (W90). I delved into the W90 subroutine to understand how the method is implemented and appreciated the detailed comments provided by its developers. As I read the papers, I sought to connect the mathematical formula to the code language used in W90. Finally, I considered how to implement the same equations in OCTOPUS, which has a different code structure than W90. Overall, it took me about two days from Tuesday afternoon to Thursday morning.  

With my background knowledge and the necessary components identified, I was ready to tackle one part of OCTOPUS (yeah, definitely create a new branch using git) and implement the SCDM-k method for spinors. I spent the last two days of the hackathon on implementing what I learned about the SCDM-k method for spinors. Surprisingly, the implementation process was not as complex as I initially anticipated. The most challenging part was understanding the programming jargon and deciphering the lines of code. In the end, I felt like a code archaeologist, excavating buried treasure and uncovering its secrets.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/hackathon/codes-snapshots.png" class="img-fluid rounded z-depth-1 center" %}
    </div>
</div>
<div class="caption">
    Implementing and translaing the main ideas of what I have learned about the SCDM-k method in W90
</div>


In general, I felt great about being able to complete some tasks quickly. One of these tasks was new to me, and I finished it within five days. Unfortunately, there are still some problems with the program that I need to fix, as it's causing segmentation faults. I plan to address these issues soon, possibly when I begin working on another research project that requires that feature.

# The learned lessons

> 🤖 [ChatGPT](https://chat.openai.com/chat) helped me rewrite and extend this section

Participating in this hackathon was a valuable learning experience for me. It gave me the opportunity to revisit and reflect upon the various stages involved in completing a code project. One of the most important stages is defining the problem statement and determining which questions or problems are worth pursuing given the time constraints. This requires a critical evaluation of the feasibility, impact, and significance of the research problem. It is essential to define clear research objectives and goals that guide the entire project.

The next stage involves finding related resources such as research papers, websites, lectures, codes, and other materials that provide valuable insights into the problem being addressed. It is essential to learn and master the key concepts and methods involved to ensure a strong foundation for the implementation stage. This stage requires a significant investment of time and effort in reviewing, organizing, and synthesizing the relevant information.

The implementation stage is where the rubber hits the road. It is the most challenging and time-consuming stage, where the actual coding and development of the project take place. This requires a comprehensive understanding of the problem and a strong grasp of the programming language and tools being used. Attention to detail, proper documentation, and adherence to best practices are crucial in this stage to ensure a robust and effective implementation.

Once the implementation stage is complete, testing the implementation is the final step. This stage ensures that the implementation works as intended and meets the research objectives and goals set out in the beginning. It involves identifying and addressing any bugs or issues and verifying that the implementation meets the necessary quality and performance standards. 

In conclusion, the hackathon experience reinforced the importance of these stages in completing a successful code project and the value of careful planning, research, implementation, and testing.

# What I would do differently next time 

From my experience with hackathons, there are typically two strategies that one can use. The first approach involves tackling a small and simple task that can be completed within a few hours, without the need for extensive research, before moving on to other categories or groups. For example, the OCTOPUS hackathon includes groups that focus on high performance, website design, fundamental code structure, data extraction, and output. This allows participants to work with a variety of experts specializing in fields such as DFT theory, numerical solvers, software performance, and maintenance. The second strategy involves defining a project based on a general direction, as I described earlier.

In the future, I plan to use the first strategy to work on several small, easy tasks and learn from others. Specifically, I would like to learn how to use shell commands, how the website is constructed, how a particular time propagation solver works, and how to use git more efficiently, among other things.