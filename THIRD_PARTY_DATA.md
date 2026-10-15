# External preflop supplement

The 137 original course charts are unchanged.

Source: https://github.com/jensbaagaard/poker-practice
Revision: 449993f78d995c77b72d0bcac418a8507dd6f783
Data format and sizing: https://github.com/jensbaagaard/poker-practice/blob/449993f78d995c77b72d0bcac418a8507dd6f783/data/openSourcePokerData/README.md

The source README declares MIT and states its range data is free to use.
A standalone LICENSE file was not present at the time of review. The range
documentation describes Poker Trainer built-in data extracted from application
bundles; the upstream solver provenance and its accuracy are not independently
verified. This attribution does not claim independent solver certification.

Only missing `vs_raise` charts are supplemented. Course charts and existing
adaptations always take precedence. No opens, limp defenses, rejam calls or
response-to-3bet charts are replaced.

Imported anchors:
- MTT 20 BB, used only within the UI 20–25 BB band as a labelled approximation.
- MTT 40 BB, used only within the UI 40–49 BB band as a labelled approximation.

No interpolation or extrapolation to the other UI stack bands. 100 BB was
not stretched over 50+ BB. 5/10 BB shove calls were not mislabelled as calls
of a normal open-raise or of a rejam after our own open.

Ante 1 BB is stated by the source sizing profile. These are not treated as
ICM, PKO, satellite, or separately solved 8/9-handed ranges. Position mapping:
UTG=EP1, UTG+1=EP2, UTG+2=EP3, MP=LJ, HJ=HJ, CO=CO, BU=BTN, SB=SB, BB=BB.
The 8-max UI omits UTG/EP1; it does not rename EP2 to EP1.

Frequencies for raising and calling are preserved. Fold = 1 - raise - call.
The source's zero weights remain zero. Missing JSON hands are interpreted as
zero according to the source schema. Every imported row was validated for
finite [0,1] frequencies and raise + call <= 1. No random 50/50 splitting.

Source JSON SHA256:
{
  "MTT_20_GTO.json": {
    "sha256": "87d432c8bf364ec7990422bad446e8d141e3f2d45f1897a59499e70c8b888e0b",
    "url": "https://github.com/jensbaagaard/poker-practice/blob/449993f78d995c77b72d0bcac418a8507dd6f783/data/openSourcePokerData/MTT_20_GTO.json"
  },
  "MTT_40_GTO.json": {
    "sha256": "043d0ae8ae926069ce3d2188a469e9776a7f74c9e147920147a734f063a5c70b",
    "url": "https://github.com/jensbaagaard/poker-practice/blob/449993f78d995c77b72d0bcac418a8507dd6f783/data/openSourcePokerData/MTT_40_GTO.json"
  }
}
