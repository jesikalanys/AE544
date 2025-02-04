---
date created: 2025-01-31T00:38:26-05:00
date modified: 2025-02-03T00:33:57-05:00
---
# AE_544_LecNote_Examples_Ch01_Ch02

## Textbook problem 1.8 
![[fig-p1-8_rotating_disk_on_train.png|600]]

The rail is straight.

Inertial frame $\calN:\{\nht{}\}$ not shown in the figure, assume $v(t)$ is measured in this frame, doesn't really matter. 

Cartesian frame $\calD:\{\dht1,\dht2,\dht3\}$ centered at the disk

Polar frame $\calE: \{\eht{r},\eht{\theta},\dht3\}$ at the same center

Train is moving in a constant/fixed direction, which is $\dht1$ in the figure.

Disk's constant rotation vector is $\bmo = \omega_{\calE/\calD} \dht3$

Position vector is
$$
\bmr = r \eht{r}
$$

The vector measured in $\calE$ is
$$
\ddtD{\bmr} = r \ddtE\eht{r} = r \bmo\times\eht{r} = r\omega_{\calE/\calD}\dht3\times\eht{r} = r\omega\eht{\theta} = r\omega (-\sin\theta\dht1 + \cos\theta\dht2)
$$
The inertial velocity is then
$$
\dot{\bmr} = \ddtN \bmr = v(t)\dht{1} + \ddtD \bmr = v(t)\dht1 + r\omega (-\sin\theta\dht1 + \cos\theta\dht2)
$$
$$
= (v-r\omega\sin\theta)\dht1 + r\omega \cos\theta\dht2
$$

The inertial acceleration can be directly got as
$$
\begin{aligned}
\ddot{\bmr} &= \ddtN [(v-r\omega\sin\theta)\dht1 + r\omega \cos\theta\dht2] \\
&= (\dot{v}-r\omega\dot{\theta}\cos\theta)\dht1 - r\omega\dot{\theta}\sin\theta \dht2
\end{aligned}
$$


## Textbook problem 1.9
![[fig-p1-8_rotating_disk_on_train.png|600]]
Repeat problem 1.8, but this time assume that the particle P is free to move radially on the disk. Again find the corresponding inertial velocity and acceleration.

Inertial frame $\calN:\{\nht{}\}$ not shown in the figure, assume $v(t)$ is measured in this frame.

Cartesian frame $\calD:\{\dht1,\dht2,\dht3\}$ centered at the disk

Polar frame $\calE: \{\eht{r},\eht{\theta},\dht3\}$ at the same center

Train is moving in a constant/fixed direction, which is $\dht1$ in the figure.

Disk's constant rotation vector is $\bmo = \omega_{\calE/\calD} \dht3$

Position vector is
$$
\bmr = r \eht{r}
$$

The vector measured in $\calE$ is
$$
\begin{aligned}
\ddtD{\bmr} &= \dot{r}\eht{r} + r \ddtE\eht{r} \\
&= \dot{r}\eht{r} + r \bmo\times\eht{r} = \dot{r}\eht{r} + r\omega_{\calE/\calD}\dht3\times\eht{r} \\
&= \dot{r}\eht{r} + r\omega\eht{\theta} \\
&= \dot{r}(\cos\theta\dht1 + \sin\theta\dht2) + r\omega (-\sin\theta\dht1 + \cos\theta\dht2)\\
&=  (\dot{r}\cos\theta - r\omega\sin\theta)\dht1 + (\dot{r}\sin\theta + r\omega\cos\theta)\dht2
\end{aligned}
$$
The inertial velocity is then
$$
\begin{aligned}
\dot{\bmr} &= \ddtN \bmr = v(t)\dht{1} + \ddtD \bmr \\
&= v(t)\dht1 + (\dot{r}\cos\theta - r\omega\sin\theta)\dht1 + (\dot{r}\sin\theta + r\omega\cos\theta)\dht2 \\
&= (v(t) + \dot{r}\cos\theta - r\omega\sin\theta)\dht1 + (\dot{r}\sin\theta + r\omega\cos\theta)\dht2
\end{aligned}
$$

The inertial acceleration can be directly got as
$$
\begin{aligned}
\ddot{\bmr} &= \ddtN [(v(t) + \dot{r}\cos\theta - r\omega\sin\theta)\dht1 + (\dot{r}\sin\theta + r\omega\cos\theta)\dht2] \\
&= (\dot{v} -\ddot{r}\cos\theta-\dot{r}\dot{\theta}\sin\theta - \dot{r}\omega\sin\theta + r\omega\dot{\theta}\cos\theta)\dht1 + (\ddot{r}\sin\theta + \dot{r}\dot{\theta}\cos\theta + \dot{r}\omega\cos\theta - r\omega\dot{\theta}\sin\theta) \dht2 \\
&= (\dot{v} -\ddot{r}\cos\theta - 2\dot{r}\omega\sin\theta + r\omega^2\cos\theta)\dht1 + (\ddot{r}\sin\theta + 2\dot{r}\omega\cos\theta - r\omega^2\sin\theta) \dht2 \\
\end{aligned}
$$

