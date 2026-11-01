---
tags:
  - university/INF295
  - cs/ai
  - moc
aliases:
  - IA
  - INF295
  - "#university/INF295"
---
# INF295 - Inteligencia Artificial

## Contenidos C1

> [!source] Problemas CSP/CSOP
> Las fuentes para encontrar todos los modelos y demás son varias
> - Se encuentra la bitácora de clase
> - Libro Guía: [[Artificial Intelligence - A modern Approach]] 

### Modelamiento

Definición de los tipos de problemas: 
- [[Constraint Satisfaction Problem|CSP/CSOP]] 
	- [[Constraint Satisfaction Problem#Search Space|CSP > Search Space]] o espacio de búsqueda
- [[Combinatorial Optimization]]

Caracteristicas de los problemas:
- [[Polynomial Complexity]] ([[P Complexity|P]], [[NP Complexity|NP]], [[NP-Hard Complexity|NP-Hard]] and [[NP-Complete Complexity|NP-Complete]]) 

Tipos de (Constraints) Restricciones
- [[Constraints in CSP#Variable Types]]
- [[Constraints in CSP#Hardness]] (Restricciones duras y blandas)

> [!important] 
> Los modelos se puede hacen mediante [[Integer Programming]] o [[Constraint Satisfaction Problem|CSP]]. La diferencia de estos se pueden ver en sus notas particulares.

Modelos comunes
- [[N-Queens]]
- [[Knapsack Problem]] (Problema de la mochile)
- [[Set Cover Problem]] (Set packing, covering and partitioning)
- [[K-Graph-Coloring Problem]]
- [[Travelling Salesman Problem]] (Problema del vendedor viajero)
- [[Timetabling Problem]]
	- [[Airline Crew Scheduling Problem]]
- [[Job-Shop Scheduling Problem]]
- [[Space Planing Problem]]
- [[Car Sequencing Problem]]
- [[Vehicle Routing Problem]]
- [[Quadratic Assignment Problem]]

Sobre complejidad de los problemas
- [[Fase de Transición en Modelos CSP]]
### Técnicas de Filtro

Conceptos para filtrar
- [[Trashing]]

Grafo de Restricciones
- [[Constraints in CSP|Constraints in CSP/CSOP]]
- [[Constraint Graph]]

Sobre Consistencia
- [[K-Consistency]]
	- [[Node Consistency]]
	- [[Arc Consistency]]
	- [[Path Consistency]]
- [[Arc Consistency Algorithm 3]] (AC-3)

Modelos con generación de columna
- [[Column Generation Model]]

### Técnicas de Resolución Completas

> [!note] 
> Estas son las técnicas de resolución para el certamen 1. Después se explica que este tipo de técnicas se llaman "completas" al tomar todo el espacio de búsqueda.

Técnicas basadas en Look-Back
- [[Backtracking]]
- [[Graph Backward Jumping]] (GBJ)
- [[Conflict Backward Jumping]] (CBJ)

Técnicas basadas en Look-Ahead
- [[Forward Checking]] 
- [[Real Full Lookahead]]
### Técnicas de Heuristica

Definición de Heuristica:
- [[Heuristic Techniques]]
- [[Dynamic Order Heuristic]]

Heuristicas de Instanciación
- [[Minimum Remaining Value Heuristic]]
- [[Degree Heuristic]]
- [[Least Constraining Value Heuristic]]

## Contenidos C2
### Definición Técnicas de Resolución
Definición de todos los algoritmos:
- [[General Taxonomy for Problem-Solving Techniques]]

Categorias Principales:
- [[Exhaustive Search Algorithms]]: Algoritmos/Técnicas Completas
- [[Local Search Algorithms]]: Algoritmos/Técnicas Incompletas

Metaheuristicas:
- [[Metaheuristics]]
- [[Heuristic Techniques]]

Concepto de explosión combinatorial
- [[Combinatorial Explosion]]

### Técnicas Incompletas de Solución

Algoritmo Constructivos
- [[Greedy Algorithm]]
- [[Greedy Randomized Adaptive Search Procedure Algorithm]] (Greedy + Probabilidades)

Algoritmos Reparadores (Profundización en [[Local Search Improvement Algorithms|Improvement Algorithm]])
- [[Hill Climbing Algorithm]]
- [[Simulated Annealing Algorithm]]
- [[Tabu Search Algorithm]]

Parámetros para técnicas incompletas
- [[How to choose Parameters Values for Local Search Algorithms]]

### Técnicas Incompletas Geneticas

Definición de algoritmo genético
- [[Genetic Algorithm]]

Algoritmo Constructor:
- [[Ant Colony Optimization]]

Algoritmo Reparadores:
- [[Evolution Algorithm]]

