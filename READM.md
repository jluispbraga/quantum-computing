# Computação Quântica - Uma pequena introdução
## [Hello world Quântico](bell-state-hello-world.ipynb)

## [Os 4 estados de Bell](four-bell-state.ipynb)
| Estado | Nome (Bell State) | Superposição | Correlação                               | Gate extra                       |
|--------|-------------------|--------------|------------------------------------------|----------------------------------|
| \|Φ⁺⟩ | Phi Plus | (\|00⟩ + \|11⟩) / √2 | 00 ou 11 sempre iguais correlação +      | —                                |
| \|Φ⁻⟩ | Phi Minus | (\|00⟩ − \|11⟩) / √2 | 00 ou 11 sempre iguais fase relativa -1  | Z no q0 depois do Φ⁺             |
| \|Ψ⁺⟩ | Psi Plus | (\|01⟩ + \|10⟩) / √2 | 01 ou 10 sempre opostos correlação anti  | X no q0 depois do Φ⁺             |
| \|Ψ⁻⟩ | Psi Minus | (\|01⟩ − \|10⟩) / √2 | 01 ou 10 sempre opostos fase relativa -1 | X e Z no q0 depois do Φ⁺ (ou iY) |

## Algoritmos Quânticos
- [Algoritmo de Bernstein-Vazirani](bernstein-vazirani-algorithm.ipynb)
- [Algoritmo de Deutsch-Jozsa](deutsch-jozsa-algorithm.ipynb)
- [Algoritmo de Grover](grover-algorithm.ipynb)

## Protocolos Quânticos
- [Teletransporte](teleportation.ipynb)
- [Superdense coding](superdense-coding.ipynb)

### Teletransporte X Superdense coding

|                | Teletransporte           | Superdense coding        |
|----------------|--------------------------|--------------------------|
| Envia          | 1 qubit desconhecido     | 2 bits clássicos         |
| Usa            | 2 bits clássicos + 1 qubit Bell | 1 qubit Bell      |
| Recurso        | par \|Φ⁺⟩ pré-compartilhado | par \|Φ⁺⟩ pré-compartilhado |
| Limitação      | velocidade da luz (bits clássicos) | precisa do qubit físico |

## Ferramentas e suas documentações
- *Qiskit*: [Jupyter](frameworks/qiskit-ibm.ipynb) - [Documentação](https://qiskit.org/documentation/)
- *Cirq*: [Jupyter](frameworks/cirq-google.ipynb) - [Documentação](https://quantumai.google/cirq/start/start)
- *Pennylane*: [Jupyter](frameworks/pennylane-xanadu.ipynb) - [Documentação](https://docs.pennylane.ai/en/stable/)

|                    |Qiskit (IBM)                                         |Cirq (Google)                                      |Pennylane (Xanadu)                                        |  
|--------------------|-----------------------------------------------------|---------------------------------------------------|----------------------------------------------------------|
|Foco principal      |Educação, algoritmos hardwares IBM                   |Controle fino de harware NISQ                      |Quantum ML, diferenciação automática                      |
|Nível de abstração  |Alto - funções pronta para algoritmos comuns         |Baixo - Gates e momentos explícitos                |Médio - Circuits como funções diferenciáveis              |
|Hardware real       |IBM Quantum (acesso free)                            |Google Quantum AI (acesso restrito)                |Plugin para qualquer hardware via plugins                 |
|Curva de aprendizado|Gentil - docs extensos IBM Quantum Composer          |Íngreme - reque base sólida em QC                  | Média - fácil se sabe ML/Pytorch                         |
|Diferencial único   |Ecossistema completo: Nature, Finance, ML            | Momentos = controle total do scheduling           | Gradientes automáticos VQE/QAOA nativos                  |
|Use quando          |Aprender, rodar em hardware real IBM química quântica| Pesquisa Google, compilação customizada, NISQ fino| QML, VQE, QAOA, otimização variacional, hardware agnostic|