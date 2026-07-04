---
layout: paper
number: "002"
title: "How Heavy Is the Internet?"
fields: "Physics · Computer Science"
published: 2026-07-02
status: Published
description: "A Quantitative Investigation into the Physical Mass of Information, Energy, Digital Storage, and Global Internet Infrastructure"
---

> *A Quantitative Investigation into the Physical Mass of Information, Energy, Digital Storage, and Global Internet Infrastructure*

## Abstract

The Internet is routinely described as something that exists "in the cloud" — a phrase that, on reflection, is one of the more effective pieces of misdirection in modern language. Every webpage, video call, and poorly-timed group chat notification ultimately depends on matter: silicon, copper, magnetized rust, and a genuinely alarming number of diesel generators. This raises a question that sounds like a joke and turns out not to be one: how heavy is the Internet?

The honest answer is that "the Internet" is not a single physical object, so it does not have a single weight. Depending on what is being measured — information itself, the energy required to represent that information, the storage media holding it, or the global infrastructure running it — the resulting mass spans more than **forty orders of magnitude**. This paper evaluates all four interpretations using Landauer's principle, mass–energy equivalence, manufacturer datasheets, and industry infrastructure statistics, and shows that each answer is correct, provided nobody asks a follow-up question.

---

# 1. Introduction

Every second, the Internet moves an amount of data that would have seemed fictional twenty years ago. Global Internet traffic reached roughly **7.3 zettabytes in 2024** alone, combining fixed and mobile traffic — and it grew again the following year<sup>[1]</sup>. None of this is remotely tangible. You cannot hold a zettabyte, and if you could, you would almost certainly regret it.

And yet the intuition that "the Internet must weigh *something*" is not wrong — it is just underspecified. This paper takes that intuition seriously and interrogates it properly, in the same spirit as our previous investigation into intestinal gas: absurd question, real methodology, no shortcuts.

The infamous starting point for this line of inquiry is a 2006 back-of-the-envelope calculation by physicist Russell Seitz, who estimated the mass of the Internet's active electrons at around 50 grams — "about the weight of a strawberry"<sup>[2]</sup>. The comparison is charming and has been repeated for nearly two decades. It is also, as this paper will show, measuring something considerably more specific than "the Internet," and considerably lighter than the buildings that house it.

We define four independent physical systems, each a legitimate reading of the original question, and estimate the mass of each.

---

# 2. Defining the Internet

Before any calculation can mean anything, the system being weighed has to be defined. Asking "how heavy is the Internet" without saying which Internet is a bit like asking how heavy "transportation" is — the answer depends entirely on whether you mean a bicycle or the global shipping fleet.

This paper considers four models:

1. **Information** — the Internet as an abstract collection of bits, independent of any physical medium.
2. **Energy** — the physical energy required to represent that information, converted to mass via $E = mc^2$.
3. **Storage** — the physical media (HDDs, SSDs) required to persist the world's digital information.
4. **Infrastructure** — the complete physical apparatus that makes the Internet operational: servers, network equipment, power systems, and the buildings that contain them.

Each model answers a different question. None of them is "more correct" than the others — they simply describe different systems that all happen to share the same casual name.

---

# 3. Model I — The Internet as Information

A bit is not a particle. It is an abstract logical state — a distinction between two possibilities — that happens to require *some* physical system to represent it, but is not identical to that system. The same photograph can survive a hard-drive failure, a phone upgrade, and three separate cloud migrations without losing a single bit of what it depicts, which is either reassuring or mildly existential, depending on your relationship with permanence.

Because information has no physical medium built into its definition, it has no intrinsic rest mass. Under this model, the Internet — understood purely as the pattern of ones and zeros — weighs precisely nothing, in the same sense that a melody weighs nothing independent of the instrument playing it.

This is a clean answer, but not a useful one for anyone hoping to put the Internet on a scale. It does, however, motivate the next model directly: information may not have mass, but the *physical states* used to represent it obey the ordinary laws of thermodynamics, and those laws do not hand out anything for free.

