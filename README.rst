MIRI Investigations: Using the 1st group
========================================

Investigations of using the 1st group when saturation happens
in a pixel between the 2nd and 3rd group.  Generally, the 
1st group is always flagged as DO_NOT_USE in all MIRI 
observations due to a known transient seen in the 1st group.

These investigation found that in the case of saturation
between the 2nd and 3rd group, the 1st and 2nd groups can be
used to get a slope measurement that is around 1% accurate.
This is because the 1st group transient is small compared to 
the number of DN measured between the 1st and 2nd group.  The 
analysis is given in `Test_use_group1_if_bright.ipynb`.

This work was written up in a JWST report (ref TBA) and
the PR to the jwst pipeline that added the `bright_use_group1`
flag to the `firstframe` CALWEBB_DETECTOR1 step.

In addition, there is a 2nd notebook `Test_use_only_group1_if_bright.ipynb`
that has done a preliminary analysis of using *just* the 1st group
along to estimate the slope.  This analysis assumes the ramp stars at 
0 DN, something that is not correct, but may be a reasonable approximate
for such bright pixels.  This *prelminary* analysis shows that such a 
slope estimate is likely at least 10% incorrect.  More analysis is needed
on using the 1st group alone.


In Development!
---------------

Active development.

Contributors
-----------
Karl Gordon

License
-------

This code is licensed under a 3-clause BSD style license (see the
``LICENSE`` file).
