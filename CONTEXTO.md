# Contexto del Proyecto — SciML + Neurociencia

## Objetivo
Simular biología neuronal usando Julia + SciML para fijar conocimiento de forma práctica.
El enfoque es: **simular para entender, no simular para publicar**.
La simulación es la forma de fijar el conocimiento biológico — equivalente a simular un circuito RLC para entender electrónica.

## Estado actual
- Repo creado: `/home/jemanuelv/workspace/sciml-neuro`
- GitHub: https://github.com/jemanuelv/sciml-neuro
- Estructura de carpetas lista, nada de código todavía
- **Próximo paso: empezar con 01_gpcr — cascada de señalización**

## Estructura del repo
```
sciml-neuro/
├── 01_gpcr/          ← EMPEZAR ACÁ
├── 02_hodgkin_huxley/
├── 03_oscilaciones/
├── 04_stdp/
└── utils/
```

## Hoja de ruta
1. **GPCR — cascada de señalización** (ODEs con Catalyst.jl)
   - Cinética ligando-receptor
   - Cascada intracelular: proteína G → cAMP → PKA
   - Efecto sobre canales iónicos / excitabilidad neuronal
2. **Hodgkin-Huxley** — potencial de acción neuronal
3. **Redes neuronales acopladas** — oscilaciones y sincronización
4. **STDP** — aprendizaje sináptico

## Stack elegido
- **Julia** (no Python — Julia gana claramente en simulación de ODEs biológicas)
- **DifferentialEquations.jl** — solver de ODEs
- **Catalyst.jl** — redes de reacciones bioquímicas (ideal para GPCR)
- **SciMLSensitivity.jl** — inferencia de parámetros
- **Pluto.jl** — notebooks reactivos (equivalente Julia de Jupyter, pero reactivo)

## Por qué Julia y no Python
- DifferentialEquations.jl y SciML no tienen equivalente real en Python
- Catalyst.jl es específico para bioquímica
- El objetivo es dinámica y simulación, no ML clásico
- Python se usaría si el objetivo fuera ML general

## Escala molecular (MD) — descartada por ahora
- Computacionalmente muy cara (clusters de GPUs, días de cómputo)
- Herramientas si se necesitan en el futuro: GROMACS, NAMD, OpenMM (Python/C++), Molly.jl
- Alternativa accesible: PyMOL/VMD para visualización estática de estructura 3D
- Mejor estrategia: empezar por cascada bioquímica (ODEs) que corre en laptop en minutos

## Papers clave
- Izhikevich (2003) "Simple Model of Spiking Neurons" — IEEE Trans. Neural Networks
- Buzsáki & Draguhn (2004) "Neuronal Oscillations in Cortical Networks" — Science
- Breakspear (2017) "Dynamic models of large-scale brain activity" — Nature Neuroscience
- Markram et al. (1997) — STDP original
- Abbott & Nelson (2000) "Synaptic plasticity: taming the beast" — Nature Neuroscience
- Rackauckas et al. (2020) "Universal Differential Equations for Scientific Machine Learning"
- Rackauckas et al. (2017) "DifferentialEquations.jl"
- Hodgkin & Huxley (1952) — el original, vale leerlo

## Libros de referencia
- Dayan & Abbott "Theoretical Neuroscience" — **YA LEÍDO**
- Izhikevich "Dynamical Systems in Neuroscience" — pendiente (recomendado, muy geométrico)
- "Neural Data Analysis" de Kass, Eden & Brown — para señales electrofisiológicas

## Perfil del usuario
- **Ingeniero mecánico** → intuición física, sistemas dinámicos, ODEs
- **Procesamiento de señales** → datos reales con ruido, EEG/MEG, filtros
- **IA** → conoce modelos, no es usuario ciego de la herramienta
- **Técnico electrónico** → hardware, medición, señales reales
- **Maestría en neurociencias** (orientación biológica/investigación)
- 45 años, perfil multidisciplinario — exactamente el perfil ideal para SciML + neuro
- El valor está en la formulación del problema (dominio) + Claude para el código

## Cómo trabajar con Claude en este repo
- El usuario entiende el dominio, Claude escribe y depura el código
- Cuando algo no tiene sentido biológicamente, el usuario lo detecta
- Claude puede leer papers y documentación que se le pasen en la conversación
- Julia es nuevo para el usuario — Claude explica sintaxis cuando es necesario
