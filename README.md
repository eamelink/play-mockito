Play Mockito module *Unmaintained*
===================

*THIS MODULE IS NOT MAINTAINED ANYMORE(

Mockito is slightly incompatible with Play, for two reasons:

* Mockito caches classes, causing class cast exceptions when play reloads them after modification.
* Mockito uses a classloader to find the MockitoConfiguration class, that does not find source java files as used in Play.

This plugin solves those problems by:

* Shipping a minimally modified mockito in which you can disable the cache.
* Shipping a compiled MockitoConfiguration class that will be found by Mockito.

Hopefully, the patch for the first issue will be accepted upstream, so that this plugin no longer needs to ship a modified Mockito in the future.

*UPDATE*

I believe a patch for the first issue has been accepted a long time ago, and this plugin can be much simplified; no modified Mockito needs to be shipped anymore.

License
=======

Copyright 2011 Erik Bakker (http://eamelink.net).

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this project except in compliance with the License. You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0.

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
