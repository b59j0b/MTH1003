java c
MTH1003 Mathematical Modelling
CW3: Group project on population dynamics:
Model of competition between species
Submission deadline: 12:00 noon on Thursday 20 March 2025 (week 10).
In this project you will use mathematics and numerical methods coded in Python to study the dynamics of a Lotka–Volterra model of competition between species. You will work in groups of five or six people, and each group will write a report, using LATEX, to be submitted in week 10. The report should describe the methods used and clearly illustrate the results using plots created in Python. This assignment is AI-prohibited.
1 Conservation
Consider the populations of two species of squirrel – let’s call them ‘reds’ and ‘greys’ – who inhabit the same ecosystem and compete for resources. Their respective populations are r(t) and g(t), in suitably scaled units.
To begin with, suppose the squirrel populations obey the Lotka–Volterra model

Find and classify the equilibrium points of this system.
Show that the quantity

is conserved for this system.
2 Numerical simulation and testing
Use a foward Euler time integration scheme to obtain the solution of (1) for t ∈ [0, 6] with initial condition (r(0), g(0)) = (0.5, 0.116). To start with, use a time step ∆t = 0.1. By substituting your numerical solution for r(t), g(t) into the expression for C(x, y), compute the quantity C(t) = C(r(t), g(t)) for this numerical solution. The quantity C(t) is constant mathematically, and you should discuss how well C is conserved in your numerical solution.
Repeat the calculation for smaller values of ∆t. What value of ∆t (let’s call it ∆t0) is needed to ensure that the relative change in C, i.e. |(C(t) − C(0))/C(0)|, is less than 0.001 at the final time t = 6?
For the two cases ∆t = 0.1 and ∆t = ∆t0, plot the trajectories (r(t), g(t)) in the (r, g)-plane. Also indicate on the plot the positions of the equilibrium points. Briefly discuss the implications of your results for numerically modelling the system (1).
Use ∆t ≤ ∆t0 for any numerical integration in the questions below.
3 Stable and unstable manifolds
One of the equilibrium points you found in section 1 should be a saddle. By using linear stability theory, determine the directions of the stable and unstable manifolds close to the saddle.
Use your forward Euler time stepping code to compute and plot an estimate of the unstable manifold by choosing suitable initial conditions close to the saddle. Discuss briefly whether this estimate agrees with the linear stability analysis.
By modifying your time stepping code to step backwards in time, or otherwise, compute and plot an estimate of the stable manifold of the saddle. Again, discuss briefly whether this estimate agrees with the linear stability analysis.
4 Nullclines and equilibria
Now consider the extended Lotka–Volterra model

