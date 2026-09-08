
An Auto-knotting Anchor is a sophisticated and modern iteration on a traditional [Weave Anchor](Weave%20Anchor.md). Traditionally, Maji would carry a set of pre-made knots in their desired materials. Whenever they would want to use a specific type of Majik within the school they are anchored to, they would open the small chamber of their Anchor, rip out the installed not, and then connect the two ends of their other knot manually. This meant that switching between Majiks in a school was not the fastest thing. Most Maji could do it in about 5-10 seconds, so nothing major, but 5-10 seconds in a battle could be the difference between life and death.

Because of this, most usually focused on mastering just one or two specific Majiks *within* their school, but others still trained to be more well rounded of course.

After many years, as technology had improved, Artificers were able to use a complex set of gearing to build "Auto-knotting Anchors". A Majus could now take an unknotted string/wire, insert it into the chamber of their autoknot Anchor, and then quickly select the knot they wanted to use, at that point, the Anchor would automatically make the knot and insert the ends into the core and the veinport, at which point the Majus could now use that type of Majik within their school, no more manually swapping out pre-made knots.

Maji work closely with their school's Artificers to come up with a knotting selection system that works best for them. It usually involves intense surgery to implant the needed mechanisms. 

## Autoknot Anchor Systems

### Power Systems

Power systems define how the autoknotting gearing is powered to actually "auto-knot" and plugin the knot ends to the coreport and the veinport. They also determine the "confirmation" mechanism.

#### Blood Powered Autoknotting (modern)
The cost is honestly pretty small, blood is a fairly powerful force in terrum, so most go with this, the cost is a bit more though, but ultimately much less invasive.

Since there is no real "action" to "confirm" a knot-slot selection so the auto-knot anchor knows to actually knot it, a Majus needs to install some confirmation input, it can be a switch or a gesture. Gestures are popular but expensive installs, it involves alot of hand surgery to implement pulleys to only trigger an autoknot for the selected knot-slot when a certain gesture is made, which causes all the pulleys to pull the confirmation pins all into alignment, thus triggering the auto-knotting.

#### Ripcord Powered Autoknotting (antiquated system)
A rip cord autoknotting system saves you from the blood cost a Blood powered autoknot anchor has. But the system can be less reliable over time as the rip cord wears with use, you also have to have the space to do it. People with these typically don't have the rip cord installed right on the arm where most anchors are embedded, its usualy somewhere on their body (with the cord threaded back to the anchor internally, very invasive install) so that if they loose their non-anchor arm, they can still pull on the ripcord. Very few have this power system installed, mostly old Maji before the blood powered systems where invented.

With a ripcord autoknot, they simply pull the ripcord to "confirm" the knot setting as it won't autoknot until the cord is pulled.

## Knot Materials

string isn't used with autoknotting anchors as string is mainly used as one time use knot material. No sense in putting a string in an autoknotter when the string is just going to get gunked up with dried blood.

### Metal Knots

Metal knots are the main material as you can get reuse out of them since they don't soak up the blood. But metal wires come with their own complexities too. Since auto-knotters reuse the same piece to create the knot, that piece of metal is getting unknotted and re-knotted over and over.

Different metals have different fatiguing before they break. The gauge of the wire can increase durability, but it also limits the complexity of the knots it can make. What further complicates things is that depending on the type of blood of the Majus and the school of majik they are anchored to will also play into what type of metal, and what gauge is best. So there are multiple factors that play into the effectiveness of a knot for a given majus. A majus needs to work work with their Artificers as they'll help them know what's best for them.

The metals that Artificers use:
- Aluminum (most common)
- Copper (fairly abundant)
- Silver (common enough)
- Gold (rare)
- Platinum (extremely rare)

A Majus can truly use any metal and gauge and successfully use it to pull majik from a Cord in the school of majik they are anchored to. However, to maximize the power to blood ratio, the following has been found to be the best configuration, however it doesn't account for longevity (fatiguing of the wire, the gauging will be the main trade off majus will need to determine, though maji who's configuration is best suited with rare metals are the main ones who have to consider the longevity question: do I go with a lower gauge and limit the knot types I can make but get the most power out of the knots I can make, AND get more uses? Or do I use a metal less conducive with my blood for my given school of majik and blood at the cost of access to more complex knots and thus a wider range of majik AND still get longevity)

