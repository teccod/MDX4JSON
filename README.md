Cache-MDX2JSON
==============

RESTful web api for MDX2JSON transformation (also JSONP and XML/A).

Installation.

1. Make Cachelib database read-write. (SMP → System Administration → Configuration → System Configuration → Local Databases, choose CACHELIB, uncheck Read Only, Save changes)
2. Import all files into namespace with cube(s), you wish to query (if cubes are distribted across several namespaces the best practice would be to create new namespace, import these files and link cubes globals to new namespace)
3. Compile classes, if you linked globals check that all DeepSee cubes work in new namespace (you may also need to enable DeepSee in the new namespace, to do it execute terminal command: D EnableDeepSee^%SYS.cspServer("/csp/NewNamespace/")
4. Make Cachelib database read-only (optional but recommended, see 1 for how-to)
5. Create new webapplication, important settings are: namespace - choose namespace, in which you imported this project; Dispatch class:  MDX2JSON.REST
6. Give the new webapplication correct roles for it to query cubes


For information on how to work with this RESTful web API please refer to included documentation.
