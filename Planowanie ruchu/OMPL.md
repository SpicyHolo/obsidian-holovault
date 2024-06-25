*Biblioteka implementująca wiele popularnych metod planowania ruchu*
>[!WARNING]
> Nie zawiera metod wykrywania kolizji, ograniczeń i wizualizacji

- Przestrzenie poszukiwań (domyślne): $SE2, SO3, SE3, \mathbb{R}^n$
- Dostępny front-end oparty o PyQt / PySide, wrapper do wykrywania kolizji ([[FCL]], PQP), Assimp do wczytywanie siatek mesh
### Dostęp za pośrednictwem biblioteki MoveIt!

### Dostępne planery geometryczne
#### Mutli-query
- PRM (LazyPRM, PRM*, LazyPRM*)
- SPARS
- SPARS2
#### Sinqle-query
- RRT (RRT-Connect, RRT*, Lower Bound Tree RRT (LBTRRT), Sparse Stable RRT, Transition-based RRT (T-RRT), Vector Field RRT, Parallel RRT (pRRT), Lazy RRT(LazyRRT))
- Expansive Space Trees (EST)
- Kinematic Planning by Interior-Exterior Cell Exploration (KPIECE)
- Search Tree with Resolution Independent Density Estimation (STRIDE)
- Path-Directed Subdivision Trees (PDST)
- Fast Marching Tree Algorithm (FMT*)
- Bidirectional Fast Marching Tree algorithm (BFMT*)
#### Oparte o optymalizację:
- PRM*, LazyPRM*
- RRT*, RRT#, RRTX, Informed RRT*
- Batch Informed Trees (BIT*)
- Lower Bound Tree RRT (LBTRRT)
- Sparse Stable RRT, Transition-based RRT (T-RRT)
- SPARS, SPARS2
- FMT*, CForest, Anytime Path Shortening (APS)
### Dostępne planery kinodynamiczne:

- RRT, Sparse Stable RRT
- Expansive Space Trees (EST)
- Kinodynamic Planning by Interior-Exterior Cell Exploration (KPIECE)
- Path-Directed Subdivision Trees (PDST)
- Syclop
- Linear Temporal Logical Planner (LTLPlanner
#todo not finished note

#robotics #motion_planning #library
