# Local potential problems

(Notes by Gustav Schmid)

<!-- TODO: Add informal human notes below. Suggested structure: -->

## Main idea

All of the main ideas where already present in the original paper, but in the original analysis, we payed twice for the ball growing argument at the hart of the approach. I already knew that the original analysis could be done using only the sequence of improving sets lemma, but i always had a diameter (of the improving sets) dependency. I knew that it should be possible ot remove this and GPT-6 managed to do it. 


## What I checked

The new improving sequence lemma is correct and gives both of the improvments in the upperbounds with a straightforward adaptation of the existing approach. 

## Open questions and possible issues

The lowerbounds do not quite match the upperbounds. The issue might be because the definitions are slightly off. Basically with LOC we have a potential that is just counting "bad" edges (so non-cut edges). While in the generic definition of Local Potential Problems, we also have potential on the nodes. I think this is why upper and lowerbounds do not match exactly. Maybe by making some reasonable assumption on the local Scale, or having a slightly cleaner definition, we can also get rid of the K dependency.

I feel like it should be possible to shave one or two more log factors if one is aiming for specific problems, so e.g. in a specific algorithm for LOC. 