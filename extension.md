# Extension (extension.md): How can we add additional features to the protocol without breaking previous functionality?


For each web packet, we could have `header` and `body`. Within the `header`, we could contain multiple fields. The `header` could reserve some place in the header to specify the type of the content (e.g. ASCII test, Unicode test, etc). Once the packet is received and acknowledged by the node, it's going to add its own identity information to the header, such as its IP address, so that the protocol is able to keep a record of what nodes the packet passed through. To send this packet to anyone on the whole UW campus, we could:
1. Specify some representative of all people in each classroom
2. People in the same classroom could send the packet directly to the receiver
3. If someone wants to send the packet outside the classroom, he/she will first give the packet to the representative
   1. The representative would send the packet to another representative of the classroom where the receiver is located
   2. The receiver will get the packet from his/her own representative
   3. Once the receiver receives the packet, send back the acknowledgement based on the route specified by the header

If there's any additional features need to added, we would just added more fields for each feature to the header of the packet.