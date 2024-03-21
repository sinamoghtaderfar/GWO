1. Intro
In this article, we’ll review the Grey Wolf Optimization (GWO) algorithm and how it works. As we can conclude from the name, this is a nature-inspired metaheuristic that is based on the behavior of a pack of wolves. Similar to other nature-inspired metaheuristics such as genetic algorithm and firefly algorithm, it explores the search space in hope of finding an optimal solution.

In summary, this is an iterative method that is used for optimization problems.

2. Inspiration
The inspiration for this algorithm is the behavior of the grey wolf, which hunts large prey in packs and relies on cooperation among individual wolves. There are two interesting aspects of this behavior:
<ul>
	<li>social hierarchy</li>
  <li>hunting mechanism</li>
</ul>

<strong style="color:red;">The grey wolf is a highly social animal with the result that it has a complex social hierarchy.</strong> This hierarchical system, where wolves are ranked according to strength and power, is called “dominance hierarchies”. Therefore, there are the alphas, betas, deltas, and omegas.
<ol>
  <li>
     The alpha male and females are at the top of the hierarchy, and they lead the pack. All members of the pack have ordered within a specific rank. The wolf’s hierarchical system is        not just about dominance and aggression; it also provides assistance to vulnerable members of the pack who cannot hunt for themselves.
  </li>
<li>
  Afterward is the beta wolf that supports the alpha wolf’s decisions and helps keep discipline within the pack.
</li>
  <li>
    The delta wolf is below the beta wolf in rank. They are often strong but lack leadership skills or confidence in themselves to take on leadership responsibilities.
    And last, the omega wolf does not have any power at all and other wolves will quickly chase him. Omega wolf is also responsible for watching over younger wolves.
  </li>
</ol>

![hierarchy-768x547](https://github.com/sinamoghtaderfar/GWO-/assets/72755430/40f86e15-eb9f-4480-b03d-dc19f01b8ffa)

Besides social hierarchy, grey wolves have a very specific way of hunting with a unique strategy. They hunt in packs and work together in groups to separate the prey from the herd, then one or two wolves will chase after and attack the prey while the others chase off any stragglers.

Muro et al. describe the hunting strategy of the wolf pack and it includes:
<ul>
  <li>
approach, track and chase the prey
  </li>
<li>
pursuit, harass, and encircling maneuver around the prey until it stops moving
</li>
  <li>
    attack the prey when it is exhausted
  </li>
</ul>
3. Definition
Applying the previously described methodology to our optimization problem, at each step, we’ll denote respectively the three best solutions by alpha, beta, and delta, and other solutions by omega. Basically, it means the optimization process goes with the flow of the three best solutions. Also, the prey will be the optimal solution of the optimization.

Most of the logic follows the equations:

3. Definition
Applying the previously described methodology to our optimization problem, at each step, we’ll denote respectively the three best solutions by alpha, beta, and delta, and other solutions by omega. Basically, it means the optimization process goes with the flow of the three best solutions. Also, the prey will be the optimal solution of the optimization.

Most of the logic follows the equations:
https://www.baeldung.com/cs/grey-wolf-optimization

4. Example
In order to better understand this algorithm, we’ll present one concrete example of the wolf pack behavior. In the image below (left), we can see the initial state of the agents, where prey or optimal solution has a red color. The closest wolves to the prey (alpha, beta, and delta) have a green, blue, and purple color respectively. Black dots represent other wolves (omegas).

Further, if we update the position of omega wolves according to the formulas explained in the previous section, we can observe the behavior of agents in the image below (right). Notice that the variable a that controls the trade-off between exploration and exploitation is set to the value 2. This means that we prefer exploration overexploitation:

![image](https://github.com/sinamoghtaderfar/GWO-/assets/72755430/e6b3e7fa-11a2-4170-8dc7-389f019c7893)

Finally, in the image below, the variable a is equal to 0. It means that the optimization process is at the end and we’re hopefully converging towards the optimal solution following the best three wolves. We can see how omega wolves are gathering between the best three wolves, around the point that geometrically represents centroid between alpha, beta, and delta agents:

![gwo_gif2](https://github.com/sinamoghtaderfar/GWO-/assets/72755430/0cb9cecd-787d-4f70-b180-655df87305ae)



