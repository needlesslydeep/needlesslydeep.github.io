---
layout: paper
number: "003"
title: "Can You Outrun Rain?"
fields: "Physics, Meteorology"
published: 2026-08-15
status: Published
description: "A needlessly rigorous investigation into whether running keeps you drier, why the obvious answer is almost right, and when a tailwind makes physics unhelpful."
---

> *A needlessly rigorous investigation into whether running keeps you drier, why the obvious answer is almost right, and when a tailwind makes physics unhelpful.*

## Abstract

When rain begins and shelter is some fixed distance away, two intuitions immediately compete. Running reduces the time spent beneath the cloud. It also makes the rain strike harder and more horizontally, as anyone who has sprinted face-first into a storm can confirm. Which effect wins?

For steady vertical rain, the answer is unusually clean: **run**. The water landing on the top of the body decreases in inverse proportion to speed, while the water intercepted by the front depends mainly on the distance traveled and is approximately independent of speed. Running therefore cannot eliminate wetness, but it can reduce it toward a finite lower limit. Using a simplified human-shaped box in moderate rain, this paper estimates that covering 100 meters at 4.0 m/s instead of 1.4 m/s reduces intercepted water by roughly **37%**; doubling speed again yields only about another **16%**, because physics believes in diminishing returns even when your shoes do not.

Wind complicates the answer. With a headwind or substantial crosswind, moving faster is generally still better. With a sufficiently strong tailwind and little crosswind, however, an optimum can occur near the horizontal speed of the rain. Recent models incorporating measured drop distributions, changing wind, body posture, and moving limbs confirm the broad rule but preserve this narrow exception. Under most conditions, one should run; under a very particular tailwind, one should approximately travel with the rain; during thunder, one should stop optimizing equations and enter a building.

---

# 1. Introduction

It begins with a betrayal by the weather forecast.

You are outdoors. Shelter is ahead. Rain has started, and you must choose between walking with dignity or running with the unmistakable posture of someone whose phone is not waterproof.

The standard arguments are familiar:

1. **Run:** you spend less time in the rain.
2. **Walk:** running makes you collide with more drops.

Both statements are true. This is why the question has survived for at least half a century in physics journals, classrooms, television experiments, and conversations held beneath inadequate awnings. The disagreement is not caused by a lack of algebra. It is caused by a lack of agreement about what, exactly, is being modeled.

Does the rain fall vertically or blow with the wind? Are all drops identical? Is the person a rectangular box, a cylinder, a sphere, or—an ambitious recent development—a person? Does every drop stick to clothing? Does the storm remain constant during the journey? Are we minimizing water intercepted, water absorbed, discomfort, or the probability of slipping dramatically in front of strangers?

This paper begins with the simplest solvable version, then restores reality one inconvenience at a time.

The central question will be defined as follows:

> For a fixed straight-line distance to shelter, what speed minimizes the volume of rainwater intercepted by a moving person?

This definition excludes a different question: whether a runner can escape an entire moving rain cell. That depends on the size, direction, evolution, and speed of the weather system, not merely on raindrop mechanics. Here, shelter is fixed and the rain is already happening. The cloud has made its decision; we are optimizing the consequences.

---

# 2. What Rain Is Actually Doing

## 2.1 Rainfall intensity is not drop speed

Meteorologists report rainfall as a depth per unit time, such as millimeters per hour. An intensity of 10 mm/h means that a flat, unobstructed surface would accumulate a 10-millimeter layer of water in one hour if none drained away. It does **not** mean that individual drops fall at 10 millimeters per hour. At that speed, rain would arrive several days after the forecast.

Drop speed depends strongly on drop size. The American Meteorological Society describes typical raindrops as approximately 1–2 mm in diameter and notes fall speeds spanning roughly 2–12 m/s depending on size and altitude<sup>[1]</sup>. NASA gives about 10 m/s as the upper terminal speed of the largest drops in still air<sup>[2]</sup>. The U.S. Geological Survey lists representative fall speeds of approximately 4.8 m/s for light rain, 5.7 m/s for moderate rain, and 6.7 m/s for heavy rain<sup>[3]</sup>.

Real rain is a population, not a regiment. A storm contains a distribution of drop sizes, and those sizes vary with formation mechanism, collision, breakup, evaporation, wind shear, and location within the storm<sup>[4]</sup>. Small drops are nearly spherical; larger ones flatten underneath, and sufficiently large drops deform and break apart. The classic teardrop-shaped raindrop is therefore mostly a triumph of illustration over fluid mechanics.

