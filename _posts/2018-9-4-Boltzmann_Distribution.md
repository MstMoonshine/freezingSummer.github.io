---
layout: post
title: Boltzmann Distribution
tags: physics

---


This is a classcial model of distinguishable particles. Let's assume that there are energy levels of \\(E_1, E_2, ...\\) of degeneracy \\(\lambda_1, \lambda_2, ...\\) The total energy of the system is \\(E\\) and there are in total \\(N\\) particals. \\(a_n\\) particals are in n-th energy level, such that
\\[
\sum_n a_n=N,\\\ \tag{1}
\sum_n E_n a_n=E.
\\]


It is natural to take the probability of each state as equal (*average distribution*) so that the probability of the distribution \\(\{a_n\}\\) is proportional to the number of possible states of \\(\{a_n\}\\), which, we shall call, *relative probabiltiy*.

From my own point of view, relative probability is a more basic quantity than probability. If the sum (or integral) over it converges, normalization can be apparently done, from which you would get the probability. But it dose not necessarily converge.



Let's denote the relative probability (or simply the number of possible states) of \\(\{a_n\}\\) as \\(P(\{a_n\})\\).

1. We first put N particles into different energy levels according to \\(\{ a_n \}\\). The order of particles inside the level does not matter now. There are then \\(\frac{N!}{\prod_n a_n!}\\) ways to do this;
2. Now inside each energy level, we need to devide \\(a_n\\) particles into \\(\lambda_n\\) groups. For each particle can be in \\(\lambda_n\\) states, there are \\(\lambda_n^{a_n}\\) ways of doing this in level n. So in total, there are \\(\prod_n \lambda_n^{a_n}\\) ways;
3. \\(P(\{a_n\})=\frac{N!}{\prod_n a_n!}\prod_n \lambda_n^{a_n} \tag{2}\\).



Now the larger \\(P(\{a_n\})\\) is, the more possible to obtain distribution \\(\{a_n\}\\), which has the larger entropy (\\(S=k\ln \Omega\\)). So the distribution that has the largest \\(P(\{a_n\})\\) has the largest entropy and is to be considered as what the system is like.

So we maximize \\(S=\ln P(\{a_n\})\\) under restriction condition eqn.(1) with *Lagrange Multiplier*:
\\[
\delta[S(\{a_n\}) - \alpha \sum_n a_n - \beta \sum_n E_na_n]=0, \tag{3}
\\]
where \\(\delta\\) means the variance of \\(\{a_n\}\\): \\(\delta f(\{a_n\})=f(\{a_n+\delta a_n\})-f(\{a_n\})\\).



Using Stirling formula ( \\(\ln m!\sim m\ln m-m\\) ) and the approximation that \\(a_n \gg \lambda_n \sim 1\\), some simple calculation being done, it can be obtained that *the most probable distribution* takes the form of
\\[
\bar{a}_n=\lambda_ne^{-\alpha-\beta E_n}. \tag{4}
\\]


Define the *partition function* as
\\[
Z=\sum_n \lambda_ne^{-\beta E_n}. \tag{5}
\\]
And it's easy to get \\(\alpha=\ln \frac{Z}{N}\\). Now that \\(Z\\) only depends on \\(\beta\\), \\(\alpha\\) will be determined as soon as \\(\beta \\) is. \\(\beta\\) should be determined by the second equation of eqn.(1), which then reads
\\[
\sum_n E_n\lambda_n e^{-\beta E_n}=\frac{Z}{N}E=\frac{E}{N}\sum_n{\lambda_ne^{-\beta E_n}}.\tag{6}
\\]
This implys some meaning of the partition function —— some kinds of "average". "Once you know the partition function, you know everything". This is because so many variables can be easily obtained from the partition fuction.

It can as well be proved that \\(\beta=\frac{1}{kT}\\). I'm not going to prove it here simply because I don't know how... (Please tell me if some smart reader does.)



