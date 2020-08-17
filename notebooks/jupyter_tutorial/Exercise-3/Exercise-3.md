# Exercises 3


## Astropy units


- Create a function to evaluate the Planck function for wavelength, $B_\lambda(T)$, using `astropy.constants`:

\begin{equation}
B_\lambda(T)= \frac{2hc^2}{\lambda^5}\frac{1}{\mathrm{e}^{hc/\lambda k_b T} - 1}
\end{equation}

- Make a plot of $B_\lambda$ for T=2000 K and wavelengths between $0 < \lambda < 1500$ nm. Evaluate the function for $\lambda = 1$ cm. Use $k_b$ in CGS and note any differences.

- (**PAIR PROGRAMMING**) Write the function so that it takes any number of temperatures and any number of wavelengths, *without using loops*. 

- Consider an atom with three levels. The level energies in wavenumber (in cm$^{-1}$) are: `[0.0, 82258.211, 97491.219]`. Calculate the wavelengths (in nm) of the transition from the ground state to the first excited state, and from the first to the second excited state. What are the level energies in eV and aJ?

- (**PAIR PROGRAMMING**) The level energies and statistical weights of hydrogen are given by the following:

\begin{align} \tag{4}
g_{1,s} &= 2s^2 \\ \tag{5}
\chi_{1, s} &= 13.598 (1- 1/s^2)\; \mathrm{eV}
\end{align}

- Use them to create a text file with a model hydrogen atom, with $s$ up to 100. Each line should be for one value of $s$ (starting at 1), and have: $\chi$ (in cm$^{-1}$), $g$, and 0 (ionisation stage).