For the first model, we compress this unruly population into two bulk quantities:

- $I$: rainfall intensity, expressed as a water depth per second;
- $q$: an effective vertical fall speed of the drops.

If the air contains a volume fraction $\chi$ of liquid water, then for vertical rain:

$$
I = \chi q
$$

or

$$
\chi = \frac{I}{q}.
$$

This relation is the bridge between what a rain gauge measures and how much water a moving body encounters.

## 2.2 Terminal velocity, briefly

A falling drop accelerates until gravity is balanced by aerodynamic drag and buoyancy. It then travels near its terminal velocity. Because drag, deformation, and internal circulation change with drop diameter, there is no single "speed of rain." Tiny drizzle droplets descend slowly; large drops fall faster but eventually become unstable rather than continuing to grow into aquatic cannonballs.

The distinction matters because vertical fall speed barely changes the rain landing on one's head for a given measured intensity, but it changes the concentration of water suspended in the air. At the same rainfall rate, slower drops require more water to be present per cubic meter of air. A person moving horizontally through that volume therefore intercepts more water from the front.

Meteorology has entered the problem before we have even turned the pedestrian into a box. This is considered progress.

---

# 3. The Rectangular Human

Physics often begins by replacing a complicated object with a sphere. Unfortunately, a sphere has no obvious front, and the front is rather important when running into rain. We will instead model a person as a rectangular prism with:

- horizontal top area $A_t$,
- frontal area $A_f$,
- side area $A_s$,
- forward speed $u$,
- fixed distance to shelter $D$.

The body remains upright, rigid, and does not swing its limbs. This is not a flattering model of a human being, but it is an excellent model of a wardrobe in a hurry.

## 3.1 The water from above

The journey lasts

$$
t = \frac{D}{u}.
$$

Rain falls onto the horizontal area $A_t$ at volumetric rate $IA_t$. The total water striking the top is therefore

$$
V_{top} = IA_t t = \frac{IA_tD}{u}.
$$

This term is inversely proportional to speed. Double your speed and the top of the model receives half as much water. Stand still and the journey takes forever, which is mathematically elegant and personally damp.

## 3.2 The water from the front

In still air, the person sweeps a horizontal volume

$$
V_{swept} = A_fD.
$$

The fraction of that volume occupied by liquid water is $\chi = I/q$, so the water intercepted by the front is

$$
V_{front} = \chi A_fD = \frac{IA_fD}{q}.
$$

There is no $u$ in this expression.

Running causes more drops to strike the front each second, but it reduces the number of seconds by exactly the compensating factor. Over a fixed distance, the frontal surface sweeps through the same rain-filled volume whether it travels slowly or quickly. This cancellation is the central result of the elementary problem.

Combining the two contributions gives

$$
\boxed{V(u) = ID\left(\frac{A_t}{u}+\frac{A_f}{q}\right)}.
$$

The first term shrinks with speed. The second is a speed-independent floor. Therefore:

> In steady vertical rain, for a rigid body traveling a fixed distance, faster is always drier—but infinitely fast is not infinitely dry.

You cannot avoid plowing through the column of drops already occupying the space between you and shelter. Speed merely prevents additional rain from landing on top while you do it.

## 3.3 Why the rain looks more horizontal when you run

In still air, rain falls vertically at speed $q$ in the ground frame. In the runner's frame, the relative velocity is

$$
\vec{v}_{rel}=(-u,0,-q).
$$

The apparent angle $\theta$ away from vertical satisfies

$$
\tan\theta = \frac{u}{q}.
$$

For $q=6$ m/s, rain appears about 13° from vertical to a person walking at 1.4 m/s, about 34° to a runner at 4.0 m/s, and about 53° to a heroic but short-lived sprinter at 8.0 m/s. The rain really does strike more horizontally. It simply does not produce more total frontal water over the completed route.

The sensation of "harder rain" is also real: relative impact speed increases from $q$ to $\sqrt{q^2+u^2}$. Your face is not misreporting the data; it is merely reporting a different variable.

---

# 4. A Worked Example

Consider a 100-meter route through rain falling at 10 mm/h. Use the following deliberately simplified parameters:

