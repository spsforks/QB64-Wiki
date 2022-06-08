DISPLAYTITLE:_SNDRAWDONE
[_SNDRAWDONE](_SNDRAWDONE) ensures that the final buffer portion is played in short sound effects even if it is incomplete. 


## Syntax

>  [_SNDRAWDONE](_SNDRAWDONE) [pipeHandle&]


PageParameters
* The optional pipeHandle& parameter refers to the sound pipe opened using [_SNDOPENRAW](_SNDOPENRAW). 


## Description

* Use to force playing small buffers of [_SNDRAW](_SNDRAW) data.


## See Also

* [_SNDOPENRAW](_SNDOPENRAW)
* [_SNDRAW](_SNDRAW)
* [_SNDRAWLEN](_SNDRAWLEN)
* [_SNDRATE](_SNDRATE)



