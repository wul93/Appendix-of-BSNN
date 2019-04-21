# Appendix
## The Augmented Lagrangian algorithm
&ensp;&ensp; We introduce <a href="https://www.codecogs.com/eqnedit.php?latex=w_b" target="_blank"><img src="https://latex.codecogs.com/gif.latex?w_b" title="w_b" /></a> between <a href="https://www.codecogs.com/eqnedit.php?latex=w" target="_blank"><img src="https://latex.codecogs.com/gif.latex?w" title="w" /></a> and <a href="https://www.codecogs.com/eqnedit.php?latex=sign(w)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?sign(w)" title="sign(w)" /></a>, which can be treated as the middle variable and pseudo binary. At initial stage of training, the function need satisfy <a href="https://www.codecogs.com/eqnedit.php?latex={w_b}&space;\approx&space;w" target="_blank"><img src="https://latex.codecogs.com/gif.latex?{w_b}&space;\approx&space;w" title="{w_b} \approx w" /></a> for the better convergence of loss function; at final phase of training, the function need satisfy <a href="https://www.codecogs.com/eqnedit.php?latex={w_b}&space;\approx&space;sign(w)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?{w_b}&space;\approx&space;sign(w)" title="{w_b} \approx sign(w)" /></a> for binary weight. We introduce <a href="https://www.codecogs.com/eqnedit.php?latex=w_b" target="_blank"><img src="https://latex.codecogs.com/gif.latex?w_b" title="w_b" /></a> between <a href="https://www.codecogs.com/eqnedit.php?latex=w" target="_blank"><img src="https://latex.codecogs.com/gif.latex?w" title="w" /></a> and <a href="https://www.codecogs.com/eqnedit.php?latex=sign(w)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?sign(w)" title="sign(w)" /></a> as follows:
<div align=center>
  <a href="https://www.codecogs.com/eqnedit.php?latex=w_b&space;=&space;argmin_{w_b}                (h(x)&space;&plus;&space;g(x))&space;\\&space;=&space;argmin_{w_b}(\frac{\rho}{2}&space;{\left&space;\|&space;{w_b}&space;-&space;sign(w)&space;\right&space;\|}^2&space;&plus;&space;\lambda&space;{\left&space;\langle&space;\mu,{w_b}&space;-&space;sign(w)&space;\right&space;\rangle}&space;&plus;&space;\frac{1}{2}&space;{\left&space;\|&space;{w_b}&space;-&space;w&space;\right&space;\|}^2)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?w_b&space;=&space;argmin_{w_b}(h(x)&space;&plus;&space;g(x))&space;\\&space;=&space;argmin_{w_b}(\frac{\rho}{2}&space;{\left&space;\|&space;{w_b}&space;-&space;sign(w)&space;\right&space;\|}^2&space;&plus;&space;\lambda&space;{\left&space;\langle&space;\mu,{w_b}&space;-&space;sign(w)&space;\right&space;\rangle}&space;&plus;&space;\frac{1}{2}&space;{\left&space;\|&space;{w_b}&space;-&space;w&space;\right&space;\|}^2)" title="w_b = argmin_{w_b}(h(x) + g(x)) \\ = argmin_{w_b}(\frac{\rho}{2} {\left \| {w_b} - sign(w) \right \|}^2 + \lambda {\left \langle \mu,{w_b} - sign(w) \right     \rangle} + \frac{1}{2} {\left \| {w_b} - w \right \|}^2)" /></a> </div>
where we construct <a href="https://www.codecogs.com/eqnedit.php?latex=g(x)=\frac{1}{2}{\left&space;\|&space;{w_b}&space;-w&space;\right&space;\|}^2" target="_blank"><img src="https://latex.codecogs.com/gif.latex?g(x)=\frac{1}{2}{\left&space;\|&space;{w_b}&space;-w&space;\right&space;\|}^2" title="g(x)=\frac{1}{2}{\left \| {w_b} -w \right \|}^2" /></a>, <a href="https://www.codecogs.com/eqnedit.php?latex=h(x)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?h(x)" title="h(x)" /></a> is shown as Eq(11) in paper; at initial stage of training, <a href="https://www.codecogs.com/eqnedit.php?latex=\rho" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\rho" title="\rho" /></a> is small enough to be ignored, so we can reach <a href="https://www.codecogs.com/eqnedit.php?latex={w_b}&space;\approx&space;w" target="_blank"><img src="https://latex.codecogs.com/gif.latex?{w_b}&space;\approx&space;w" title="{w_b} \approx w" /></a>; at final phase of training, <a href="https://www.codecogs.com/eqnedit.php?latex=\rho" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\rho" title="\rho" /></a> is large enough to ignore <a href="https://www.codecogs.com/eqnedit.php?latex=g(x)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?g(x)" title="g(x)" /></a>. The minimal value of function is acquired as follows:
<div align=center>
  <a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial{(h(x)&plus;g(x))}}{\partial{w_b}}&space;=&space;0" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{\partial{(h(x)&plus;g(x))}}{\partial{w_b}}&space;=&space;0" title="\frac{\partial{(h(x)+g(x))}}{\partial{w_b}} = 0" /></a></div>
