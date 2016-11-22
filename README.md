```
cd rdpl
dub build :inspector
```
failed with
```
Root package rdpl:core reference gfm:math ~>6.1.4 cannot be satisfied.
```
but if in rdpl/inspector/dub.sdl comment out line 6
```
//dependency "rdpl:core" version="~>0.0.3"
```
then recompile dub starts satisfying the reference above. You can now uncomment line 6 and it works as expected.
if you remove rdpl/.dub folder then error appears again.