---

# 4. Model II — The Internet as Energy

## 4.1 Information requires energy

Every storage technology in use today represents a bit as a distinguishable physical state: a charge held in a DRAM capacitor **(notoriously high-maintenance, and in need of refreshing roughly every 64 milliseconds or it forgets everything, like a very expensive goldfish)**, electrons trapped in a flash memory's floating gate, the orientation of a magnetic domain on a spinning platter. Creating and maintaining a distinguishable state is not free. In 1961, Rolf Landauer showed that erasing one bit of information irreversibly requires a minimum amount of dissipated energy:

$$E_{min} = kT\ln 2$$

where $k$ is the Boltzmann constant and $T$ is the absolute temperature of the system. This is not an engineering limitation — it is a thermodynamic floor. Real hardware sits far above it, but nothing can sit below it<sup>[3]</sup>. The principle has since been confirmed experimentally, including in single-bit reset operations<sup>[4]</sup>.

## 4.2 From energy to mass

Einstein's mass–energy equivalence gives every quantity of energy an equivalent mass:

$$m = \frac{E}{c^2}$$

Substituting Landauer's minimum energy gives the theoretical minimum mass-equivalent of a single erased bit:

$$m_{bit} = \frac{kT\ln 2}{c^2}$$

At room temperature ($T = 300\text{ K}$), this evaluates to:

$$m_{bit} \approx 3.19 \times 10^{-38}\ \text{kg}$$

This is, for context, about twenty-five orders of magnitude lighter than a single electron. It is not a quantity anyone will ever weigh directly, no matter how patient or well-funded.

## 4.3 Scaling to global data

To estimate the Landauer-limit mass of *all* stored information, we take a commonly cited estimate of the world's digital storage volume — roughly **175 zettabytes**, per IDC's Global DataSphere projections<sup>[5]</sup> — and convert it to bits:

$$N_{bits} = 175 \times 10^{21}\ \text{bytes} \times 8 = 1.4 \times 10^{24}\ \text{bits}$$

The theoretical minimum equivalent mass of the entire global datasphere is then:

$$M_{internet} = N_{bits} \times m_{bit} \approx 4.5 \times 10^{-14}\ \text{kg} \approx 45\ \text{picograms}$$

Forty-five picograms is, by a comfortable margin of about six orders of magnitude, lighter than a single grain of fine sand. Seitz's strawberry, by comparison, is heavier by roughly *thirty-six* orders of magnitude — which is not a criticism of Seitz's arithmetic so much as a reminder that "electrons in motion" and "the thermodynamic minimum of information itself" are not the same measurement, even though both technically answer the question "how much does the Internet weigh."

## 4.4 Limitations of the model

This figure represents an idealized lower bound, not an operating reality. Real memory devices dissipate vastly more energy than the Landauer limit due to resistive losses, leakage current, and the simple fact that engineers optimize for speed and reliability, not thermodynamic elegance. This model tells us the smallest the Internet could possibly weigh if physics ran a considerably tighter ship. It says nothing about the hardware actually required to store the data — which is the subject of the next model.

---

# 5. Model III — The Internet as Digital Storage

## 5.1 Mass is a property of the device, not the data

An empty 24 TB hard drive and a full 24 TB hard drive weigh the same, to any precision achievable outside a national metrology laboratory. Writing a wedding album to an SSD does not make the SSD heavier in any practical sense — the mass difference predicted by Model II is many orders of magnitude below what any scale on Earth could register. So the meaningful question is not "how much do the bits weigh," but "how much does the hardware required to hold them weigh."

## 5.2 Representative storage devices

Rather than relying on a generic industry average, this paper uses two enterprise devices with manufacturer-published, verifiable specifications, representing the two dominant storage technologies.