<table class="paper-table paper-table-small">
  <thead>
    <tr>
      <th>Parameter</th>
      <th class="numeric">Value</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Distance, $D$</td><td class="numeric">100 m</td></tr>
    <tr><td>Rainfall intensity, $I$</td><td class="numeric">10 mm/h</td></tr>
    <tr><td>Effective drop fall speed, $q$</td><td class="numeric">6.0 m/s</td></tr>
    <tr><td>Top projected area, $A_t$</td><td class="numeric">0.15 m²</td></tr>
    <tr><td>Front projected area, $A_f$</td><td class="numeric">0.50 m²</td></tr>
  </tbody>
</table>

The rainfall intensity in SI units is

$$
I=\frac{0.010\ \text{m}}{3600\ \text{s}}=2.78\times10^{-6}\ \text{m/s}.
$$

Applying the equation from Section 3 gives:

<table class="paper-table">
  <thead>
    <tr>
      <th>Motion</th>
      <th class="numeric">Speed</th>
      <th class="numeric">Time outside</th>
      <th class="numeric">Top water</th>
      <th class="numeric">Front water</th>
      <th class="numeric">Total</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Walk</td><td class="numeric">1.4 m/s</td><td class="numeric">71.4 s</td><td class="numeric">29.8 mL</td><td class="numeric">23.1 mL</td><td class="numeric"><strong>52.9 mL</strong></td></tr>
    <tr><td>Run</td><td class="numeric">4.0 m/s</td><td class="numeric">25.0 s</td><td class="numeric">10.4 mL</td><td class="numeric">23.1 mL</td><td class="numeric"><strong>33.6 mL</strong></td></tr>
    <tr><td>Sprint</td><td class="numeric">8.0 m/s</td><td class="numeric">12.5 s</td><td class="numeric">5.2 mL</td><td class="numeric">23.1 mL</td><td class="numeric"><strong>28.4 mL</strong></td></tr>
  </tbody>
</table>

In this example, running rather than walking reduces intercepted water by approximately **37%**. Sprinting at twice the running speed saves only another **16%** relative to running. The immutable frontal term increasingly dominates, so each additional unit of speed buys less dryness than the previous one.

These numbers are illustrations, not universal predictions. Human projected area, posture, clothing, rainfall rate, and drop distribution all vary. The robust feature is the shape of the result: a rapid initial benefit followed by a finite asymptote.

This explains why the useful practical instruction is "run" rather than "qualify for the Olympic final."

---

# 5. Adding Wind: Where the Simple Answer Develops Terms and Conditions

Let the horizontal wind component along the route be $w$, positive when it blows from behind. Let $c$ be the crosswind component, and let rain fall vertically through the moving air at speed $q$. The rain velocity in the ground frame is then

$$
\vec{v}_{rain}=(w,c,-q),
$$

while the person's velocity is

$$
\vec{u}=(u,0,0).
$$

The apparent rain velocity is their difference:

$$
\vec{v}_{rel}=(w-u,c,-q).
$$

For the rectangular model, the total intercepted volume becomes

$$
\boxed{V(u)=\frac{ID}{u}\left[A_t+\frac{A_f|u-w|}{q}+\frac{A_s|c|}{q}\right]}.
$$

This compact expression contains several different weather reports.

## 5.1 No wind

Setting $w=c=0$ recovers the earlier result:

$$
V(u)=ID\left(\frac{A_t}{u}+\frac{A_f}{q}\right).
$$

Run faster.

## 5.2 Headwind

For a headwind, $w<0$. The rain's horizontal speed toward the front increases, but the time-dependent top and wind contributions still decrease as $u$ increases. In the rectangular model, faster remains better. It will not feel better, which is a separate and apparently more important complaint.

## 5.3 Crosswind

A crosswind wets the side at a rate proportional to $|c|$. Because the route time is $D/u$, the side contribution decreases with forward speed. Crosswind therefore strengthens the case for running. It also makes choosing the driest shoulder a matter of meteorological strategy, a sentence no one expected to need.

## 5.4 Tailwind

A tailwind is the interesting case. If $u=w$ and crosswind is negligible, the rain has no apparent along-route component. It appears to fall vertically, so neither the chest nor back intercepts it in the box model.

Should one run faster than the tailwind? For $u>w$ and $c=0$,

$$
V(u)=ID\left[\frac{A_f}{q}+\frac{A_t-A_fw/q}{u}\right].
$$

