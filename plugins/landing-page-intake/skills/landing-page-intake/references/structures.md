# Landing Page Structures

## Base Structures

### SERVICE Base Structure

```
1. Navbar (optional)
2. Hero
3. (Optional) Social proof #1 (logos/press/customer count)
4. Features/Benefits + Objections (main body)
5. (Optional) Social proof #2 (testimonials/results)
6. (Optional) How it works / Process
7. (Optional) Pricing / "starting at"
8. (Optional) FAQ
9. CTA Section
10. Footer
```

### PRODUCT Base Structure

```
1. Navbar
2. Hero
3. Social proof #1
4. Features/Benefits + Objections
5. Social proof #2
6. (Optional) How it works
7. (Optional) Pricing
8. (Optional) FAQ
9. CTA Section
10. Footer
```

---

## Optional Section Rules

### Add "How it works / Process" if:

- User provided a clear process (Q12), OR
- The offer is novel/complex, OR
- "Main friction" (Q14) includes confusion/complexity/trust

### Add "Pricing / starting at" if:

- Pricing is known AND they want to qualify leads, OR
- Objections (Q14) include "price" / budget misfit, OR
- CTA is "buy" (product) → pricing usually needed

### Add "FAQ" if:

- There are 2+ strong objections (Q14), OR
- The offer is complex/novel

### Social proof #1 if:

- They have logos/press/customer count (Q11)

### Social proof #2 if:

- They have testimonials/results/case studies (Q11)

### Navbar rules:

- Optional for services if it distracts (single-purpose lead gen page)
- If unsure, keep it but minimal
- Required for products

---

## Decision Matrix

| Signal | Include Section |
|--------|-----------------|
| Clear process provided | How it works |
| Complex/novel offer | How it works + FAQ |
| Trust issues in objections | How it works |
| Price objections | Pricing (with anchoring) |
| CTA = "buy" | Pricing |
| 2+ objections | FAQ |
| Has logos/press | Social proof #1 |
| Has testimonials/cases | Social proof #2 |
| Lead gen page (service) | Navbar optional |

---

## Structure Selection Logic

```
IF business_type == SERVICE:
    Start with SERVICE base
    Navbar = optional (omit if pure lead gen)

IF business_type == PRODUCT:
    Start with PRODUCT base
    Navbar = required
    Social proof #1 = required if any proof exists

THEN apply optional section rules based on Q11-Q14 answers
```