with a = 2 and b = 3.
Plot the nullclines of this system, and hence find the equilibrium points. Also classify the equilibrium points.
5 Ecosystem management
Consider again the system (2). To begin with, a = 2 and b = 3, as in section 4. However, as a consequence of environmental changes, the parameter b is slowly decreasing. Discuss how the dynamics of the system changes as a result, and determine the critical value of the parameter b at which a stable equilibrium of co-existing reds and greys ceases to exist.
Ecosystem managers are able to alter conditions so as to change the value of the parameter a. How should they change a in order to offset the effects of the decrease in b, and what value of a should they choose in order that the system should have a stable equilibrium with roughly equal populations of reds and greys?
What would happen if the ecosystem managers changed a by too much?
Is there a point, as b decreases, beyond which the ecosystem managers are unable to save the ecosystem? What happens in that case?
Illustrate these various scenarios using suitable diagrams.
6 Red and grey squirrels in the real world
Do some background reading around the competition between red and grey squirrels in the real world. As a starting point, there are some excellent web sites aimed at the wider public [2,3]. For a deeper, more technical discussion you could look at [4,5,6], amongst others. Discuss briefly some of the factors that are thought to be important in the real world but have been omitted or simplified in the model (2) introduced above. Suggest ways in which the model (2) could be made more realistic for modelling the real world population dynamics; be specific about what mathematical terms one might include in the model and what they would represent, or you may even consider incorporating further differential equations.
Reports
Write up your project as a report using LATEX (no other medium is allowed). You will probably find the Overleaf online system a useful way to cooperate on the project report. A template is provided on ELE: you don’t have to use this, but you may find it helpful (for example it makes better use of space on the page than the LATEX default). You can drag the zipped template file on ELE into Overleaf and then you will have something to look at and potentially work with.
You must submit your report as a pdf file. Reports should be a maximum of 10 sides of A4 – this includes everything except an appendix of Python scripts, see below – with a font size no smaller than 11pt. Methods and results should be clearly and concisely explained, with appropriate equations and figures (and perhaps tables). All figures and tables should have a caption, and should be referred to (by their number) in the main text; LATEX’s built-in cross-referencing capability is very useful for this.
You should submit key Python scripts (i.e. if several scripts are minor variations of each other then there is no need to include more than one) in an appendix to your report; the appendix falls outside the 10-page limit. The template gives an example of a convenient way to include a Python script. in your report. Scripts should include a reasonable number of clear comments to aid understanding of how they work.
Your report should reference any sources you use in some standard style; for example see [1] below. All figures and plots presented should be your own unless they are clearly flagged as taken from a reference, for example by saying “ . . ., taken from [1]” in the caption. Any direct quotes from sources should be in quotation marks and clearly referenced.
You must not take Python or other code directly from other sources for the topics above, though you can of course study any such code and use it to inspire how you write your own. If you do find code from other sources helpful, then you s代 写MTH1003 Mathematical Modelling CW3Python
代做程序编程语言hould give a reference to those sources. You can however take any Python scripts or functions from the MTH1003 lecture notes and ELE page, and use and modify these without attribution.
Assessment and marking criteria
Marks will be awarded as follows:
• 90% Quality of report: including progress on the problem brief, mathematical accuracy, quality of discussion demonstrating good understanding, background information, quality of figures, overall layout, attractiveness and readability.
• 10% Evidence on the ELE Wiki showing the functioning of the group, including minuting key meetings, uploading and commenting on draft material, and assigning tasks, setting deadlines, and supporting each other within the group.
An overall mark will be given to each group based on the above breakdown. We will also require each student to give information on the contribution of other students within the group, and this will be used to determine individual marks from the group mark, which may be higher or lower than the group mark. The group ELE Wiki may be used to check on the contribution of students to the group effort. Any student who does not participate in their group, or shows very limited engagement, will gain a correspondingly low mark.
Group working
We will create new groups for CW3 that are distinct from those for CW2. The advice about working in groups for CW2 applies equally to CW3. So do divide up the tasks appropriately, and keep in touch with your group members and meet regularly to discuss progress. The advice from CW2 is reproduced here (with minor changes):
This module and its assessment are not just about learning new mathematics or applying it in new contexts; they are also about working together in a professional manner, managing and coordinating work within a group of five or six people from diverse backgrounds and abilities, and ensuring a fair division of work between you. For the group work in this project you will need to jointly contribute to preparation of a report. This should involve you doing some or all of the following:
• working together in a group on aspects of the problem,
• doing mathematical calculations,
• implementing numerical methods in Python,
• explaining what you have done clearly and concisely,
• helping others with support and constructive criticism (but do be tactful),
• drafting and/or editing sections, and preparing diagrams for the report.
We will provide each group with a Wiki on ELE which should be used to document the functioning of the group, and the contribution of individual students. You should use this medium to record notes of key meetings and who was present, tasks with deadlines as assigned within the group, the uploading of draft material (text, figures, codes, reports), and the commenting on and editing of draft material. The use of the Wiki is part of how we will assess your contribution to the project; see below.
Dividing up tasks
There are various ways of dividing up the work on this project among group members. There are interdependencies between the different parts, so those working on different parts will need to communicate and coordinate. In particular the early parts are easier than the later parts, particular part 5 on ecosystem management, and so we suggest that for the mathematical side you organise to share out the earlier parts amongst the group members first, and then when these are complete you share out the later parts,Another way is to think about the different types of tasks involved and to try to play to the strengths of the different group members: Who might be a good leader/coordinator/organiser? Who might be good at mathematical derivations? Who might be a good coder? Who might be good with LATEX? Who might be good at clear and concise communication and report layout?
We recommend you work in pairs (or threes) on different aspects of the project. Either way, it will be important to bring all of the pieces of the project together at the end into a coherent piece of work.
Although you’ll need to divide up tasks, it is every group member’s responsibility that the resulting report is as good as possible in terms of addressing the science and computing tasks and explaining the results to the reader in a manner that is attractive, clear, and ‘flows’.
Working as a group
All members of your group (including you) depend upon each other to engage in the required task and make a full contribution. So do what you say you will do to the best of your ability, and if you are ill or can’t attend a group meeting for any reason, then let members of your group know as soon as possible and arrange with them how to rectify the situation. It is a good idea to exchange email addresses and mobile numbers and/or use a social media group facility.
Don’t expect your group to countenance clear lack of effort or unreliability on your part. To encourage all group members to make a full contribution to the project, the mark awarded will depend in part on how your fellow group members rate your contribution. We will explain the mechanics of this rating system towards the end of the project.
Submission
Your report should be submitted as a pdf file via ELE. Only one report per group should be submitted, but please include on the front page of the report the student IDs of all the group members who contributed.
The deadline is 12:00 noon on Thursday 20th March 2025 (week 10).
Bibliography
[1] University of Exeter. LibGuides: An introduction to referencing. Retrieved January 20, 2022 from https://libguides.exeter.ac.uk/referencing/.
[2] Woodland Trust: Red Squirrel Facts. Retrieved November 25, 2022 from https://www.woodlandtrust.org.uk/blog/2018/11/red-squirrel-facts/
[3] Wildlife Trusts: Red squrrels. Retrieved November 25, 2022 from https://www.wildlifetrusts.org/saving-species/red-squirrels
[4] Gurnell, J., Wauters, L.A., Lurz, P.W.W., Tosi, G., 2004. Alien species and interspecific competition: Effects of introduced eastern grey squirrels on red squirrel population dynamics. J. Animal Ecology, 73, 26-35.
[5] Roberts, M.G., Heesterbeek, J.A.P., 2001. Infection dynamics in ecosystems: on the interac tion between red and grey squirrels, pox virus, pine martens and trees. J. Roy. Soc. Interface, 18, 20210551. https://doi.org/10.1098/rsif.2021.0551
[6] Twining, J.P., Lawton, C., White, A., Sheehy, E., Hobson, K., Montgomery, W.I., Lambin, X., 2022. Restoring vertibrate predator populations can provide landscape-scale biological control of established invasive vertebrates: Insights from pine marten recovery in Europe. Global Change Biology, 28, 5368–5384. DOI:10.1111/gcb.16236











         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