The sign of the numerator in the final term decides the strategy:

- If $w < qA_t/A_f$, faster remains better.
- If $w > qA_t/A_f$, speeding beyond $w$ increases wetness, and the optimum is $u=w$.

Using the example geometry from Section 4, the threshold is

$$
w_{threshold}=q\frac{A_t}{A_f}=6\times\frac{0.15}{0.50}=1.8\ \text{m/s}.
$$

Thus even this extremely simple model does **not** say that any tailwind creates an optimum. It requires a tailwind strong enough relative to drop fall speed and body geometry. A crosswind can weaken or remove the optimum by adding a time-dependent side penalty.

This conclusion agrees with the general analyses by Ehrmann and Blachowicz and by Bocci: body shape, orientation, wind direction, and wind magnitude determine whether a finite optimum exists<sup>[5][6]</sup>. The famous instruction "match the tailwind" is not wrong; it is merely a special case wearing the costume of a universal law.

---

# 6. The Human Body Objects to Being a Box

Real people lean forward when running. Their arms bend and swing. Their legs separate. Their head is, regrettably for the algebra, attached above the torso rather than machined into a flat roof. These changes alter the projected area exposed to the apparent rain.

Two modern numerical studies have attacked this problem with increasing realism.

## 6.1 Real rain, a simplified human

Zaegel and colleagues modeled a human-like assembly moving through measured rainfall events, incorporating time-varying wind as well as observed distributions of drop sizes and velocities<sup>[7]</sup>. They tested 11 rain events over three 1-kilometer routes, producing 33 scenarios. Their comparison used:

- walking at 4 km/h,
- running at 12 km/h,
- sprinting at 18 km/h.

In all 33 modeled scenarios, running intercepted less water than walking. The reduction reached **86%**, and exceeded 50% in more than two-thirds of the cases. Sprinting was far less decisive: nine scenarios had an optimum below 18 km/h, meaning the sprint was actually wetter, and most of the remaining gains were modest.

This is a valuable result, but it should not be mistaken for 33 people being weighed in wet clothing. It was a numerical study driven by real meteorological measurements. Its strength is atmospheric realism; its simplified body translated rigidly and did not reproduce the changing geometry of gait.

## 6.2 A moving, articulated human

In 2026, Crespi and Manini introduced a model made from spheres, boxes, and capsule-shaped limbs whose body parts move during walking and running<sup>[8]</sup>. A ray-tracing-like calculation evaluated which drops would be intercepted and which would be shielded by other body parts. Physics had finally upgraded the pedestrian from furniture to a low-budget animated character.

Their projected areas illustrate why gait matters:

<table class="paper-table paper-table-small">
  <thead>
    <tr>
      <th>Gait model</th>
      <th class="numeric">Front projection</th>
      <th class="numeric">Side projection</th>
      <th class="numeric">Top projection</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Walking</td><td class="numeric">0.493 m²</td><td class="numeric">0.297 m²</td><td class="numeric">0.140 m²</td></tr>
    <tr><td>Running</td><td class="numeric">0.429 m²</td><td class="numeric">0.359 m²</td><td class="numeric">0.200 m²</td></tr>
  </tbody>
</table>

The running model presents less area from the front but more from above, largely because of its forward lean, bent arms, and wider leg motion. Under no-wind conditions, the study found that walking collected approximately **37% more water than running**. Across most wind conditions, running was preferable.

But the exception survived.

When the tailwind was close to the person's speed and crosswind was small, the apparent rain became nearly vertical. The walking posture then benefited from its smaller top projection. In a narrow region near a tailwind of about $0.7q$ and crosswind below about $0.2q$, walking collected up to approximately **7% less water** than running. The study also found that a nontrivial optimum could arise once tailwind exceeded roughly 20% of the drop fall speed; crosswind raised that optimum and could eliminate it entirely.

The practical conclusion is not that one should estimate $0.7q$ from the nearest raindrop and adopt a calibrated stroll. Drop populations and wind fluctuate, and ordinary pedestrians do not carry disdrometers. The conclusion is that the simple rule is impressively robust, but not a theorem about every possible storm and posture.

---

# 7. Intercepted Water Is Not the Same as Wetness

Nearly every neat derivation quietly assumes that each intercepted drop is completely absorbed. Clothing is less cooperative.

