#################################################
labPBR 1.4
#################################################
An update to keep compatibility with 1.3 while adding extra functionality.

Reason:
A feature request has been given to sp614x to add another specular map and normal map using some of the free samplers. Using these two maps, we can fit in any extra data we need for full metalness-based PBR.

Priorities:
- Keep 1.3 compliant, so shaders with 1.3 support can use 1.4 resource packs with no issues.
- Fit in the values needed to have a full metalness workflow.
- Be easy to design for.

Things to keep in mind:
- This is going to increase memory bandwidth use, as we're adding two more textures to sample.
- 1.3 f0 and metalness support MUST remain intact.
- For now this is theoretical, as sp614x has not confirmed he will add the features required to Optifine.

