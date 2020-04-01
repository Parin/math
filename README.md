# Repository that contains simple and intutite Math concepts usind in Machine Learning

# 1. Understanding Angular metric in Annoy Index

Annoy uses *Euclidean* distance of *normalized* vectors for its angular distance, which for two vectors $u$, $v$ is equal to $\sqrt{2(1-cos(u,v))}$

For $\mathcal{L_2}$ normalized vectors $u$ and $v$,
* $||u||=1$ and $||v||=1$

Euclidean distance $ED$,
\begin{equation}
\begin{split}
ED &= || u - v||\\
   &= \sqrt{(u - v)^(u - v)}\\
   &= \sqrt{u^Tu - 2u^Tv + v^Tv}\\
   &= \sqrt{2 -2u^Tv}\\
   &= \sqrt{2(1 - \frac{2u^Tv}{||u||||v||})}\\
   &= \sqrt{2(1-cos(u,v))}
\end{split}
\end{equation}

Thus, **Euclidean distance** betwenn two vectors is proprtional (non-linearly) to their **Cosine similarity**
and the range for $ED$ is $[0, \sqrt{2}]$.  So, the value for threshold to compute Rest2Vec SLO can very between
$[0, \sqrt{2}]$. We choose the threshold on distance such that to **maximize** the coverage!
