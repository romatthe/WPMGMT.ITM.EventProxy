````
+----+ +----+ +----+ +----+ +----+ +----+ +----+
| PC | | PC | | PC | | PC | | PC | | PC | | PC | ... ...
+--+-+ +--+-+ +-+--+ +--+-+ +--+-+ +--+-+ +--+-+
   |      |     |       |      |      |      |
   |   +--+  +--+  +----+    <-+    <-+    <-+
   |   |     |     |
+---v---v-----v-----v+         +-----------------------+
|                    | TCP/IP  |                       |
| Monitoring Backend +--------->  Data Enrichment App  |
|                    |         |                       |
+--------------------+         +---------+-------------+
                                        |
         +------------------------------+        +---------+
         |                                       |         |
         |                +----------------+     |         |
   +-----v-----+---------->    DB Proxy    +----->  S Q L  |
   |           | PUB/SUB  +----------------+     |         |
   |   Redis   |                                 |         |
   |           |          +----------------+     +---------+
   +-----------+          |     TO BE...   |
                          +----------------+
````