<table class="paper-table">
  <thead>
    <tr>
      <th>Manufacturer</th>
      <th>Model</th>
      <th>Technology</th>
      <th class="numeric">Capacity</th>
      <th class="numeric">Mass</th>
      <th class="numeric">Density</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Seagate</td>
      <td>Exos X24</td>
      <td>HDD</td>
      <td class="numeric">24 TB</td>
      <td class="numeric">685 g</td>
      <td class="numeric">28.5 g/TB</td>
    </tr>
    <tr>
      <td>Kioxia</td>
      <td>CM7-R (2.5")</td>
      <td>SSD</td>
      <td class="numeric">30.72 TB</td>
      <td class="numeric">130 g</td>
      <td class="numeric">4.23 g/TB</td>
    </tr>
  </tbody>
</table>

The nearly seven-fold gap between the two is not a rounding error — it reflects a genuine architectural difference. An HDD is, at its core, a small precision-engineered machine with spinning platters and a mechanical actuator arm; an SSD is a slab of flash chips with comparatively little to it besides silicon and a controller. Solid-state storage is, quite literally, less *stuff* per terabyte.

## 5.3 Global storage requirement

Using the same estimate of global digital storage as Section 4.3 — approximately 175 ZB, or $1.75 \times 10^{11}\ \text{TB}$ — the total mass of physical media required to store it is:

$$M_{storage} = S \times D$$

Applying the density range from Table 1:

$$M_{storage,\ low} = 1.75 \times 10^{11}\ \text{TB} \times 4.23\ \text{g/TB} \approx 7.4 \times 10^{8}\ \text{kg} \approx 0.74\ \text{Mt}$$

$$M_{storage,\ high} = 1.75 \times 10^{11}\ \text{TB} \times 28.5\ \text{g/TB} \approx 5.0 \times 10^{9}\ \text{kg} \approx 5.0\ \text{Mt}$$

In other words: if humanity stored the entirety of its data on enterprise SSDs, the total media would weigh somewhere around **0.7 million metric tons**. If it were all stored on HDDs instead, that figure climbs to roughly **5 million metric tons** — a sevenfold difference driven entirely by which side of the storage-technology debate manufacturers happened to win in a given data center.

Neither figure includes the servers, shelving, cabling, or power systems required to actually operate that storage — that is the subject of the next, considerably heavier, model.

---

# 6. Model IV — The Internet as Global Infrastructure

## 6.1 A note on methodology

It is worth being explicit about something the previous section glossed over: the "storage" estimated in Section 5.3 is a *data-volume-driven* calculation — how much media is needed to hold all the world's data, full stop, regardless of where it lives. The estimate in this section is a *power-driven* calculation — how much storage hardware is physically installed inside data centers, inferred from data centers' share of global electricity use. These are related but not identical quantities (plenty of the world's data lives outside data centers, on personal devices, and plenty of data-center storage capacity sits unused as overhead). Treating them as interchangeable would be sloppy, so this paper doesn't, **however tempting the shortcut**.

## 6.2 From electricity to mass

The International Energy Agency estimates that data centers consumed approximately **415 TWh in 2024**, about 1.5% of global electricity demand<sup>[6]</sup>. On average, servers account for roughly 60% of that consumption, storage for about 5%, networking equipment for up to 5%, and cooling for anywhere between 7% and over 30% depending on facility efficiency<sup>[6]</sup>. The Uptime Institute separately reports a global average Power Usage Effectiveness (PUE) of **1.56** — meaning that for every kilowatt actually doing computational work, another 0.56 kilowatts goes to cooling, power conversion, and other overhead<sup>[7]</sup> — **the electrical equivalent of a company where more than a third of the staff exists purely to keep the other two-thirds from overheating**.

Converting 415 TWh/year into average power:

$$P_{total} = \frac{415 \times 10^{12}\ \text{Wh}}{8760\ \text{h}} \approx 47.4\ \text{GW}$$

$$P_{IT} = \frac{47.4\ \text{GW}}{1.56} \approx 30.4\ \text{GW}$$

Roughly 30 GW is doing the actual computing; the remaining ~17 GW keeps that computing from overheating, browning out, or catching fire.

## 6.3 Mass by category

Combining these power allocations with representative equipment masses — enterprise servers (16–37 kg, ~600–750 W)<sup>[8]</sup>, switches and routers<sup>[9,10]</sup>, standard 42U racks (125–161 kg empty)<sup>[11]</sup>, UPS systems (~2.1 t/MW)<sup>[12]</sup>, backup batteries<sup>[13]</sup>, diesel generators (~8–12 t/MW)<sup>[14]</sup>, and chillers (~3 t/MW)<sup>[15]</sup> — produces the following order-of-magnitude estimate for hardware installed in data centers worldwide.

<table class="paper-table">
  <thead>
    <tr>
      <th>Category</th>
      <th>Estimated global mass</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Servers</td><td>0.52 – 1.54 Mt</td></tr>
    <tr><td>Storage hardware (installed base)</td><td>0.02 – 0.24 Mt</td></tr>
    <tr><td>Network equipment</td><td>0.05 – 0.12 Mt</td></tr>
    <tr><td>Racks (empty)</td><td>0.47 – 0.69 Mt</td></tr>
    <tr><td><strong>IT hardware subtotal</strong></td><td><strong>1.1 – 2.6 Mt</strong></td></tr>
    <tr><td>Support systems (UPS, batteries, generators, chillers)</td><td>0.5 – 0.9 Mt</td></tr>
    <tr><td>Buildings and structural material</td><td>11.8 – 35.6 Mt</td></tr>
    <tr><td><strong>Total infrastructure</strong></td><td><strong>~13 – 39 Mt</strong></td></tr>
  </tbody>
</table>

**Notably, the racks alone weigh nearly as much as all the networking equipment combined — a reminder that a data center is, structurally speaking, mostly furniture.**

## 6.4 Where the buildings come from

The building estimate deserves a word of explanation, since it dominates the total by an order of magnitude. Using an industry rule of thumb of roughly 780 m² of total facility area per megawatt of IT load<sup>[16]</sup>, the ~30.4 GW of global IT capacity implies approximately **23.7 million square meters** of data center floor space. Applying a structural material intensity of 500–1,500 kg/m² — a range drawn from a survey of 200 real building structures, and if anything a conservative one for facilities built to hold rows of dense equipment racks<sup>[17]</sup> — yields the building mass range shown above.

It is, in other words, mostly concrete and steel. The Internet, weighed as infrastructure, is a construction project that happens to also process email.

## 6.5 What this model leaves out

This estimate does not include the global fiber-optic network — hundreds of thousands of kilometers of terrestrial and submarine cable — nor consumer-side hardware such as phones, laptops, routers, or cell towers **— collectively a very large number of very small objects, which is precisely the kind of category that ruins otherwise tidy back-of-envelope math**. No sufficiently reliable global mass figures for these categories were available at the rigor this paper otherwise insists on, so rather than guess, we've left them out and flagged it here, in the finest tradition of admitting what you don't know.

---

# 7. Comparison of the Four Models

<table class="paper-table">
  <thead>
    <tr>
      <th>Model</th>
      <th>System measured</th>
      <th>Estimated mass</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>I — Information</td><td>Abstract bits</td><td>No intrinsic rest mass</td></tr>
    <tr><td>II — Energy (Landauer limit)</td><td>Thermodynamic minimum to represent global data</td><td>≈ 45 picograms</td></tr>
    <tr><td>III — Digital storage</td><td>Physical media for all world data</td><td>≈ 0.7 – 5 million metric tons</td></tr>
    <tr><td>IV — Global infrastructure</td><td>Servers, networking, power, and buildings</td><td>≈ 13 – 39 million metric tons</td></tr>
  </tbody>
</table>

The spread between Model II and Model IV is roughly **forty-five orders of magnitude** — the numerical equivalent of comparing a single picogram to the mass of a small mountain range. Both numbers are correctly derived. Neither is wrong. They are simply not measuring the same thing, which is the entire point of this paper.

For a sense of physical scale: the total infrastructure estimate from Model IV is comparable to roughly **two to seven Great Pyramids of Giza**, built not from limestone blocks but from server racks, chillers, and diesel generators, and requiring considerably more air conditioning to maintain.

---

# 8. Discussion

The apparent contradiction between these four estimates is, on inspection, not a contradiction at all — **much like "transportation" can mean a bicycle or a supertanker without either definition being wrong**. Information, energy, storage hardware, and infrastructure are related concepts, but they are not interchangeable systems, and conflating them is precisely how a defensible physics estimate (Seitz's fifty grams) and an equally defensible infrastructure estimate (tens of millions of tons) end up sounding like they disagree, when in fact they're answering different questions asked in the same words.

It's also worth separating physical mass from environmental impact, since the two are easy to confuse and measure very different things. A heavier data center is not automatically a more harmful one — electricity consumption, embodied carbon in construction, and equipment lifecycle matter considerably more than tonnage. On that front, the numbers are less abstract: data centers accounted for roughly 415 TWh of electricity in 2024 and are projected to approach 945 TWh by 2030<sup>[6]</sup>, while the world generated **62 million metric tons of e-waste in 2022**, of which only about 22% was documented as formally collected and recycled<sup>[18]</sup>. If the goal is to understand the Internet's real-world footprint rather than satisfy curiosity about its weight, those are the numbers that matter — mass just happens to be the more entertaining way in.

---

# 9. Conclusion

The Internet does not have a weight. It has several, depending entirely on what is being weighed. As pure information, it has no intrinsic mass at all. As the thermodynamic minimum required to represent that information, it weighs about as much as a few dozen picograms — considerably less than the strawberry it's often compared to. As the physical media required to store the world's data, it weighs somewhere in the neighborhood of a million metric tons. As the complete infrastructure that keeps it running — racks, chillers, generators, and the buildings around all of it — it weighs tens of millions of metric tons, several Great Pyramids' worth of concrete and silicon, quietly humming in windowless buildings around the world.

None of these numbers is the "real" answer. All of them are, provided you're willing to say which Internet you mean before you ask how much it weighs.

---

# Acknowledgements

The authors thank the engineers and standards bodies whose public datasheets, thermodynamic principles, and infrastructure surveys made this exercise possible — and Russell Seitz, whose strawberry comparison has now survived nearly twenty years and one full academic paper attempting to gently correct it.

---

# Appendix A — Calculation Summary

**For readers who skipped straight to the appendix hoping for the punchline without the effort — you've found the right place.**

**Model II**

$$E_{min} = kT\ln 2 \qquad m_{bit} = \frac{kT\ln 2}{c^2}$$

**Model III**

$$M_{storage} = S \times D$$

**Model IV**

$$P_{IT} = \frac{P_{total}}{PUE} \qquad M_{Infrastructure} = M_{Servers} + M_{Storage} + M_{Network} + M_{Support} + M_{Buildings}$$

# Appendix B — Assumptions

<table class="paper-table paper-table-small">
  <thead>
    <tr>
      <th>Parameter</th>
      <th>Assumption used</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Ambient temperature</td><td>300 K</td></tr>
    <tr><td>Global digital storage volume</td><td>~175 ZB (IDC estimate)</td></tr>
    <tr><td>Global data center electricity use</td><td>415 TWh/year (2024, IEA)</td></tr>
    <tr><td>Global average PUE</td><td>1.56 (Uptime Institute, 2024)</td></tr>
    <tr><td>Building material intensity</td><td>500–1,500 kg/m² (De Wolf, 2014)</td></tr>
    <tr><td>Scope</td><td>Excludes fiber-optic network and consumer-side hardware</td></tr>
  </tbody>
</table>

# Appendix C — Physical Constants

<table class="paper-table paper-table-small">
  <thead>
    <tr>
      <th>Constant</th>
      <th class="numeric">Value</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>Speed of light, $c$</td><td class="numeric">$2.998 \times 10^{8}\ \text{m/s}$</td></tr>
    <tr><td>Boltzmann constant, $k$</td><td class="numeric">$1.381 \times 10^{-23}\ \text{J/K}$</td></tr>
    <tr><td>Standard temperature</td><td class="numeric">300 K</td></tr>
    <tr><td>$\ln 2$</td><td class="numeric">0.6931</td></tr>
  </tbody>
</table>

---

# References

1. International Telecommunication Union. *Facts and Figures 2024 — Internet Traffic.* [itu.int](https://www.itu.int/itu-d/reports/statistics/2024/11/10/ff24-internet-traffic/)
2. Wired. *The Weight of the Internet Will Shock You.* March 2025. [wired.com](https://www.wired.com/)
3. Landauer, R. "Irreversibility and Heat Generation in the Computing Process." *IBM Journal of Research and Development*, 5(3), 1961. [doi.org/10.1147/rd.53.0183](https://doi.org/10.1147/rd.53.0183)
4. Bormashenko, E. "Landauer Bound in the Context of Minimal Physical Principles." *AIP Advances*, 2024. [pubs.aip.org](https://pubs.aip.org/)
5. Rydning, D. et al. "The Digitization of the World: From Edge to Core." IDC / Seagate White Paper, *Data Age 2025*. [seagate.com](https://www.seagate.com/our-story/data-age-2025/)
6. International Energy Agency. *Energy Demand from AI — Energy and AI Report.* 2025. [iea.org](https://www.iea.org/reports/energy-and-ai/energy-demand-from-ai)
7. Uptime Institute. *Global Data Center Survey Results 2024.* [datacenter.uptimeinstitute.com](https://datacenter.uptimeinstitute.com/)
8. Shehabi, A. et al. *2024 United States Data Center Energy Usage Report.* Lawrence Berkeley National Laboratory. [eta-publications.lbl.gov](https://eta-publications.lbl.gov/)
9. Cisco Systems. *Nexus 9300-FX Series Switches Data Sheet.* [cisco.com](https://www.cisco.com/)
10. Juniper Networks. *MX304 Universal Routing Platform — Hardware Specifications.* [apps.juniper.net](https://apps.juniper.net/)
11. Schneider Electric / APC. *NetShelter SX 42U Enclosure — Product Specifications.* [se.com](https://www.se.com/)
12. Vertiv. *Liebert EXL S1 1000–1200 kW UPS — Technical Specifications.* [vertiv.com](https://www.vertiv.com/)
13. Vertiv. *EnergyCore Li5 Lithium-Ion Battery Cabinet — Data Sheet.* [vertiv.com](https://www.vertiv.com/)
14. Caterpillar Inc. *3516 Diesel Generator Set — Electric Power Specifications.* [cat.com](https://www.cat.com/)
15. Daikin Applied. *Water-Cooled Centrifugal Chiller — Specifications.* [daikinapplied.com](https://www.daikinapplied.com/)
16. Rasmussen, N. "Guidelines for Specification of Data Center Power Density." Schneider Electric / APC White Paper. [mercurymagazines.com](https://www.mercurymagazines.com/)
17. De Wolf, C. "Material Quantities in Building Structures and Their Environmental Impact." MIT, 2014. [dspace.mit.edu](https://dspace.mit.edu/)
18. United Nations Institute for Training and Research (UNITAR). *The Global E-waste Monitor 2024.* [globalewaste.org](https://globalewaste.org/)
19. Einstein, A. "Does the Inertia of a Body Depend Upon Its Energy Content?" *Annalen der Physik*, 1905.
20. Vopson, M. M. "The Mass-Energy-Information Equivalence Principle." *AIP Advances*, 2019. [pubs.aip.org](https://pubs.aip.org/)

---

## Author's Note

This paper was prepared by combining publicly available manufacturer datasheets, thermodynamic first principles, and industry infrastructure surveys with original calculations.

No data center was placed on a scale during this investigation, no zettabyte was weighed directly, and Russell Seitz's original strawberry was left entirely undisturbed.

The authors would like to think this was a methodological choice rather than a practical limitation.