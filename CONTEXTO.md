# Contexto del Proyecto — SciML + Neurociencia

## Objetivo
Simular biología neuronal usando Julia + SciML para fijar conocimiento de forma práctica.
El enfoque es: simular para entender, no simular para publicar.

## Por dónde empezar
1. Cascada de señalización de una GPCR (ODEs) — primer proyecto concreto
2. Modelo de Hodgkin-Huxley — potencial de acción neuronal
3. Redes neuronales acopladas — oscilaciones y sincronización
4. STDP — aprendizaje sináptico

## Stack elegido
- **Julia + SciML** (DifferentialEquations.jl, Catalyst.jl, SciMLSensitivity.jl)
- **Pluto.jl** para notebooks reactivos
- Repo: `/home/jemanuelv/workspace/sciml-neuro`

## Papers clave para arrancar
- Izhikevich (2003) "Simple Model of Spiking Neurons"
- Buzsáki & Draguhn (2004) "Neuronal Oscillations in Cortical Networks"
- Rackauckas et al. (2020) "Universal Differential Equations for Scientific Machine Learning"
- Rackauckas et al. (2017) "DifferentialEquations.jl"
- Markram et al. (1997) — STDP original
- Abbott & Nelson (2000) "Synaptic plasticity: taming the beast"

## Libros de referencia
- Dayan & Abbott "Theoretical Neuroscience" — YA LEÍDO
- Izhikevich "Dynamical Systems in Neuroscience" — pendiente

## Perfil del usuario
- Ingeniero mecánico → sistemas dinámicos, ODEs, intuición física
- Procesamiento de señales → datos reales, EEG, filtros
- IA → conoce modelos, no es usuario ciego
- Técnico electrónico → hardware, medición, señales
- Maestría en neurociencias (biológica/investigación) → dominio biológico
- Background ideal para SciML aplicado a dinámica neural

## Notas
- Escala molecular (MD) es computacionalmente cara, mejor empezar por cascada bioquímica (ODEs)
- Herramientas MD si se necesitan: GROMACS, NAMD, OpenMM (Python/C++)
- Catalyst.jl es ideal para redes de reacciones bioquímicas tipo GPCR