<div align=center>
  <a href="https://www.codecogs.com/eqnedit.php?latex=\rho&space;({w_b}-sign(w))&space;&plus;&space;\lambda&space;\mu&space;&plus;&space;{w_b}&space;-&space;w&space;=&space;0" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\rho&space;({w_b}-sign(w))&space;&plus;&space;\lambda&space;\mu&space;&plus;&space;{w_b}&space;-&space;w&space;=&space;0" title="\rho ({w_b}-sign(w)) + \lambda \mu + {w_b} - w = 0" /></a></div>
Then, <a href="https://www.codecogs.com/eqnedit.php?latex=w_b" target="_blank"><img src="https://latex.codecogs.com/gif.latex?w_b" title="w_b" /></a> can be descriped as follows:
<div align=center>
 <a href="https://www.codecogs.com/eqnedit.php?latex={w_b}&space;=&space;\frac{\rho&space;\cdot&space;sign(w)&space;-&space;\lambda&space;\mu&space;&plus;&space;w}{\rho&space;&plus;&space;1}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?{w_b}&space;=&space;\frac{\rho&space;\cdot&space;sign(w)&space;-&space;\lambda&space;\mu&space;&plus;&space;w}{\rho&space;&plus;&space;1}" title="{w_b} = \frac{\rho \cdot sign(w) - \lambda \mu + w}{\rho + 1}" /></a></div>
In the same way, we can use the derivation of <a href="https://www.codecogs.com/eqnedit.php?latex=\mu" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\mu" title="\mu" /></a>:
<div align=center>
  <a href="https://www.codecogs.com/eqnedit.php?latex=\frac{\partial(h(x)&plus;g(x))}{\partial&space;\mu}&space;=&space;\lambda&space;({w_b}&space;-&space;sign(w))" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\frac{\partial(h(x)&plus;g(x))}{\partial&space;\mu}&space;=&space;\lambda&space;({w_b}&space;-&space;sign(w))" title="\frac{\partial(h(x)+g(x))}{\partial \mu} = \lambda ({w_b} - sign(w))" /></a></div>
According to the gradient descent method, <a href="https://www.codecogs.com/eqnedit.php?latex=\mu" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\mu" title="\mu" /></a> can be updated as follows:
<div align=center>
  <a href="https://www.codecogs.com/eqnedit.php?latex=\mu&space;=&space;\mu&space;-&space;\eta&space;\cdot&space;\lambda&space;({w_b}-sign(w))" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\mu&space;=&space;\mu&space;-&space;\eta&space;\cdot&space;\lambda&space;({w_b}-sign(w))" title="\mu = \mu - \eta \cdot \lambda ({w_b}-sign(w))" /></a></div>
where <a href="https://www.codecogs.com/eqnedit.php?latex=\eta" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\eta" title="\eta" /></a> is the learning rate. At final, the loss function <a href="https://www.codecogs.com/eqnedit.php?latex=f(w_b)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?f(w_b)" title="f(w_b)" /></a> can be updated in the same way as follows:
<div align=center>
  <a href="https://www.codecogs.com/eqnedit.php?latex=w&space;=&space;w&space;-&space;\eta&space;\bigtriangledown&space;f(w_b)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?w&space;=&space;w&space;-&space;\eta&space;\bigtriangledown&space;f(w_b)" title="w = w - \eta \bigtriangledown f(w_b)" /></a></a></div>
