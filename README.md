# Cyber Alliance Game

## Brief summary


This Python script models a two-player game using game theory principles and visualizes the outcomes on a probabilistic grid. It utilizes three primary libraries: **NumPy** for handling large arrays and matrix computations,** Nashpy** for calculating Nash equilibria, and **Pillow** for creating and manipulating visual representations of the results.

- **NumPy**: https://numpy.org/doc/stable/

- **Nashpy**: https://nashpy.readthedocs.io/en/stable/

- **Pilow**: https://pypi.org/project/pillow/

The program begins by defining a 500×500 matrix (my_array) to store the strategic profiles derived from Nash equilibrium calculations. It sets parameters such as rewards (r1, r2), biases (b1, b2), and effectiveness coefficients (e1, e2) to influence the payoff equations for different strategies. Probabilities p and q, representing the likelihood of specific strategic choices by each player, are iteratively calculated within nested loops that span all possible values from 0 to 1 in increments of 0.002 (1/500).

For each combination of p and q, the script constructs payoff matrices for both players. These matrices encapsulate the rewards associated with various strategic outcomes, parameterized by the input coefficients. Using Nashpy, the script defines a game instance for the current payoff matrices and calculates Nash equilibria with the support enumeration method. Each equilibrium provides probabilities for the players' strategies (S1, A1, S2, A2), which are compared to categorize the equilibrium into one of several strategic profiles. These profiles are labeled as 'X', 'Y', 'Z', 'W', or 'D', each corresponding to a specific combination of pure or mixed strategies.

The results of these calculations are stored in the matrix my_array. A color mapping is applied to link each strategic profile to a unique color: blue for 'X', red for 'Y', green for 'Z', yellow for 'W', and orange for 'D'. Using the Pillow library, a blank 500×500 image is created, and the matrix values are translated into pixel colors to generate a visual representation of the strategic landscape.

Finally, the image is saved as output.png and displayed. This visualization provides an intuitive way to understand the distribution of strategic profiles across the probability space, offering insights into the dynamics of the game under study. By blending mathematical rigor with visual clarity, this script serves as a powerful tool for exploring and illustrating game theory concepts.

The Cyber Alliance Game: How Alliances Influence Cyber-Warfare: https://arxiv.org/abs/2410.05953


