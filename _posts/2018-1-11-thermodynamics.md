---
layout: post
title: Gerneral Thermodynamics
tags: physics

---

The article is a review note of the 1st year physics study in thermodynamics.

# REVIEW NOTES

- Temperature

  - The Zeroth Law of  Thermodynamics

    If bodies A and B are each in thermal equilibrium with a third body T, then A and B are in thermal equilibrium with each other.

    With the 0th law, temperature can be defined. \\(\longrightarrow\\) A and B are in thermal equilibrium if A and B are at the same temperature.

  - Triple Point of Water

    Under which liquid water, solid ices and water vapor can coexist. Only one choise of pressure and temperature can do that. This temperature, then, is called the **Triple Point of Water**.
    \\[
    T_{tp}=273.16K
    \\]

  - The Celsius and Fahrenheit Scales

    \\(T_C=T-273.15^\circ, T_F=\frac{9}{5}T_C+32^\circ\\)

- Thermal Expansion

  - Linear Expansion

    \\(\Delta L=L\alpha\Delta T\\), where \\(L\\) is the former length, \\(\alpha\\) is a constant and \\(\Delta T\\) is the change of temperature.

  - Volume Expansion

    \\(\Delta V=V\beta \Delta T=3V\alpha\Delta T,\beta=3\alpha\\)(Because \\(\Delta L\\) is very small.)


- Heat

  For solids and liquids: ( No phase transformation )

  - Heat Capacity

    Measuring the ability of an object to store heat. (Related to mass)

    \\(Q=C\Delta T\\)

  - Specific Heat

    \\(Q=cm\Delta T\\)

    \\(c\\) is the specific heat, which is only determined by the tpye of the material.

  Heat of Transformation

  - Melting or Vaporizing

    \\(Q=Lm\\), \\(L\\) is a constant determined by the transformation and \\(m\\) is mass.

- Work

  The work done **by the gas**:

  \\(W=\int_i^f dW=\int_i^f\vec{F}\cdot d\vec{s}=\int_i^f pdV\\)

