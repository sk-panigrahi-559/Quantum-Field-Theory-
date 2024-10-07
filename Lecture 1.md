# Classical Field Theories and Principle of Locality
## Classical Field Theory
### Principle of Locality
- In Newtonian Mechanics we have action at a distance.
- Ex: Gravity, Coulomb interactions
- Faraday gave Principle of Locality (1830)
	- All point in space participate in the physical process and the impact propagates form a point to a neighbouring point.
	- **Fields:** mathematical device that the principle of locality works with.
	- we associate each point in space a dynamical variable.
	- Ex: if we have $\vec{E_\vec{x}}(t) = \vec{E}(\vec{x},t)$  $\vec{B_\vec{x}}(t) = \vec{B}(\vec{x},t)$ 
		- **Maxwell Eqns:** 
			- $\nabla\cdot\vec{B}=0$ 
			- $\nabla\cdot\vec{E}=4\pi\rho$
			- $\frac{\partial \vec{B}}{\partial t} = - \nabla\times\vec{E}$ 
			- $4\pi \vec{J} + \frac{\partial \vec{E}}{\partial t} =  \nabla\times\vec{B}$
			- These are called local eqns: contain only $\vec{E}$ and $\vec{B}$ at same point with finite number of derivatives.
	- Ex2: Einstein's Gravity
		- $g_{\mu\nu}(\vec{x},t)$ 
### Types of Fields
- Scalar fields : $\phi(\vec{x},t)$
- vector : $\vec{E}, \vec{B}$
- Tensor fields : $g_{\mu\nu}(\vec{x},t)$ 
- Spinor filds
> [!tip] Convention
> - $\mu$ = 0, 1, 2, 3
> - $X^\mu = (ct,\vec{x}) = (ct,x^i)$
> - $\partial_\mu = (\frac{1}{c}\partial_t,\nabla)$ 
> - $A_\mu = (A_0,\vec{A})=(A_0,A_i)$
> - $c = 1$ and $\hbar = 1$
### Action Principle
- In classical mechanics, $$ S = \int dt L(x,\dot x,t) $$
	- Canonical momentum and Hamiltonian$$p = \frac{\partial L}{\partial \dot x}  ; H=p\dot x -L $$
- equations of motion are obtained from optimizing $S$.
- from principle of locality, L is significantly constrained. $$L = \int d^3 \mathscr{L}(\phi_a,\partial_t\phi_a,\partial_i\phi_a) $$ where $\phi_a(\vec{x},t)$ : General field, $a$ labels different fields
	- $\mathscr{L}$: lagrangian density
	- a function of $\phi_a$ and its derivatives, it only depends on the value of $\phi_a$ and its derivatives at a single point.
> [!note] Remarks
> (i) Principle of locality doesn't allow $$L = \cdot\cdot\cdot+\int d^3xd^3y\phi_a(\vec{x},t)\phi_a(\vec{y},t)$$
> (ii) Only allow first derivative in time and not second derivative $\Rightarrow$ EOM has only two derivatives of time.
> (iii) arbitrary no. of space derivatives are allowed but for simplicity, we use single derivative in space (in relativistic systems we do this to maintain Lorentz invariance, otherwise for non relativistic systems we still can have any no. of space derivatives)

- Canonical Momentum Density $$\Pi(\vec{x},t) = \frac{\partial\mathscr{L}}{\partial \dot \phi_a(\vec{x},t)} $$
- Hamiltonian Density $$\mathscr{H} = \dot\phi\Pi_a -\mathscr{L}$$ $a$ is summed over : Enstein's Convention of repeated indices.
	- EOM: $\delta S =0$ $$\Rightarrow S = \int  dt L = \int d^4 x \mathscr{L}(\phi_a,\partial_\mu\phi_a) $$ $$\Rightarrow\delta S = \int d^4x \left[\frac{\partial\mathscr{L}}{\partial\phi_a} \delta\phi_a+\frac{\partial \mathscr{L}}{\partial(\partial_\mu \phi_a)}\delta(\partial_\mu \phi_a)\right]$$ $$\Rightarrow\delta S = \int d^4x \left[\frac{\partial\mathscr{L}}{\partial\phi_a} \delta\phi_a+\frac{\partial \mathscr{L}}{\partial(\partial_\mu \phi_a)}\partial_\mu(\delta \phi_a)\right]$$ $$\Rightarrow\delta S = \int d^4x \left[\frac{\partial\mathscr{L}}{\partial\phi_a} -\partial_\mu\left(\frac{\partial \mathscr{L}}{\partial(\partial_\mu \phi_a)}\right)\right]\delta\phi_a + BT$$ BT : Boundary terms
	- We always choose $\delta \phi_a$ s.t. BT $\rightarrow$ 0 $$\delta S = 0$$$$\Rightarrow\frac{\partial\mathscr{L}}{\partial\phi_a} -\partial_\mu\left(\frac{\partial \mathscr{L}}{\partial(\partial_\mu \phi_a)}\right)=0$$
	- For simplicity we consider
		- Translational invariance
		- Lorentz invariance
> [!Example] Ex: Maxwell Theory
> Dynamical variables : $A_\mu(x)$
> $F_{\mu\nu} = \partial_\mu A_\nu - \partial_\nu A_\mu$
> $$S_{EM} = \int d^4x\left(-\frac{1}{4}F_{\mu\nu} F^{\mu\nu}\right)$$
> if you do $\delta S_{EM} = 0$ you will get Maxwell's equations in free space.

> [!Example] Ex: Einstein Gravity
> $$S= \frac{1}{16\pi G_N} \int F_g R$$

> [!Example] Ex: Scalar Field
> Consider a real valued scalar field $\Phi(x)$
> Higgs field, pion field are some examples
> 	$$S = \int d^4 x\left[\frac{-1}{2} \partial_\mu\Phi\partial^\mu\Phi-V(\Phi)\right] $$
> Notice that the lorentz indices on the derivatives are contracted $\Rightarrow$ Lorentz invariance
> $V(\Phi) =$ some function of $\Phi$
> Incase of translational symmetry, all parameters in $V(\Phi)$ must be constant. ie they cannot depend on $\Phi$
> $$\Pi(x) = \frac{\partial\mathscr{L}}{\partial\dot\Phi} = \dot\Phi(x) $$
> where $\mathscr{L}$ = quantity inside \[]
> $\partial_\mu\Phi\partial^\mu\Phi = -\dot\Phi^2 + (\nabla\Phi)^2$ 
> Hamiltonian density,
> $$ \mathscr{H} =\Pi\dot\Phi -\mathscr{L} = \frac{\Pi^2}{2} + \frac{1}{2}(\nabla\Phi)^2 + V(\Phi) $$
> EOM: $$\partial^2\Phi-\frac{\partial V}{\partial \Phi} =0 $$
> where $\partial^2 = \partial_\mu\partial^\mu= -\partial_t^2+\nabla^2$
> simplest form : $V(\Phi)= f\Phi$ f is constant
> $\Rightarrow \partial^2\Phi = f$
> in this case we say this '$f$' is some external force
> Say $f=0$
> $$V(\Phi) = \frac{1}{2}m^2\Phi^2$$
> $$\Rightarrow \partial^2 - m^2\Phi = 0$$
> This is **Klein Gordon Equation** : a very famous equation. This is the equation corresponding to the simplest field theory we can consider.
