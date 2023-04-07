# rust_alpha

This is my attempt at writing a compiler for the Alpha-Notation used in my Systemnahe Informatik lecture at university.

## Current status

Internal handling of instructions is finished, now the "compiler" needs be be written.

## TODO

- [ ] Make it possible to customize the available memory cells (preferably by adding an option to the gui)
- [ ] Make progamm work with GUI 
	- [ ] (Customization of available accumulators)
	- [ ] (Customization of available memory cells)
		- if no memory cells are set all commands that require memory cells should be disabled ("compiling" with those commands included should fail)	
- [ ] Debug mode -> Step through each instruction
- [ ] Add tests (at least one for each command)

### Instructions

Be $k,u,v\in\mathbb{Z};n\in\mathbb{N}|n\geq0:i,j\in\lbrace h_0,\ldots,h_n\rbrace;op\in\lbrace +,-,*,/\rbrace;cmp\in\lbrace <,\leq,=,\geq,>\rbrace$

#### Text parsing to instruction

This section logs what instructions can be parsed from text

- [ ] $\alpha_u:=\alpha_v$
- [ ] $\alpha_u:=\rho(i)$
- [ ] $\rho(i):=\alpha_u$
- [ ] $\rho(i):=k$
- [ ] $\alpha_u:=k$
- [ ] $\alpha_u:=\alpha_u\space\textbf{op}\space k$
- [ ] $\alpha_u:=\alpha_u\space\textbf{op}\space\alpha_v$
- [ ] $\alpha_u:=\alpha_v\space\textbf{op}\space\alpha_w$
- [ ] $\alpha_u:=\alpha_u\space\textbf{op}\space \rho(i)$
- [ ] $\alpha_u:=\rho(i)\space\textbf{op}\space \rho(j)$
- [ ] $\rho(i):=\rho(j)\space\textbf{op}\space k$
- [ ] $\rho(i):=\rho(j)\space\textbf{op}\space\alpha_u$
- [ ] $\rho(i):=\rho(j)$
- [ ] if $\alpha_u\space\textbf{cmp}\space\alpha_v$ then goto label
- [ ] if $\alpha_u\space\textbf{cmp}\space k$ then goto label
- [ ] if $\alpha_u\space\textbf{cmp}\space\rho(i)$ then goto label
- [ ] goto label 
- [ ] push 
- [ ] pop

#### Internal handling of instructions 

This section logs what instructions are implemented in the backend

- [X] $\alpha_u:=\alpha_v$
- [X] $\alpha_u:=\rho(i)$
- [X] $\rho(i):=\alpha_u$
- [X] $\rho(i):=k$
- [X] $\alpha_u:=k$
- [X] $\alpha_u:=\alpha_u\space\textbf{op}\space k$
- [X] $\alpha_u:=\alpha_u\space\textbf{op}\space\alpha_v$
- [X] $\alpha_u:=\alpha_v\space\textbf{op}\space\alpha_w$
- [X] $\alpha_u:=\alpha_u\space\textbf{op}\space \rho(i)$
- [X] $\alpha_u:=\rho(i)\space\textbf{op}\space \rho(j)$
- [X] $\rho(i):=\rho(j)\space\textbf{op}\space k$
- [X] $\rho(i):=\rho(j)\space\textbf{op}\space\alpha_u$
- [X] $\rho(i):=\rho(j)$
- [X] if $\alpha_u\space\textbf{cmp}\space\alpha_v$ then goto label
- [X] if $\alpha_u\space\textbf{cmp}\space k$ then goto label
- [X] if $\alpha_u\space\textbf{cmp}\space\rho(i)$ then goto label
- [X] goto label 
- [X] push 
- [X] pop
