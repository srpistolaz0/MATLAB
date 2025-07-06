# MATLAB / GUI Octave Linear System Solvers

Toolbox that collects **direct methods** for solving linear systems and inverting matrices, including Gaussian elimination (with several pivoting strategies) and LU factorization (with and without pivoting, plus iterative refinement).

src/
├── solve_backsub.m                  ← backward-substitution                          | Sustitución hacia atrás
├── solve_forwardsub.m               ← forward-substitution                           | Sustitución hacia adelante
├── solve_gauss.m                    ← Gaussian elimination (no pivot)                | Gauss sin pivoteo
├── solve_gauss_pivot_column.m       ← Gaussian elimination with column pivoting      | Gauss con pivoteo por columnas
├── solve_gauss_pivot_complete.m     ← Gaussian elimination with complete pivoting    | Gauss con pivoteo completo
├── solve_lu.m                       ← LU factorization (no pivot)                    | LU sin pivoteo
├── solve_lu_pivot_complete.m        ← LU factorization with complete pivoting        | LU con pivoteo completo
└── solve_lu_iterative_refinement.m  ← LU + iterative refinement                      | LU + refinamiento iterativo 

Quick Start
% Example / Ejemplo:
A= [4,2,1;6,3,0;2,7,5]:
B= [ 9 ; 18 ; 17 ]; 

x = solve_gauss_pivot_column(A, b);      % Gaussian elimination with column pivoting
% x = solve_lu(A, b);                    % LU factorization (no pivoting)
% x = solve_lu_iterative_refinement(A);  % LU + refinement


Each function is self-documented with a bilingual header and can be called independently.  
Cada función incluye cabecera bilingüe y puede llamarse de forma independiente.

Author: srpistolaz0

Released under the **MIT License**.  
Publicado bajo licencia **MIT**.
