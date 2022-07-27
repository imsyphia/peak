Peak is a Minecraft density function library that computes coordinates.

Peak is licensed under the Mozilla Public License version 2.0. A copy
of the license is included, and an FAQ regarding the license can be
found [here](https://www.mozilla.org/MPL/2.0/FAQ/).

The current supported versions of Minecraft are 1.19 and 1.19.1, however
the pack may still work on older versions.

The x and z coordinates provided are inexact, and may change for a given seed
based on implementation details, so implementations are given different names.
A given version of Peak is guaranteed to be compatible with any other version
based on the same Minecraft version, meaning that _all_ density functions and
noises in all stable implementations will work, and give the same result, when
multiple versions of Peak are loaded. The purpose of this is to make embedding
Peak in a data pack safer, and to make it easier to build new implementations
from on other ones, while also maintaining performance. Stable implementations
reside in `peak:s/`, while unstable ones should be in `peak:exp/`.

The density functions that compute the coordinates can be accessed at
`peak:s/<impl>/x`, `peak:s/<impl>/y`, and `peak:s/<impl>/z`. With the simple
(and currently only) implementation _base_, it would look like `peak:s/base/x`.

Embedding Peak into a data pack is suggested for ease of distribution, and
because loading multiple data packs containing different versions of Peak
should not cause any issues. The `peak` namespace folder in `data` contains
an additional copy of the license, so the entire folder can just be copied
into a data pack.