A drop may splash, bounce, break, run off, remain on an outer waterproof layer, or transfer only part of its mass to fabric. The retained fraction can depend on impact speed, angle, material, existing saturation, surface treatment, and drop size. Patriota, Bertuola, and Peixoto showed that introducing even a simple speed-dependent absorption fraction can produce a finite optimum in vertical rain where the traditional complete-absorption model predicts only "faster is better"<sup>[9]</sup>.

There are also effects omitted from nearly all ideal models:

- shoe splash and water kicked onto the legs;
- puddles, which are rain that has abandoned ballistics for ambush;
- evaporation from warm or breathable clothing;
- water transferred between garments and skin;
- shielding by hair, hats, backpacks, and umbrellas;
- a rain rate that changes while the route is being completed.

This means that "intercepted water," "water retained by clothing," and "how wet a person feels" are different observables. Physics can calculate the first cleanly. Textile science complicates the second. The third is willing to depend on your socks.

Still, these complications do not reverse the most reliable reason to run: in typical rain and wind, less time outdoors means less opportunity for water to arrive on surfaces exposed from above and from the side.

---

# 8. Can You Literally Outrun a Raindrop?

Not in the useful sense.

A fast human can exceed the vertical speed of some small droplets in numerical magnitude, but the runner and drop are moving mostly in perpendicular directions. Winning a 100-meter race against something descending toward the pavement is not a well-defined victory. The drop is not going to the shelter.

Nor does exceeding a drop's horizontal wind speed make the rain disappear. It changes which surface the drop strikes. At a matching tailwind, rain may cease hitting the front, but it continues to land on the top. At higher speed, the runner begins encountering it from ahead again.

One can sometimes outrun a localized shower or move out of a rain shaft, but that is a different optimization problem involving the storm's spatial boundary and evolution. If rainfall ends naturally before a long journey is complete, waiting under cover may beat every running speed. The elementary fixed-distance model assumes constant rain precisely because clouds otherwise acquire a vote.

So the strict answer is:

> You cannot outrun rain as a substance. You can reduce the time and volume over which your path intersects it.

Less cinematic, perhaps, but substantially more accurate.

---

# 9. The Practical Decision Rule

For anyone unwilling to solve a vector-flux problem on the sidewalk, the research reduces to the following hierarchy:

1. **If there is no strong tailwind, run at a safe pace.** This covers vertical rain, headwind, and most crosswind conditions.
2. **Expect diminishing returns.** Running usually helps substantially; sprinting often helps only a little more and may not help at all in unusual tailwind conditions.
3. **With a strong, steady tailwind and little crosswind, matching the wind can be near-optimal.** In practice, the required measurements and changing storm make this more scientific curiosity than commuting protocol.
4. **Use an umbrella or waterproof layer if available.** Altering the exposed area and absorption is generally more effective than fine-tuning speed.
5. **Do not let wetness optimization overrule safety.** Slippery pavement, traffic, poor visibility, hail, flash flooding, and lightning are not small correction terms.

The National Weather Service states that there is no safe place outdoors when thunderstorms are nearby and advises entering a substantial building or hard-topped vehicle when thunder is heard<sup>[10]</sup>. In that situation, run only as needed to reach proper shelter safely. The relevant question is no longer how many milliliters reached your jacket.

---

# 10. Conclusion

We can now answer the original question.

**Can you outrun rain?**

Not completely. For a fixed route through steady vertical rain, the front of your body must sweep through a fixed volume of rain-filled air. That contribution does not vanish as speed increases. You are not escaping every drop; you are choosing how quickly to complete the unavoidable introductions.

But **running usually keeps you drier than walking**. The water arriving from above, and much of the water arriving from crosswind, accumulates with time. Running reduces that exposure. In the worked 100-meter example, increasing speed from 1.4 to 4.0 m/s reduced intercepted water from about 53 to 34 milliliters, while sprinting produced a much smaller additional benefit.

The qualifier is wind. A sufficiently strong tailwind with negligible crosswind can create an optimum near the rain's horizontal speed. Realistic models preserve this exception, and the most recent articulated-body simulation even finds a narrow range in which walking can beat running by several percent because the walking posture presents less area to nearly vertical apparent rain.

Under most skies, however, the result remains wonderfully ordinary:

**Run, but do not expect miracles.**

The universe will permit you to become less wet. It will not permit you to negotiate the frontal term.

---

# References

