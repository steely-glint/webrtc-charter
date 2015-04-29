# webrtc-charter
Draft for an updated WebRTC Working Group charter

I have a couple of serious problems with the EKR text.
Firstly I don’t like the characterzation of low-level and high-level  APIs.
I substituted 'object-orientated' and 'declarative SDP’ - (I considered ‘opaque SDP blob’)

The reality of the current API is that everyone has to mess with the SDP to get what they
want, and frankly there is nothing lower level than regexps on SDP.

Secondly the backwards compatibility is phrased in a way that binds the future spec to 
reproducing every quirk of the current _implementations_ - We should not be doing this.
It is (as I said a while back) reasonable to expect that apps written to the 1.0 API spec
work in 1.1 - but not if they use undocumented features of implementations (like some
of the more bizarre SDP mangling)- If folks have treated the SDP blob as opaque then
their apps should work in 1.1 - if they have mangled it then probably not.

Thirdly, the exclusion of 1.0 api surfaces in the new object-orientated API is absurd.
I’m hoping that it is a quirk of language and not the intention that the new API has to
have similar - but different - method and object names. As currently written EKR's charter
forbids the new api from using the Doohickey stuff if it gets included in 1.0. Which is 
perverse since it was largely lifted from ORTC discussions. 

I’ve done a quick re-write to fix these issues.
