## NAME FORMAT:
- SM_port_JN_a_b_c:
  1. a: Fleet size;
  2. b: Sample size;
  3. d: index of the instance in a group of the same a,b, and c (d=1,2,3,4,5,DD). 
     DD: the instance was generated by the data-driven routing sampling approach

## PARAMETERS:
- Variables:
  1.  R:     number of routes
  2.  F:     number of trucks
  3.  V:     number of time vertices
  4.  N:     number of nodes
  5.  A:     number of arcs
  6.  K:     number of charging station types
  7.  H:     number of configurations of trucks
  8.  L:     number of legs
  9.  MRN:   maximum number of nodes in a route
  10. MRA:   maximum number of arcs in a route
  11. MRL:   maximum number of legs in a route
  12. MLN:   maximum number of nodes in a leg
  13. Orivc: initial electricity of each truck starting a route
  14. VER:   per-kilo meter electricity consumption in WH
  15. VDR:   per-kilo meter diesel consumption in litre 


- Vectors and Matrices:
  1.  Setable[V]:     indicators for whether a station can be set at a vertex; 0: a charging station cannot be set at the vertex, 1: a charging station can be set at the vertex 
  2.  Length[B][V]:   the length between nodes, in meters 
  3.  RLEN[R]:        number of nodes in each route
  4.  RLGS[R]:        number of legs in each route 
  5.  RVset[R][MRN]:  set of vertices in each route
  6.  RNset[R][MRN]:  set of nodes in each route 
  7.  RAset[R][MRA]:  set of arcS in each route 
  8.  RLset[R][MRL]:  set of legS in each route
  9.  LNN[L]:         number of nodes in each leg
  10. LNset[L][MLN]:  set of nodes in each route
  11. Sertimes[L]:    the service time at each leg, in seconds 
  12. Tratimes[L]:    the traveling time at each leg, in seconds 
  13. RDIS[R]:        distance of routes, in metres 
  14. POWER[K]:       charging speed of each type of charging stations, in kW
  15. Capacity[H]:    capacity of each configuration of trucks
  16. C2[H]:          cost of each configuration of trucks




