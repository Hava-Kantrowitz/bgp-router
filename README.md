# bgp-router

We implemented several functions for the milestone, including `lookup_routes()`, `forward()`,
`update()`, `dump()`, `handle_packet()`, and `filter_relationships()`. We had some issues sending
updates to other peers, such as formatting issues for not updating the AS paths and sending
duplicate updates. We tested our router by ensuring that it passed the Level 1 test cases.