Parameters can be iteratively updated as follows:
<div align=center>
<a href="https://www.codecogs.com/eqnedit.php?latex=\left\{&space;\begin{aligned}&space;&{w_b^{k&plus;1}}&space;=&space;\frac{\rho&space;^&space;k&space;sign(w^k)&space;&plus;&space;w^k&space;-&space;\lambda&space;^&space;k&space;\mu&space;^&space;k}{\rho&space;^&space;k&space;&plus;&space;1}\\&space;&\mu&space;^&space;{k&plus;1}&space;=&space;\mu&space;^&space;k&space;-&space;\eta&space;\lambda(w_b^k&space;-&space;sign(w))&space;\\&space;&w^{k&plus;1}&space;=&space;w^k&space;-&space;\eta&space;\bigtriangleup&space;f(w_b^k)&space;\\&space;&\rho&space;^{k&plus;1}&space;=&space;\gamma_{\rho}&space;\rho&space;^&space;k,&space;\lambda&space;^{k&plus;1}&space;=&space;\gamma_{\lambda}&space;\lambda^k&space;\end{aligned}&space;\right." target="_blank"><img src="https://latex.codecogs.com/gif.latex?\left\{&space;\begin{aligned}&space;&{w_b^{k&plus;1}}&space;=&space;\frac{\rho&space;^&space;k&space;sign(w^k)&space;&plus;&space;w^k&space;-&space;\lambda&space;^&space;k&space;\mu&space;^&space;k}{\rho&space;^&space;k&space;&plus;&space;1}\\&space;&\mu&space;^&space;{k&plus;1}&space;=&space;\mu&space;^&space;k&space;-&space;\eta&space;\lambda(w_b^k&space;-&space;sign(w))&space;\\&space;&w^{k&plus;1}&space;=&space;w^k&space;-&space;\eta&space;\bigtriangleup&space;f(w_b^k)&space;\\&space;&\rho&space;^{k&plus;1}&space;=&space;\gamma_{\rho}&space;\rho&space;^&space;k,&space;\lambda&space;^{k&plus;1}&space;=&space;\gamma_{\lambda}&space;\lambda^k&space;\end{aligned}&space;\right." title="\left\{ \begin{aligned} &{w_b^{k+1}} = \frac{\rho ^ k sign(w^k) + w^k - \lambda ^ k \mu ^ k}{\rho ^ k + 1}\\ &\mu ^ {k+1} = \mu ^ k - \eta \lambda(w_b^k - sign(w)) \\ &w^{k+1} = w^k - \eta \bigtriangleup f(w_b^k) \\ &\rho ^{k+1} = \gamma_{\rho} \rho ^ k, \lambda ^{k+1} = \gamma_{\lambda} \lambda^k \end{aligned} \right." /></a></div>
where <a href="https://www.codecogs.com/eqnedit.php?latex=k" target="_blank"><img src="https://latex.codecogs.com/gif.latex?k" title="k" /></a> is the number of iterative.

## The Dynamics-back STDP
&ensp;&ensp; The STDP rule as the most effective biological unsupervised learning method provides super ability for learning. It reveals how the weight is optimized by the time sequence of the pre-synaptic and post-synaptic that performs LTD (long term depression) and LTP (long term potential).
<div align=center>
  <a href="https://www.codecogs.com/eqnedit.php?latex=\bigtriangleup&space;w&space;=&space;\left\{&space;\begin{aligned}&space;&e^{-\bigtriangleup&space;t&space;/&space;{\gamma_{&plus;}}}&space;\qquad&space;t_{post}&space;>&space;t_{pre}\\&space;&-e^{-\bigtriangleup&space;t&space;/&space;{\gamma_{-}}}&space;\qquad&space;t_{post}&space;<&space;t_{pre}&space;\end{aligned}&space;\right." target="_blank"><img src="https://latex.codecogs.com/gif.latex?\bigtriangleup&space;w&space;=&space;\left\{&space;\begin{aligned}&space;&e^{-\bigtriangleup&space;t&space;/&space;{\gamma_{&plus;}}}&space;\qquad&space;t_{post}&space;>&space;t_{pre}\\&space;&-e^{-\bigtriangleup&space;t&space;/&space;{\gamma_{-}}}&space;\qquad&space;t_{post}&space;<&space;t_{pre}&space;\end{aligned}&space;\right." title="\bigtriangleup w = \left\{ \begin{aligned} &e^{-\bigtriangleup t / {\gamma_{+}}} \qquad t_{post} > t_{pre}\\ &-e^{-\bigtriangleup t / {\gamma_{-}}} \qquad t_{post} < t_{pre} \end{aligned} \right." /></a>