1. American Meteorological Society. *Glossary of Meteorology: Raindrop.* [glossary.ametsoc.org](https://glossary.ametsoc.org/wiki/raindrop/)
2. NASA Global Precipitation Measurement Mission. *How Fast Do Raindrops Fall?* [gpm.nasa.gov](https://gpm.nasa.gov/resources/faq/how-fast-do-raindrops-fall)
3. U.S. Geological Survey. *Precipitation and the Water Cycle — Precipitation Size and Speed.* [usgs.gov](https://www.usgs.gov/water-science-school/science/precipitation-and-water-cycle)
4. American Meteorological Society. *Glossary of Meteorology: Raindrop-Size Distribution.* [glossary.ametsoc.org](https://glossary.ametsoc.org/wiki/raindrop-size-distribution/)
5. Ehrmann, A., Blachowicz, T. "Walking or Running in the Rain—A Simple Derivation of a General Solution." *European Journal of Physics* 32(2), 2011, 355–361. [doi.org/10.1088/0143-0807/32/2/008](https://doi.org/10.1088/0143-0807/32/2/008)
6. Bocci, F. "Whether or Not to Run in the Rain." *European Journal of Physics* 33(5), 2012, 1321–1332. [doi.org/10.1088/0143-0807/33/5/1321](https://doi.org/10.1088/0143-0807/33/5/1321)
7. Zaegel, M., Vehils-Vinals, M., Guastalla, H., Benabou, B., Gires, A. "Should You Walk, Run or Sprint in the Rain to Get Less Wet?" *European Journal of Physics* 45, 2024, 025802. [doi.org/10.1088/1361-6404/ad06bf](https://doi.org/10.1088/1361-6404/ad06bf)
8. Crespi, C. A., Manini, N. "Optimal Speed in Rain: A Numerical Model of a Dynamically Deforming Human Body." *Physics Open* 26, 2026, 100381. [doi.org/10.1016/j.physo.2026.100381](https://doi.org/10.1016/j.physo.2026.100381)
9. Patriota, H., Bertuola, A. C., Peixoto, P. "Walking or Running in the Rain: A Nontrivial Problem." *Revista Brasileira de Ensino de Física* 35(3), 2013, 3316. [doi.org/10.1590/S1806-11172013000300016](https://doi.org/10.1590/S1806-11172013000300016)
10. U.S. National Weather Service. *Lightning Safety.* [weather.gov](https://www.weather.gov/safety/lightning-safety)

---

# Appendix A — General Box-Model Equation

For rainfall intensity $I$, effective vertical drop speed $q$, travel distance $D$, body speed $u$, tailwind component $w$, crosswind component $c$, and projected body areas $A_t$, $A_f$, and $A_s$:

$$
V(u)=\frac{ID}{u}\left[A_t+\frac{A_f|u-w|}{q}+\frac{A_s|c|}{q}\right].
$$

The model assumes:

- uniform, steady rain over the entire route;
- a fixed drop fall speed;
- constant wind;
- a straight, horizontal path;
- constant body speed;
- a rigid rectangular body aligned with the route;
- complete interception and retention of every geometrically incident drop;
- no splash, evaporation, shielding, or puddles.

The equation is therefore not reality. It is reality after being asked to remain still long enough for calculus.

# Appendix B — Limiting Cases

<table class="paper-table paper-table-small">
  <thead>
    <tr>
      <th>Condition</th>
      <th>Box-model result</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Vertical rain, $w=c=0$</td><td>Faster is always drier; frontal water is speed-independent.</td></tr>
    <tr><td>Headwind, $w&lt;0$</td><td>Faster is always drier.</td></tr>
    <tr><td>Pure crosswind, $c\neq0$</td><td>Faster reduces top and side exposure.</td></tr>
    <tr><td>Weak tailwind</td><td>Faster remains better.</td></tr>
    <tr><td>Strong tailwind, negligible crosswind</td><td>A finite optimum may occur at $u=w$.</td></tr>
    <tr><td>$u\rightarrow\infty$, no wind</td><td>$V\rightarrow IDA_f/q$, not zero.</td></tr>
  </tbody>
</table>

---

## Author's Note

This paper was prepared by combining published research in physics and meteorology with original calculations based on a transparent rectangular-body model.

No author was deliberately left outside in the rain for validation. The articulated digital humans, however, were shown no such mercy.
