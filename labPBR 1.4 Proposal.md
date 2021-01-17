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

Textures will be named either `texture_s.png` or omit the `texture` and be `_s.png` or `_s` for the purposes of this document.
Until sp614x defines the behaviour in Optifine, the second specular and normal map will use the extensions `_s2` and `_s3` as in `texture_s2.png`

The additional maps are going to be as follows:
- Metalness (override labPBR 1.3 metals)
    - More granularity for stuff like copper in MC 1.17
- Anisotropic rotation (0-90)
    - 90 degrees is enough to make a circle
- Anisotropic strength
- Extinction RGB
    - As best I understand it, metalness and metallic colour in three channels
- f0 Colour
    - Also for metals?