>[!question]- What if the ball is free to move not just radially but in all directions? 
>Then we need to make assumptions about the friction and forces, introduce another frame to describe the relative motion between the ball and the disk.



## Textbook problem 1.14
![[fig-p1-14_grinding_disk.png|600]]

Inertial frame $\calN:\{\nht1,\nht2,\nht3\}$

Polar frame $\calE:\{\eht{r},\eht{\phi},\eht{3}\}$, centered at the center of the grind.

Polar frame $\calS:\{\sht{r},\sht{\theta},\sht{3}\}$, centered at the grind, pointing to $P$.

Constants: $R$, $r$, $h$

Time-varying variables: $\dot{\phi}$, $\dot{\theta}$

Rotation velocity vectors: 

$\bmo_{\calE/\calN} = \dot{\phi}\nht3$

$\bmo_{\calS/\calE} = - \dot{\theta}\eht{r}$ (Notice this is in the negative direction!)

$\bmo_{\calS/\calN} = \dot{\phi}\nht3 - \dot{\theta}\eht{r}$

### (a) inertial v and a
$$
\bmr = r \sht{r} + R \eht{r}
$$

$$
\begin{aligned}
\dot{\bmr} &= \dot{r}\sht{r} + r\ddtN \sht{r} + R \ddtN\eht{r} \\
&= \bm{0} + r\bmo_{\calS/\calN}\times\sht{r} + R\bmo_{\calE/\calN}\times\eht{r} \\
&= r(\dot{\phi}\nht3 - \dot{\theta}\eht{r})\times\sht{r} + R(\dot{\phi}\nht3)\times\eht{r} \\
&= r(\dot{\phi}\nht3\times\sht{r} - \dot{\theta}\eht{r}\times\sht{r}) + R(\dot{\phi}\eht{\phi}) \\
&= r(\dot{\phi}(\cos\theta\sht{r}-\sin\theta\sht{\theta})\times\sht{r} - \dot{\theta}(-\sht{\theta})) + R(\dot{\phi}\eht{\phi}) \\
&= r(\dot{\phi}(\sin\theta\sht{3} + \dot{\theta}\sht{\theta})) + R(\dot{\phi}\eht{\phi}) \\
%&\\
%&= r(\dot{\phi}\nht3 - \dot{\theta}\eht{r})\times(\cos\theta\eht{\phi}+\sin\theta\eht{3}) + R(\dot{\phi}\eht{\phi}) \\
%&= r[\dot{\phi}\nht3\times(\cos\theta\eht{\phi}+\sin\theta\eht{3}) - \dot{\theta}\eht{r}\times(\cos\theta\eht{\phi}+\sin\theta\eht{3})] + R(\dot{\phi}\eht{\phi}) \\
%&= r[\dot{\phi}\nht3\times\cos\theta\eht{\phi} + \dot{\phi}\nht3\times\sin\theta\eht{3} - \dot{\theta}\eht{r}\times\cos\theta\eht{\phi} - \dot{\theta}\eht{r}\times\sin\theta\eht{3}] + R(\dot{\phi}\eht{\phi}) \\
%&= r[-\dot{\phi}\cos\theta\eht{r} + \bm{0} - \dot{\theta}\cos\theta\eht{e} + \dot{\theta}\sin\theta\eht{\phi}] + R(\dot{\phi}\eht{\phi}) \\
\end{aligned}
$$

$$
\ddot{r} = \dots
$$

### (b) as seen by point P
A new frame $\cal{M}:\{\nht1,\nht2,\nht3\}$, which is non-rotating and non-accelerating but just moving along a straight line.

$$
\bm{\rho} = \bmr - \bmr_M
$$

