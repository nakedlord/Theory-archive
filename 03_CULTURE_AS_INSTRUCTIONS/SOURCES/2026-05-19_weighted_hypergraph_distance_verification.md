# Source Verification — Weighted Hypergraph Distance

Status: source verification / supports formalization probe / not canon
Date: 2026-05-19
Source ID: `source-2026-05-18-higher-order-instruction-networks`
Target hypothesis: `03_CULTURE_AS_INSTRUCTIONS/HYPOTHESES/2026-05-18_hypergraph_formalization_probe.md`
CSP event: `projects/syntax/events/2026-05-19-chatgpt-hypergraph-instructional-culture-source-case-test.md`

## Verified Source

```text
Title: Distances in weighted higher-order networks
Journal: Communications Physics
Publication date: 2026-03-26
Article number: 178
DOI/article URL: https://www.nature.com/articles/s42005-026-02592-w
```

Authors include Charo I. del Genio, Ekaterina Vasilyeva, Liubov Tupikina, Dmitry Fedorov, Daniil Musatov, Andrei M. Raigorodskii, and Stefano Boccaletti.

## What the Paper Actually Claims

The paper proposes a general distance measure for weighted hypergraphs.

The relevant claims for this theory module are:

1. Weighted hypergraph distance is nontrivial because arbitrary hyperedge weights can create inconsistencies.
2. The proposed measure is well-defined and reduces to classic graph distance when all hyperedges are pairwise links.
3. Clique projection can lose meaningful higher-order information.
4. Hyperedge size, hyperedge intersection, and hyperedge weights can change distances in ways that pairwise projection hides.
5. The authors test the method on real-world higher-order datasets, including arXiv preprint categories.
6. The authors provide data and code links.

## Applicability to Culture as Externalized Instructions

The paper does not study culture, ritual, institutions, myths, or instructions.

Its direct relevance is methodological:

```text
If a system contains meaningful higher-order edges, projecting them into pairwise edges can lose structural information.
```

This supports the Culture module's formalization probe only at the level of representation choice.

## What Transfers Cleanly

### 1. Higher-order edges preserve bundle structure

Cultural transmission often works through carrier bundles:

```text
text + ritual + institution + image + repeated practice -> instruction bundle
```

A pairwise graph turns this into many two-node links and may lose the fact that the whole carrier bundle acted together.

### 2. Hyperedge size matters

A transmission involving two carriers is not structurally equivalent to a transmission involving six carriers.

This matters for culture because a larger carrier bundle may mean broader stabilization, but also lower specificity.

### 3. Hyperedge intersection matters

Two cultural transmission events may overlap by one carrier or by many carriers.

Example:

```text
e1 = {text, ritual, institution, instruction A}
e2 = {ritual, institution, image, instruction B}
```

Their shared carriers matter. Pairwise projection may hide how much of the transmission structure overlaps.

### 4. Hyperedge weights matter

The paper's method allows weighted hyperedges. For Culture as Instructions, candidate weights include repetition, emotional load, institutional support, ritual recurrence, identity linkage, and transmission cost.

## What Does Not Transfer Directly

### 1. Distance is not yet transmission strength

The paper defines distance. Culture as Instructions needs transmission strength, persistence, mutation, and reinterpretation.

These may use distance, but they are not the same thing.

### 2. The paper is mostly static / structural

Culture needs time and direction:

```text
who transmits -> through which carrier bundle -> to whom -> with what mutation -> at what time
```

A usable cultural model must be typed, temporal, directional, and source-aware.

### 3. We cannot assume irreducibility

The paper itself shows that some datasets are better approximated by clique projection when pairwise interactions dominate. Therefore the Culture module needs a comparison test, not automatic hypergraph adoption.

## Formal Consequence for the Hypothesis

Update the hypothesis constraint:

```text
Use hypergraph modeling only when the cultural case contains irreducible carrier-bundle transmission that pairwise projection fails to preserve.
```

Do not model every cultural network as a hypergraph by default.

## Recommended Test

For each candidate cultural case:

1. Build a pairwise graph representation.
2. Build a typed temporal hypergraph representation.
3. Ask whether hypergraph representation changes:
   - nearest carriers;
   - inferred transmission path;
   - explanation of mythologization;
   - survival of inconvenient details;
   - MEAT complex stability.
4. Reject hypergraph complexity if pairwise graph captures the same distinctions.

## Status

```text
source verified for representation-risk claim
not evidence for cultural theory by itself
supports formalization probe only
```