We shall see the importance of the most probable distribution by calculating \\(\frac{P(\{\bar{a}_n+\delta a_n\})}{P(\{\bar{a}_n\})}\\), which tells us what the probability is comparing to \\(\{\bar{a}_n\}\\) if the distribution is disturbed a little.
\\[
\begin{eqnarray}
\frac{P(\{\bar{a}_n+\delta a_n\})}{P(\{\bar{a}_n\})} &=& \exp(\ln P(\{\bar{a}_n+\delta a_n\})-\ln P(\{\bar{a}_n\}))\\\
&=&\exp(\delta S(\{a_n\})\vert_{\{a_n\}=\{\bar{a}_n\}}).
\end{eqnarray}
\\]
\\(\delta S(\{a_n\})\\) has been calculated out a few minutes ago from the fisrt term in eqn.(3): \\(\delta S(\{a_n\})=\sum_n\delta a_n\ln \frac{\lambda_n}{a_n}\\). So,
\\[
\frac{P(\{\bar{a}_n+\delta a_n\})}{P(\{\bar{a}_n\})}=\exp(\delta S(\{a_n\})\vert_{\{a_n\}=\{\bar{a}_n\}})=\exp(-\sum_n\delta a_n\ln \frac{\bar{a}_n}{\lambda_n}).\tag{7}
\\]


To evaluate it, let's take 1-D simple harmonic oscillator as an example, where \\(\lambda_n=1, E_n=n\hbar\omega\\).

Partition function: \\(Z=\sum_n e^{-\beta n\hbar\omega}=\frac{1}{e^{\beta\hbar\omega}-1};\\)

Most probable distribution: \\(\bar{a}_n=\frac{N}{Z}e^{-\beta n\hbar\omega}\\),

Assume \\(\delta a_n=\frac{\bar{a}_n}{R}\\), so
\\[
\begin{eqnarray}
\frac{P(\{\bar{a}_n+\delta a_n\})}{P(\{\bar{a}_n\})} &=& \exp(-\sum_n\delta a_n\ln\bar{a}_n)\\\
&=& \exp(-\frac{1}{R}\sum_n \bar{a}_n\ln \bar{a}_n)\\\
&=& \exp(-\frac{1}{R}\sum_n \frac{N}{Z}e^{-\beta n\hbar\omega}(\ln \frac{N}{Z}-\beta n\hbar\omega))\\\
&=& \exp(-\frac{N}{R}(\ln \frac{N}{Z}-Z\beta\hbar\omega e^{\beta\hbar\omega})).
\end{eqnarray}
\\]
Now for a macroscopic matter, \\(N\sim 10^{23}\\).

- If the temperature is very low: \\(\beta\hbar\omega\sim 1\\),

  \\(Z\sim\frac{1}{e-1}=0.5819767,\\)

  \\(\frac{P(\{\bar{a}_n+\delta a_n\})}{P(\{\bar{a}_n\})}\sim\exp(-\frac{10^{23}}{R}(23\ln 10-\ln0.5819767-0.5819767e))=\exp(-\frac{51.9\times 10^{23}}{R}).\\)

  If \\(R=10^{23}\\), that is, \\(\delta a_n=0.00000000000000000000001\times\bar{a}_n\\), the result is fairly small: \\(2.88480... × 10^{-23}\\).

- At room temperature: \\(\beta\hbar\omega\sim 10^{-5}\\),

  \\(Z\sim 10^6,\\)

  \\(\frac{P(\{\bar{a}_n+\delta a_n\})}{P(\{\bar{a}_n\})}\sim\exp(-\frac{10^{23}}{R}(23\ln10-6\ln10-10)))=\exp(-\frac{29.1439\times 10^{23}}{R}),\\)

  which gives us a similar result.

It can be guessed that the expression \\(\frac{P(\{\bar{a}_n+\delta a_n\})}{P(\{\bar{a}_n\})}\\) is not very sensitive to temperature, at least in the range of normal temperature.



This result means that if we change the most probable distribution by a little bit (\\(\sim 10^{-23}\\)), the probability to get the state is fairly low. If we perform a normalization on \\(P(\{a_n\})\\), there would be a extremly sharp peak around \\(\{\bar{a}_n\}\\), or, in other words, \\(P(\{\bar{a}_n\})\approx 1\\). So, in this case, *average distribution* is identical to *the most probable distribution*.