$$
\begin{aligned}
\ddtM \bm{\rho} &= \ddtM \bmr - \ddtM \bmr_M \\
&= \ddtN \bmr + \bmo_{\calM/\calN}\times\bmr - \ddtN\bmr_M + \bmo_{\calM/\calN}\times\bmr_M \\
&= \ddtN \bmr - \ddtN\bmr_M \\
&= r(\dot{\phi}(\sin\theta\sht{3} + \dot{\theta}\sht{\theta}) + R(\dot{\phi}\eht{\phi})   - (-\nht2) \\
&= r(\dot{\phi}(\sin\theta\sht{3} + \dot{\theta}\sht{\theta}) + R(\dot{\phi}\eht{\phi})   + \nht2 \\
\end{aligned}
$$

$$
\ddtM \left(\ddtM \bm{\rho}\right) = \ddtN \left(\ddtN \bmr - \ddtN\bmr_M\right) = \ddot{\bmr} - \ddot{\bmr}_M = \ddot{\bmr}
$$

Alternatively, noticing that $\calM$ is non-rotating and non-accelerating, we can directly calculate the relative velocity and acceleration without taking derivatives using $\ddtM$.



# Monday

## Textbook problem 1.10
![[fig-p1-10_two_rotating_disks.png|600]]
### (a) inertial relative between B and A
Relative position $\bmr = r_B\bht{r} - r_A\aht{r}$.

Relative velocity $\dot{\bmr}=r_B\bmo_{\calB/\calN}\times\bht{r} - r_A\bmo_{\calA/\calN}\times\aht{r}=r_B\omega_{\calB/\calN}\bht{t}-r_A\omega_{\calA/\calN}\aht{r}$ 

Relative acceleration $\ddot{\bmr}=(r_B\dot{\omega}_{\calB/\calN}\bht{t}-r_B\omega_{\calB/\calN}^2\bht{r}) - (r_A\dot{\omega}_{\calA/\calN}\aht{t}-r_A\omega_{\calA/\calN}^2\aht{r})$

### (b) B as seen from A
$$
\begin{aligned}
\ddtA \bmr &= \ddtA (r_B\bht{r} - r_A\aht{r}) = \ddtA (r_B\bht{r}) \\
&= r_B \bmo_{\calB/\calA} \times \bht{r} \\
&= r_B (\omega_{\calB/\calN} - \omega_{\calA/\calN}) \bht{3} \times \bht{r} \\
&= r_B (\omega_{\calB/\calN} - \omega_{\calA/\calN}) \bht{t} \\
\end{aligned}
$$
$$
\begin{aligned}
\ddtA \left(\ddtA \bmr\right) &= \ddtA \left(r_B (\omega_{\calB/\calN} - \omega_{\calA/\calN}) \bht{t}\right) \\
&= \left(r_B (\dot{\omega}_{\calB/\calN} - \dot{\omega}_{\calA/\calN}) \bht{t}\right) + \left(r_B (\omega_{\calB/\calN} - \omega_{\calA/\calN})^2 \bht{3} \times \bht{t}\right)\\
&= \left(r_B (\dot{\omega}_{\calB/\calN} - \dot{\omega}_{\calA/\calN}) \bht{t}\right) - \left(r_B (\omega_{\calB/\calN} - \omega_{\calA/\calN})^2 \bht{r}\right)\\
\end{aligned}
$$


## Textbook problem 1.12
![[fig-p1-12_rotating_disk_telescoping_rod.png|600]]

Inertial Cartesian frame $\calN$

Rod polar frame $\calE$

Disk polar/spherical frame $\calS$

Constants: $\dot{L}$, $\dot{\theta}$, $\dot{\alpha}$, $r$

$$
\bmr = L\eht{L} + r \sht{r}
$$
$$
\begin{aligned}
\dot{\bmr} &= \dot{L}\eht{L} + L \bmo_{\calE/\calN}\times\eht{L} + r \ddtN \sht{r} \\
&= \dot{L}\eht{L} + L \dot{\theta}\eht{\theta} + r \ddtE \sht{r} + r \bmo_{\calE/\calN} \times \sht{r} \\
&= \dot{L}\eht{L} + L \dot{\theta}\eht{\theta}  + r \bmo_{\calS/\calE} \times \sht{r} + r \bmo_{\calE/\calN} \times \sht{r} \\
&= \dot{L}\eht{L} + L \dot{\theta}\eht{\theta}  + r \dot{\alpha} \sht{\alpha} + r \dot{\theta} \sht{\alpha} \\
\end{aligned}
$$
$$
\begin{aligned}
\ddot{\bmr} &= \ddtN \left( \dot{L}\eht{L} + L \dot{\theta}\eht{\theta}  + r \dot{\alpha} \sht{\alpha} + r \dot{\theta} \sht{\alpha} \right) \\
&= \ddot{L}\eht{L} + \dot{L}\dot{\theta}\eht{\theta}   +   \dot{L}\dot{\theta}\eht{\theta} + L \ddot{\theta}\eht{\theta} + L\dot{\theta}\ddtN\eht{\theta}   +    r \ddot{\alpha}\sht{\alpha} + r\dot{\alpha}\ddtN\sht{\alpha}   +    r \ddot{\theta} \sht{\alpha} + r\dot{\theta}\ddtN\sht{\alpha} \\
&= \dot{L}\dot{\theta}\eht{\theta}   +   \dot{L}\dot{\theta}\eht{\theta} + L\dot{\theta}\bmo_{\calE/\calN}\times\eht{\theta}   +   r\dot{\alpha}\bmo_{\calS/\calN}\times\sht{\alpha}   +  r\dot{\theta}\bmo_{\calS/\calN}\times\sht{\alpha} \\
&= \dot{L}\dot{\theta}\eht{\theta}   +   \dot{L}\dot{\theta}\eht{\theta} - L\dot{\theta}^2\eht{L}   -   r\dot{\alpha}(\dot{\alpha}+\dot{\theta})\sht{r}   -  r\dot{\theta}(\dot{\alpha}+\dot{\theta})\sht{r} \\
&= 2\dot{L}\dot{\theta}\eht{\theta}    - L\dot{\theta}^2\eht{L}   -   r(\dot{\alpha}+\dot{\theta})^2\sht{r} \\
\end{aligned}
$$

# Wednesday

## Textbook problem 2.10
![[fig-p2-10_rolling_cylinder_with_offset_mass.png|600]]

## Textbook problem 2.11
![[fig-p2-11_rolling_vall_inside_sphere.png|600]]

## Textbook Example 2.6

## Rocket Problem