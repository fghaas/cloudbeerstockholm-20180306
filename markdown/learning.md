Leveraging
## OpenStack
from
## Open edX

Note: Alright, we have a highly-available, scalable Open edX cluster
to play with.  How about using it to teach OpenStack itself, or any
other technology that requires learners to access complex distributed
environments?


A
## cluster
to
## play with

Note: Here's what we think is missing from the world of technology training:
affordable self-paced courses that give the trainee an easy way to practice the
theory of cluster deployment and maintenance.


## $$$!

Note: Part of the problem is that giving each and every trainee their own
cluster, even if it's just composed of VMs, would be very expensive.


## Heat
to the rescue!

- A Heat stack for each student... <!-- .element: class="fragment" -->
- ... suspended when not in use. <!-- .element: class="fragment" -->

Note: The solution we came up with is to fire a Heat stack for every student,
but then suspend it if it's not in use.  When the trainee comes back, of
course, the stack is resumed automatically.


Connecting the
## browser
to the
## lab environment

Note: The last piece of the puzzle was finding a way to connect the course
content, as displayed on a student's browser, to the lab environment that would
be created just for them.

The solution we found was Apache Guacamole, a open source, Python and
Javascript terminal emulator, GUI proxy and SSH client.  When run on
the same app server as the LMS hosting the XBlock, it allows us to
create an SSH or RDP connection securely and automatically to the
student's cluster.
