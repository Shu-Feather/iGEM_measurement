# Dry Lab Measurements

Assignee: Hou Shuyang
Status: Not started

## Dry Lab Measurements:

### **Obtaining physical parameters from the trajectory analysis**

Molecular dynamics simulation of certain biomolecule (such as protein, UNA, etc.) can reveal its dynamic properties based on proper trajectory analyses.
First comes the diffusion constant mentioned in the model part. The mean square displacement (MSD) of the multi-atom system defined as below:

![image.gif](Dry%20Lab%20Measurements%20d36cae1df6f04ada9ef1087a623d512d/image.gif)

N : the number of the atoms;
< **·** > : the average of ensembles, while the notation i means the average among atoms and the notation t means the average over the period of time;
r ( t ) : the coordination of the atom i in time t;

Besides, it can be proved by considering the Brownian motion process that diffusion constant D is proportionate to the MSD:

![image.gif](Dry%20Lab%20Measurements%20d36cae1df6f04ada9ef1087a623d512d/image%201.gif)

d: the dimension of the space;

For normal cases, d = 3 is the proper value; while for the Brownian motion happening exactly on the surface of the liquid (such as the membrane protein floating over the lipid) d = 2 is the proper value.

For our trajectory analyses, firstly linear fitting process should be performed for the MSD vs. t curve in order to get the value of slope k, then approximately we argue that k / 6 is a plausible estimation of the diffusion constant D.

The process above takes advantage of MSD and produces the “tracing” diffusion constant D_tracer actually. Because by definition the tracing diffusion constant for single atom can be calculated through the auto-correlation function of velocity:

![image.gif](Dry%20Lab%20Measurements%20d36cae1df6f04ada9ef1087a623d512d/image%202.gif)

M: the mass of the atom

While the tracing diffusion constant of multi-atom system is exactly the average of each atoms based on the formula above.

For ionic system, according to the Nernst-Einstein relation we can calculate the diffusion constant D as follows:

![image.gif](Dry%20Lab%20Measurements%20d36cae1df6f04ada9ef1087a623d512d/image%203.gif)

σ ( 0 ): the ionic conductivity;
ρ: the Ionic molar density;
F: the Faraday constant;
z: the net charge of the molecule;

Moreover, the ionic conductivity can also be obtained from the auto-correlation function of current j ( t ) :

![image.gif](Dry%20Lab%20Measurements%20d36cae1df6f04ada9ef1087a623d512d/image%204.gif)

While the current j ( t ) can be easily calculated through the MD trajectory.

The root mean square deviation (RMSD) of the molecule through MD simulation defined as follows:

![image.gif](Dry%20Lab%20Measurements%20d36cae1df6f04ada9ef1087a623d512d/image%205.gif)

m : The mass of the atom i ;
X : The coordinate of the atom i in real-time structure ;
Y : The coordinate of the atom i in compared structure ;

The RMSD together with the gyration radius Rg enable to build up the Gibbs energy landscape during the folding process. Moreover, by further analyses, it can be exploited to build up the residue contact map (RCM) of the whole molecules such as follows (Figure 1, the example of RCM for TEVp trajectory analyses).

![ResiduContact.svg](Dry%20Lab%20Measurements%20d36cae1df6f04ada9ef1087a623d512d/ResiduContact.svg)

Figure 1: The residue contact map for the TEVp system based on the analyses of the RMSD value

### **Processing EMSA results to obtain binding parameters K**

For a typical EMSA result, we define the “blocked” to be the average grey value of the retention (stay in the well) or block (lay behind) band, and we define the “fled” to be the average grey value of the leading band. Furthermore, we define the binding ratio:

![image.gif](Dry%20Lab%20Measurements%20d36cae1df6f04ada9ef1087a623d512d/image%206.gif)

Then fitting the binding ratio versus the concentration of aptamer using double reciprocal plotting, while the slope of the fitting curve is equal to 1 / K.

Figure 2 shows the results for aptamer-15. As depicted, the sample points fit well in the middle of the hyperbola curve.

![1.svg](Dry%20Lab%20Measurements%20d36cae1df6f04ada9ef1087a623d512d/1.svg)

Figure 2: The double reciprocal plotting for the EMSA result of aptamer-15

Moreover, Figure 3 shows the results for aptamer-29, and Figure 4 shows the results for aptamer-40. 

![2.svg](Dry%20Lab%20Measurements%20d36cae1df6f04ada9ef1087a623d512d/2.svg)

Figure 3: The double reciprocal plotting for the EMSA result of aptamer-29

![3.svg](Dry%20Lab%20Measurements%20d36cae1df6f04ada9ef1087a623d512d/3.svg)

Figure 4: The double reciprocal plotting for the EMSA result of aptamer-40