- \\(p\\)-\\(V\\) diagram

  ![p-V diagram]({{site.url}}/images/posts/Thermodynamics/thermodynamics_1.png)

  *Notice*: A process that can be drawn into a \\(p\\)-\\(V\\) diagram must be a **quasistatic process**（准静态过程）, which is also be **reversible** if **no dissipation exists** during the process.

  Figure f shows a cycle in which the work (done by the gas) can be calculated by the area:
  \\[
  W(by\ the\ gas)=\oint_{\partial D^-}pdV
  \\]
  \\(\partial D^-\\) means if the path is clockwise, \\(W\\) is positive.

  (But usually I'd like to take everything anti-clockwise as positive. Therefore, I made myself to remember **work done by the outside** to be an integral alone \\(\partial D^+\\))

- The First Law of Thermodynamics
  \\[
  \begin{eqnarray}
  \Delta E_{int}&=&Q-W(by\ the\ system)\\\
  &=&Q+W(on\ the\ system)
  \end{eqnarray}
  \\\
  or
  \\\
  dE_{int}=dQ-dW
  \\]
  Some special cases:

  - Adiabatic processes:
    \\[
    Q=0
    \\]

  - Constant-volume processes:
    \\[
    W=0
    \\]

  - Cyclical processes:
    \\[
    Q=W, \Delta E_{int}=0
    \\]

  - Free expansions:
    \\[
    Q=W=0=\Delta E_{int}
    \\]

- Three Transfer Mechanisms:

  - Conduction
    \\[
    P_{cond}=\frac{dQ}{dt}=kA\frac{T_{High}-T_{Low}}{L}
    \\]
    Where \\(k\\) is the thermal conductivity which depends only on the material, \\(A\\) is the face area and \\(L\\) is the thickness. 

    Also, we can define a value similar to *Resistance* called *thermal resistance*: \\(R=\frac{L}{k}\\).

    (But unlike Resistance which is relevant to \\(A\\), \\(R\\) has nothing to do with \\(A\\))

  - Convection

  - Radiation
    \\[
    P_{rad}=\sigma \varepsilon AT^4
    \\]
    Where \\(\sigma=5.6704\times10^{-8}W/m^2\cdot K^4\\) is the *Stefan-Boltzmann constant*, \\(\varepsilon\\) is the *emissivity(辐射系数)* of the object's surface. And \\(A\\) is the area, \\(T\\) is the temperature.

- Ideal Gases

  - \\(pV=NkT\\)

    Proof. (I am too lazy to draw a picture… Just imagine it)

    Imagine a plunger, one side of which is full of ideal gases(Ideal gases means the interaction between molecules can be ignored). The total number of the molecules is \\(N\\), the volume of the container is \\(V\\), the area of the plunger is \\(S\\), the velocity of the molecule is \\(v\\) and the mass of one molecule is \\(m\\).

    Now take the direction vertical to the plunger as \\(x\\)-direction. So in a shortly enough interval \\(\Delta t\\), the number of collisions between molecules and the plunger is \\(v_x \cdot \Delta t \cdot S \cdot n\\), where \\(n=\frac{N}{V}\\) is the number of molecules within an unit volume.

    (Notice that \\(v_x\\) here is a kind of average, but not the average velocity which is apparently \\(0\\))

    Then according to the *theorem of momentum*, 
    \\[
    F\Delta t=n\cdot v_x \cdot \Delta t \cdot S \cdot 2mv_x\\\
    \Longrightarrow F=2nmv_x^2S\\\
    \Longrightarrow p=\frac{F}{S}=2nmv_x^2
    \\]
    Now how to take care of \\(v_x^2\\), this 'kind of' average thing? We the average of the squares of the following equation:
    \\[
    v^2=v_x^2+v_y^2+v_z^2
    \\]
    And that is:
    \\[
    <v^2>=<v_x^2>+<v_y^2>+<v_z^2>
    \\]
    Then because of the symmetry between \\(x\\),\\(y\\) and \\(z\\), we have \\(<v_x^2>=<v_y^2>=<v_z^2>=\frac{1}{3}<v^2>\\)

    But this is not really true, because only those molecules whoes \\(v_x>0\\) has the chance to collide with the plunger, so what we are really concerned about are just \\(<v_{x+}^2>=\frac{1}{2}<v_x^2>=\frac{1}{6}<v^2>\\). Let's correct the 'incorrect' equations by adding a 'plus' to the subscript:
    \\[
    p=2nm\cdot \frac{1}{6}<v^2>=\frac{2}{3}n<\frac{1}{2}mv^2>
    \\]
    Now with \\(n=\frac{N}{V}\\), we get:
    \\[
    pV=\frac{2}{3}N<\frac{1}{2}mv^2>
    \\]
    For ideal gases, \\(<\frac{1}{2}mv^2>\propto T\propto E_{int}\\). So the equation becomes:
    \\[
    pV=NkT
    \\]
    Where \\(k=1.38\times 10^{-23}J/K\\) is the Boltzmann constant.

    Here we can also another three important formulas:
    \\[
    K_{avg}=<\frac{1}{2}mv^2>=\frac{3}{2}kT\\\
    \Longleftrightarrow v_{rms}=\sqrt{\frac{3kT}{m}}\\\
    and\\\
    p=\frac{1}{3}nmv_{rms}^2=\frac{1}{3}\frac{Nmv_{rms^2}}{V}
    \\]
    (\\(v_{rms}=\sqrt{<v^2>}\\) is the **root-mean-square speed**)

    Q.E.D.

  - Mean Free Path
    \\[
    \lambda=\frac{length\ of\ path\ during\ \Delta t}{number\ of\ collisions\ in\ \Delta t}\\\
    length\ of\ path\ during\ \Delta t =v_{avg}\cdot \Delta t\\\
    number\ of\ collisions\ during\ \Delta t =V\cdot n
    \\]
    Where \\(V\\) is the volume swept out and \\(n=\frac{N}{V}\\) is still the number of molecules per unit volume.

    We assume one molecule to have a rudius of \\(d\\), which is the only one moving, and others to be still.

    Then \\(V=\Delta x\cdot S=v_{rel}\cdot S\cdot \Delta t=\pi d^2v_{rel}\Delta t\\),

    and we got \\(\lambda=\frac{1}{\sqrt{2}\pi d^2N/V}\\), this is based on the relation \\(v_{rel}=\sqrt{2}v_{avg}\\).

- Maxwell's Speed Distribution Law:
  \\[
  P(v)=4\pi (\frac{m}{2\pi kT})^\frac{3}{2}v^2e^{\frac {mv^2}{2kT}}
  \\]
  \\(P(v)\\) is the probabilty for a molecule to be at the speed of v, which satisfies the normalization condition such that \\(\int_0^\infty P(v)=1\\).

  ![P(v)]({{site.url}}/images/posts/Thermodynamics/thermodynamics_2.png)

  The average of speed then is:
  \\[
  v_{avg}=\int_0^\infty vP(v)dv=\sqrt{\frac{8kT}{\pi m}}
  \\]
  And we have a second way to calculate the root-mean-square speed:
  \\[
  v_{rms}=\sqrt{\int_0^\infty v^2P(v)dv}
  \\]
  The velocity corresponding to the peak of the image is the **most probable speed**, which can be calculated by solving \\(\frac{dP}{dv}\rvert_{v=v_P}=0\Longrightarrow v_P=\sqrt{\frac{2kT}{m}}\\).


(\\(\frac{M}{R}=\frac{m}{k}\\) for all formulas.)

- Heat again

  For Ideal Gases:

  - Internal Energy:

    Interaction between molecules can be ignored, therefore, the molecular potential energy can be ignored. Only the **translational** kinetic energy does contribution to the total internal energy, which gives us the possibility to calculate the internal energy:
    \\[
    E_{int}=N\cdot K_{avg}=N\cdot \frac{3}{2}kT=\frac{3}{2}NkT
    \\]

  - Molar Specific Heat

    Similar to specific heat in \\(Q=cm\Delta T\\), we can use amount of substance \\(n\\) in stead of mass \\(m\\) to measure the amount. And there we get *Molar Specific Heat*.

    However, this concept has two different values under different situations(constant volume or constant pressure), which are notated as \\(C_V\\) and \\(C_p\\).

    - \\(C_V\\)
      \\[
      Q=nC_V\Delta T
      \\]
      Constant volume suggests that the work done by the gas is 0.

      According to the 1st law:
      \\[
      \begin{eqnarray}
      \Delta E_{int}&=&Q-W\\\
      &=&nC_V\Delta T-0
      \end{eqnarray}
      \\\
      \Longrightarrow C_V=\frac{\Delta E_{int}}{n\Delta T}=\frac{\frac{3}{2}Nk\Delta T}{n\Delta T}=\frac{3}{2}R
      \\]
      The equation only applies to monatomic molecules. The more general expression is
      \\[
      C_V=\frac{f}{2}R
      \\]
      , where \\(f\\) is the *degrees of freedom* of the gases. \\(f\\) is determined both by the structure of molecules and temperature.

      ![C_V]({{site.url}}/images/posts/Thermodynamics/thermodynamics_3.png)

      ![C_V corresponding to T]({{site.url}}/images/posts/Thermodynamics/thermodynamics_4.png)

      With the concept of \\(C_V\\), we can rewrite the expression of the internal energy of any ideal gases:
      \\[
      E_{int}=nC_VT\\\
      and\\\
      \Delta E_{int}=nC_V\Delta T
      \\]
      This crucial expression implies that **the internal energy of a certain amount of any ideal gas is only determined by the temperautre**. Which means we can always use 'Path 1' to calculate the change in \\(\Delta E_{int}\\):

      ![Path_1]({{site.url}}/images/posts/Thermodynamics/thermodynamics_5.png)

    - \\(C_p\\)

      Under a contant pressure:
      \\[
      \begin{eqnarray}
      \Delta E_{int}&=&Q-W,W=p\Delta V\\\
      &=& nC_p\Delta T-nR\Delta T\\\
      &=&n(C_p-R)\Delta T\\\
      &=&nC_V\Delta T
      \end{eqnarray}
      \\\
      \Longrightarrow C_V=C_p-R\\\
      \Longrightarrow C_p=C_V+R
      \\]

- Four Processes:

  - Adiabatic Process: \\(Q=0\\)

    - Free Expansions:
      \\[
      Q=0,W=0\\\
      \Delta E_{int}=0\\\
      \Longrightarrow\Delta T=0\\\
      \Longrightarrow \Delta(pV)=p_fV_f-p_iV_i=0
      \\]

    - Insulated Container:
      \\[
      pV=nRT\\\
      d(pV)=pdV+Vdp=nRdT\\\
      \begin{eqnarray}
      dE_{int}&=&dQ-dW\\\
      &=&0-pdV\\\
      &=&nC_VdT
      \end{eqnarray}
      \\\
      ndT=-\frac{pdV}{C_V}=\frac{pdV+Vdp}{C_p-C_V}\\\
      \Longrightarrow C_VVdp+C_ppdV=0\\\
      \Longrightarrow \frac{dp}{p}+\frac{C_p}{C_V}\frac{dV}{V}=0\\\
      \Longrightarrow d(\ln p+\gamma\ln V)=d\ln (pV^\gamma)=0\\\
      \Longrightarrow pV^\gamma=a\ constant, \gamma=\frac{C_p}{C_V}\\\
      W=\int_i^fpdV=p_iV_i^\gamma\int_i^fV^{-\gamma}dV=\frac{p_iV_i^\gamma}{1-\gamma}(V_f^{1-\gamma}-V_i^{1-\gamma})
      \\]
      For diatomic molecules, \\(\gamma=\frac{C_p}{C_V}=\frac{\frac{7}{2}}{\frac{5}{2}}=1.4\\)

  - Constant-volume(Isochoric) Process: (\\(dW=pdV=0\\))
    \\[
    \Delta pV=nR\Delta T\\\
    \Delta E_{int}=Q=nC_V\Delta T=\frac{C_V}{R}V\Delta p
    \\]

  - Constant-pressure(Isobaric) Process:
    \\[
    W=p\Delta V=nR\Delta T\\\
    Q=nC_p\Delta T\\\
    \Delta E_{int}=Q-W=nC_V\Delta T=\frac{C_V}{R}p\Delta V
    \\]

  - Constant-temperature(Isothermal) Process:
    \\[
    \Delta E_{int}=Q-W=0\\\
    \begin{eqnarray}
    Q=W&=&\int_i^f pdV\\\
    &=&nRT\int_i^f\frac{1}{V}dV\\\
    &=&nRT\ln \frac{V_f}{V_i}
    \end{eqnarray}
    \\]

- **Entropy**

  The change of entropy of a quasistatic process can be defined as following:
  \\[
  \Delta S=\int_i^f\frac{dQ}{T}\\\
  or\\\
  dS=\frac{dQ}{T}
  \\]
  Bear in mind that a quasistatic process **might not** be reversible. Reversible process is a quasistatic process without dissipation.

  - State Function

    Entropy is a state Function which means its value only depends on the state of the system. For a certain amount of ideal gases, the values that matter are \\((p,V,T)\\).

    Therefore, to deal with an irreversible process, we can choose a reversible process having the same initial and final state which is calculable.

    With the spirit of 'state function', \\(\Delta S\\) can be figured out:
    \\[
    dE_{int}=dQ-dW\\\
    \Longrightarrow dQ=dE_{int}+dW=nC_VdT+pdV\\\
    dS=\frac{dQ}{T}=\frac{nC_VdT}{T}+\frac{pdV}{T}\\\
    \frac{p}{T}=\frac{nR}{V}\\\
    dS=\frac{nC_VdT}{T}+\frac{nRdV}{V}\\\
    \Delta S=nC_V\ln\frac{T_f}{T_i}+nR\ln\frac{V_f}{V_i}
    \\]
    This formula is correct for all process of ideal gases.

  - Four Processes from The View of Entropy

    - Adiabatic Process:

      - Free Expansions:
        \\[
        T_i=T_f\\\
        \Delta S=nR\ln\frac{V_f}{V_i}=-nR\ln\frac{p_f}{p_i}>0
        \\]

      - Insulated Container:
        \\[
        dS=\frac{dQ}{T}\equiv 0
        \\]

    - Constant-volume(Isochoric) Process:
      \\[
      \Delta S=nC_V\ln\frac{T_f}{T_i}=nC_V\ln\frac{p_f}{p_i}
      \\]

    - Constant-pressure(Isobaric) Process:
      \\[
      \frac{V_f}{V_i}=\frac{T_f}{T_i}\\\
      \Delta S=nC_p\ln\frac{V_f}{V_i}=nC_p\ln\frac{T_f}{T_i}
      \\]

    - Constant-temperature(Isothermal) Process:
      \\[
      \Delta S=nR\ln\frac{V_f}{V_i}\\\
      or\\\
      \Delta S=\frac{1}{T}\int_i^fdQ=\frac{Q}{T}
      \\]

- The Second Law of Thermodynamics

  For a process occuring in a closed system, the entropy of the system:
  \\[
  \Delta S\ge 0
  \\]
  And \\(\Delta S=0\\) only for reversible processes.

  *Alternative version*: No series of processes is possible whoes sole result is the transfer of energy as heat from a thermal reservoir(热库) and the complete conversion of this energy to work.

- Engines

  An engine is a device that extracts energy from its environment in the form of heat and does useful work.

  **Carnot Engine** is a type of ideal engines, which has no wasteful energy transferred due to friction and turbulence.

  ![Carnot]({{site.url}}/images/posts/Thermodynamics/thermodynamics_6.png)

  ![Carnot]({{site.url}}/images/posts/Thermodynamics/thermodynamics_7.png)

  ![Carnot]({{site.url}}/images/posts/Thermodynamics/thermodynamics_8.png)

  Carnot Engine:

  1. Isothermal compression
     \\[
     W_1=|Q_H|=\int_a^bpdV=nRT_H\int_a^b\frac{1}{V}dV=nRT_H\ln\frac{V_b}{V_a}\\\
     \Delta S_1=\frac{Q}{T_H}=\frac{-W}{T_H}=nR\ln\frac{V_a}{V_b}
     \\]

  2. Adiabatic compression
     \\[
     W_2=\int_b^cpdV=\frac{p_bV_b^{\gamma}}{1-\gamma}(V_c^{1-\gamma}-V_b^{1-\gamma})\\\
     \Delta S_2=0
     \\]

  3. Isothermal expansion
     \\[
     W_3=-|Q_L|=\int_c^dpdV=nRT_L\ln\frac{V_d}{V_c}\\\
     \Delta S_3=nR\ln\frac{V_c}{V_d}
     \\]

  4. Adiabatic expansion
     \\[
     W_4=\int_d^apdV=\frac{p_dV_d^\gamma}{1-\gamma}(V_a^{1-\gamma}-V_b^{1-\gamma})\\\
     \Delta S_4=0
     \\]



  Totally,
\\[
  \Delta E_{int}=0\\\
  \Longrightarrow W=\lvert Q_H\rvert-\lvert Q_L\rvert\\\
  \Delta S=\Delta S_H+\Delta S_L=\frac{\lvert Q_H\rvert}{T_H}-\frac{\lvert Q_L\rvert}{T_L}
\\]
  For a complete cycle, the final state is the same as the initial state:
\\[
  \Longrightarrow \Delta S=0\\\
  \frac{\lvert Q_H\rvert}{T_H}=\frac{\lvert Q_L\rvert}{T_L}\\\
  or\\\
  \frac{V_b}{V_a}=\frac{V_c}{V_d}
\\]

  - Efficiency of a Engine
    \\[
    \varepsilon=\frac{|W|}{|Q_H|}
    \\]
    Efficiency of a Carnot Engine
    \\[
    \varepsilon=\frac{|Q_H|-|Q_L|}{Q_H}=1-\frac{Q_L}{Q_H}=1-\frac{T_L}{T_H}
    \\]
    A real engine's efficiency is **no greater than** this \\(\varepsilon\\).

  - Carnot Refrigerator

    Similar to an engine. But for a refrigerator the value we are concerned about is *coefficient of performance* \\(K=\frac{|Q_L|}{|W|}=\frac{|Q_L|}{|Q_H|-|Q_L|}\\)

    If the refrigerator is a carnot refrigerator,

    \\(K_C=\frac{T_L}{T_H-T_L}\\)

- Statistical View

  Consider an insulated box with two halves. Within which are molecules of number N. Focus on the *configurations* of the N molecules, assuming there are \\(n_1\\) molecules in the left half, \\(n_2\\) for the right. The total number of configurations is \\(W=C_N^{n_1}=\frac{N!}{n_1!n_2!}\\).

  The basic assumption of statistical mechanics is:

  **All microstates are equally probable.**

  The entropy of the system should then be written as:
  \\[
  S=k\ln W
  \\]
  , where \\(k\\) is again the Boltzmann's constant.

  /**

  *Stirling's approximation:*
  \\[
  \ln N!\approx N\ln N-N
  \\]
  See it here: [Wiki](https://en.wikipedia.org/wiki/Stirling%27s_approximation)

  **/







```
by freezingSummer
Jan.2018
```