</div>
where <a href="https://www.codecogs.com/eqnedit.php?latex=\bigtriangleup&space;t&space;=&space;{\left&space;|&space;t_{post}&space;-&space;t_{pre}&space;\right&space;|}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\bigtriangleup&space;t&space;=&space;{\left&space;|&space;t_{post}&space;-&space;t_{pre}&space;\right&space;|}" title="\bigtriangleup t = {\left | t_{post} - t_{pre} \right |}" /></a> denotes the interval between the spiking time of pre- and post- synapse. <a href="https://www.codecogs.com/eqnedit.php?latex=w=w^{\ast}&space;&plus;&space;\bigtriangleup&space;w" target="_blank"><img src="https://latex.codecogs.com/gif.latex?w=w^{\ast}&space;&plus;&space;\bigtriangleup&space;w" title="w=w^{\ast} + \bigtriangleup w" /></a>,  where <a href="https://www.codecogs.com/eqnedit.php?latex=w" target="_blank"><img src="https://latex.codecogs.com/gif.latex?w" title="w" /></a> is the weight after STDP, and <a href="https://www.codecogs.com/eqnedit.php?latex=w^{\ast}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?w^{\ast}" title="w^{\ast}" /></a> is the initial weight. [Caporale and Dan, 2008] expand the STDP rule. if the <a href="https://www.codecogs.com/eqnedit.php?latex=\bigtriangleup&space;t" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\bigtriangleup&space;t" title="\bigtriangleup t" /></a> is netative, the weight reduction with an exponential decay law, and vice versa. We can deduce the conclusion as follows:
<div align=center>
  <a href="https://www.codecogs.com/eqnedit.php?latex=w&space;=&space;\left\{&space;\begin{aligned}&space;&w^{\ast}&space;-&space;e^{-\bigtriangleup&space;t&space;/&space;{\gamma_{-}}}&space;\qquad&space;\bigtriangleup&space;t&space;<&space;0&space;\\&space;&w^{\ast}&space;&plus;&space;e^{-\bigtriangleup&space;t&space;/&space;{\gamma_{&plus;}}}&space;\qquad&space;\bigtriangleup&space;t&space;>&space;0&space;\\&space;&w^{\ast}&space;\end{aligned}&space;\right." target="_blank"><img src="https://latex.codecogs.com/gif.latex?w&space;=&space;\left\{&space;\begin{aligned}&space;&w^{\ast}&space;-&space;e^{-\bigtriangleup&space;t&space;/&space;{\gamma_{-}}}&space;\qquad&space;\bigtriangleup&space;t&space;<&space;0&space;\\&space;&w^{\ast}&space;&plus;&space;e^{-\bigtriangleup&space;t&space;/&space;{\gamma_{&plus;}}}&space;\qquad&space;\bigtriangleup&space;t&space;>&space;0&space;\\&space;&w^{\ast}&space;\end{aligned}&space;\right." title="w = \left\{ \begin{aligned} &w^{\ast} - e^{-\bigtriangleup t / {\gamma_{-}}} \qquad \bigtriangleup t < 0 \\ &w^{\ast} + e^{-\bigtriangleup t / {\gamma_{+}}} \qquad \bigtriangleup t > 0 \\ &w^{\ast} \end{aligned} \right." /></a></div>
Therefore, we can find the relationship between <a href="https://www.codecogs.com/eqnedit.php?latex=w" target="_blank"><img src="https://latex.codecogs.com/gif.latex?w" title="w" /></a> and <a href="https://www.codecogs.com/eqnedit.php?latex=\bigtriangleup&space;t" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\bigtriangleup&space;t" title="\bigtriangleup t" /></a>, we can discuss the error in the similar way.

## The odor encoding
&ensp;&ensp; The distribution of combinatorial odor code is proved to be exponential. Statistics suggest that the code satisfies function <a href="https://www.codecogs.com/eqnedit.php?latex=p(r)&space;=&space;\alpha&space;e&space;^{-\alpha&space;r}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?p(r)&space;=&space;\alpha&space;e&space;^{-\alpha&space;r}" title="p(r) = \alpha e ^{-\alpha r}" /></a>. The encoding procession is as follows:
<div align=center>
  <a href="https://www.codecogs.com/eqnedit.php?latex={I_b}=&space;\left\{&space;\begin{aligned}&space;&0&space;\qquad&space;I&space;<&space;r&space;\\&space;&1&space;\qquad&space;I&space;\geqslant&space;r&space;\\&space;\end{aligned}&space;\right." target="_blank"><img src="https://latex.codecogs.com/gif.latex?{I_b}=&space;\left\{&space;\begin{aligned}&space;&0&space;\qquad&space;I&space;<&space;r&space;\\&space;&1&space;\qquad&space;I&space;\geqslant&space;r&space;\\&space;\end{aligned}&space;\right." title="{I_b}= \left\{ \begin{aligned} &0 \qquad I < r \\ &1 \qquad I \geqslant r \\ \end{aligned} \right." /></a>
</div>
where <a href="https://www.codecogs.com/eqnedit.php?latex=I_b" target="_blank"><img src="https://latex.codecogs.com/gif.latex?I_b" title="I_b" /></a> is the binary input, and <a href="https://www.codecogs.com/eqnedit.php?latex=I" target="_blank"><img src="https://latex.codecogs.com/gif.latex?I" title="I" /></a> is full-float input, <a href="https://www.codecogs.com/eqnedit.php?latex=r" target="_blank"><img src="https://latex.codecogs.com/gif.latex?r" title="r" /></a> is the random number with exponential distribution. We can encode the input images by the exponential distribution to generate random 0 or 1. The average firing rate across the entire neuron is estimated by exponential function and the factor is <a href="https://www.codecogs.com/eqnedit.php?latex=1&space;/&space;\alpha" target="_blank"><img src="https://latex.codecogs.com/gif.latex?1&space;/&space;\alpha" title="1 / \alpha" /></a>.