- rastuic
	- overall: Aluminum
	- A: Silver 
	- B: 
	- AB: Aluminum
	- O: Gold, 22 gauge
- mardic
	- overall: copper
	- A: Silver
	- B: Aluminum
	- AB: Copper
	- O: Gold
- ceric
	- best metal: silver
- duric
	- best metal: gold
- woven
	- best metal: platinum




### Knot-switching Systems
### Binary Switch System

The most common setup for this type of system is to have a set of small binary switches on the thumb side of their four fingers of the hand the Anchor is embedded in, they can then use the thumb of that hand to quickly flick the switches to indicate the knot they want. The switches are connected to a set of tiny articulate pulleys that connect to their autoknot anchor where they pull on some setting pins that in-turn activate the gears. The gears are powered by the blood pumping through the connected veinports, so autoknot anchors do cost a small amount of blood for the price of Majik flexibility within their school of majik.

### Rotary Gear System (most popular)

A more expensive install, but it typically involves 2 gear rings added around the bone of a single finger, one with 8 gear spokes, and the other with 2 gear spokes, giving them 16 total "knot slots".

Most use binary switches, with 4 binary switches, that gives them 16 possible knots the autoknot anchor can make. More expensive installs involve gear rings added around the bone of a finger with 7 small gear spokes

The gearing the artificers make is extremely advanced, with a 16 slot autoknot anchor, the gearing has to be able to perform 32 operations: 16 knots movements, 16 unknotting movements.



Lorekeeper script to generate durability of different metal type gauges:
```dart
import 'dart:math';

enum MajikMetal {Platinum, Copper, Silver, Gold, Aluminum}

const double base_cycles = 2000;
const metal_weights = {
  MajikMetal.Platinum: 0.97,
  MajikMetal.Copper: 0.78,
  MajikMetal.Silver: 0.75,
  MajikMetal.Gold: 0.5,
  MajikMetal.Aluminum: 0.3,
};
const metal_gauges = [20.0, 22.0, 24.0, 26.0, 28.0, 30.0];

int knotWireCycles(MajikMetal metal, double metal_gauge) {
  final gauge_factor = pow(0.8, (30.0 - metal_gauge)); // independent degradation curve
  return (base_cycles * metal_weights[metal]! * gauge_factor).round();
}

void main() {
  for (final metal in metal_weights.keys) {
    for (final gauge in metal_gauges) {
      print("${metal.name} $gauge gauge: ${knotWireCycles(metal, gauge)} knots");
    }
    print("-----");
  }
}
```

```
Platinum 20 gauge: 208 knots
Platinum 22 gauge: 325 knots
Platinum 24 gauge: 509 knots
Platinum 26 gauge: 795 knots
Platinum 28 gauge: 1242 knots
Platinum 30 gauge: 1940 knots
-----
Copper 20 gauge: 168 knots
Copper 22 gauge: 262 knots
Copper 24 gauge: 409 knots
Copper 26 gauge: 639 knots
Copper 28 gauge: 998 knots
Copper 30 gauge: 1560 knots
-----
Silver 20 gauge: 161 knots
Silver 22 gauge: 252 knots
Silver 24 gauge: 393 knots
Silver 26 gauge: 614 knots
Silver 28 gauge: 960 knots
Silver 30 gauge: 1500 knots
-----
Gold 20 gauge: 107 knots
Gold 22 gauge: 168 knots
Gold 24 gauge: 262 knots
Gold 26 gauge: 410 knots
Gold 28 gauge: 640 knots
Gold 30 gauge: 1000 knots
-----
Aluminum 20 gauge: 64 knots
Aluminum 22 gauge: 101 knots
Aluminum 24 gauge: 157 knots
Aluminum 26 gauge: 246 knots
Aluminum 28 gauge: 384 knots
Aluminum 30 gauge: 600 knots
-----
```