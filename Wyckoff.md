## 1) Exact coordinates given (I copy them so we both use the same list)

A:
(0, 0, 0); (1/2, 1/2, 0); (0, 0, 1/2); (1/2, 1/2, 1/2) — **4 positions**

B:
(0, 1/2, 1/4); (1/2, 0, 1/4); (0, 1/2, 3/4); (1/2, 0, 3/4) — **4 positions**

C:
(1/4,1/4,0); (1/4,3/4,0); (3/4,1/4,0); (3/4,3/4,0);
(1/4,1/4,1/2); (1/4,3/4,1/2); (3/4,1/4,1/2); (3/4,3/4,1/2);
(0,0,1/4); (1/2,1/2,1/4); (0,0,3/4); (1/2,1/2,3/4) — **12 positions**

Total atoms in the conventional I4/mcm cell = 4 + 4 + 12 = **20**.

---

## 2) Strategy / how to use the Wyckoff table

* For each *set* of coordinates check how many symmetry-equivalent positions they produce (multiplicity).
* Look up the Wyckoff rows in the I4/mcm table whose coordinate *form* (and multiplicity) matches the set.
* The **asymmetric unit** is the minimal set of independent coordinates (one representative for each Wyckoff orbit). From that, the table’s symmetry operations generate the full list.

---

## 3) Match A → **Wyckoff 4c**

Look at the table row labelled **4 c (4/m..)** which lists the coordinate representatives `(0,0,0)` and `(0,0,1/2)` (the row shows these two because body centring I produces four positions total). If you apply the body-centering translation (1/2,1/2,1/2) you get:

From (0,0,0):
→ (0,0,0) and (0,0,0) + (1/2,1/2,1/2) = (1/2,1/2,1/2)

From (0,0,1/2):
→ (0,0,1/2) and (0,0,1/2) + (1/2,1/2,1/2) = (1/2,1/2,0) (mod 1)

Collecting these four gives exactly the A list:
(0,0,0), (1/2,1/2,1/2), (0,0,1/2), (1/2,1/2,0).

**Conclusion:** A sits on Wyckoff **4c**. A convenient asymmetric-unit representative is **A @ 4c : (0,0,0)**.

---

## 4) Match B → **Wyckoff 4b**

The table row **4 b (−4 2 m)** lists the two representatives `(0,1/2,1/4)` and `(1/2,0,1/4)` (again the centring gives the other two). Apply centring (1/2,1/2,1/2):

From (0,1/2,1/4) → (0,1/2,1/4) and +cent = (1/2,0,3/4)
From (1/2,0,1/4) → (1/2,0,1/4) and +cent = (0,1/2,3/4)

Collecting these four gives exactly the B list:
(0,1/2,1/4), (1/2,0,1/4), (0,1/2,3/4), (1/2,0,3/4).

**Conclusion:** B sits on Wyckoff **4b**. Representative for the asymmetric unit: **B @ 4b : (0,1/2,1/4)**.

---

## 5) Match C → split into two Wyckoff orbits **8h + 4a**

Look at the 12 coordinates for C: they break naturally into two groups:

**Group C1 (8 positions):** the 8 points at z = 0 and z = 1/2 with x,y ∈ {1/4,3/4}:

```
(1/4,1/4,0), (1/4,3/4,0), (3/4,1/4,0), (3/4,3/4,0),
(1/4,1/4,1/2), (1/4,3/4,1/2), (3/4,1/4,1/2), (3/4,3/4,1/2)
```

This matches the **8 h** row in the table. The 8h general form is (x, x+1/2, 0) etc. Choose x = 1/4. Using the 8h generator positions (the four listed in the table at z=0) and adding the I-centering (which moves those same four to z = 1/2), you obtain exactly those 8 coordinates. (Explicitly: for x=1/4 the table’s four forms generate the four z=0 points; centring gives the four at z=1/2.)

So **C(8h)** with parameter **x = 1/4** generates those 8 points. A convenient representative (one of the orbit members) is **(1/4,1/4,0)** (or the canonical table form (x,x+1/2,0) → (1/4,3/4,0)).

**Group C2 (4 positions):** the four points

```
(0,0,1/4), (1/2,1/2,1/4), (0,0,3/4), (1/2,1/2,3/4)
```

These match the **4 a** row in the table (4a : 422) whose representatives are (0,0,1/4) and (0,0,3/4); adding the I-centering gives the pair at (1/2,1/2,1/4) and (1/2,1/2,3/4). So these four are exactly the 4a orbit.

**Conclusion:** C atoms occupy two orbits: **8h (x = 1/4)** (8 atoms) **+ 4a (z = 1/4)** (4 atoms) → total 12.

---

## 6) Final asymmetric unit (smallest set of independent coordinates)

One representative per Wyckoff orbit is enough to reconstruct the full structure. So the asymmetric unit (choose simple representatives that appear in your given list) is:

* **A** : Wyckoff **4c** — representative **(0, 0, 0)**
* **B** : Wyckoff **4b** — representative **(0, 1/2, 1/4)**
* **C₁**: Wyckoff **8h** — parameter **x = 1/4** → representative **(1/4, 1/4, 0)** (or the table canonical **(x, x+1/2, 0) = (1/4,3/4,0)**)
* **C₂**: Wyckoff **4a** — representative **(0, 0, 1/4)**

That is **4 independent positions** in the asymmetric unit. Applying the symmetry operations listed in the I4/mcm Wyckoff table (and the I-centering shift (1/2,1/2,1/2)) to these representatives reproduces exactly the original lists of A (4), B (4) and C (12) coordinates you were given.

---

## 7) Quick verification (explicit generation)

(I did this implicitly above) — e.g. for 8h with x=1/4 the eight positions are:

(1/4,1/4,0), (1/4,1/4,1/2), (1/4,3/4,0), (1/4,3/4,1/2), (3/4,1/4,0), (3/4,1/4,1/2), (3/4,3/4,0), (3/4,3/4,1/2)

For 4a with (0,0,1/4) you get (0,0,1/4),(1/2,1/2,1/4),(0,0,3/4),(1/2,1/2,3/4). These match your provided C coordinates.

---

## 8) Short summary / answer block

* **Space group:** I4/mcm (No. 140) (given)
* **A** → Wyckoff **4c**; representative **(0,0,0)** (generates the four A positions)
* **B** → Wyckoff **4b**; representative **(0,1/2,1/4)** (generates the four B positions)
* **C** → two Wyckoff orbits **8h** (x=1/4) and **4a** (z=1/4); representatives **(1/4,1/4,0)** and **(0,0,1/4)** respectively (together they generate the 12 C positions)

Asymmetric unit (one convenient choice): `{ A(0,0,0)@4c, B(0,1/2,1/4)@4b, C(1/4,1/4,0)@8h, C(0,0,1/4)@4a }`.

---

If you want, I can now:

* explicitly list all generated coordinates from the asymmetric unit (so you see the exact expansion step-by-step), or
* write a tiny Python/Spglib script that takes those asymmetric-unit reps and prints all symmetry-generated coordinates for **I4/mcm** (so you can compare programmatically). Which would you prefer?
