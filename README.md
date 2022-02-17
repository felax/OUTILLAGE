``` mermaid
graph TD

A2(Contrôle):::top
A2 --- B2(Gestion derreurs):::mid
    B2 --- C2(Schéma états)
    B2 --- D2(Implémentation)
    B2 --- E2(Plan de test)
    B2 --- F2(Tester)
A2 --- G2(Contrôle source):::mid
    G2 --- H2(Schéma<br>communication)
    G2 --- I2(Implémenter)
    G2 --- J2(Test sans source)
    G2 --- K2(Tester<br>technicien)
A2 --- L2(Alimentation basse tension):::mid
    L2 --- M2(Trouver solution)
    L2 --- N2(Interfacer avec proto)
B2 ---- O2(Mesure disolement):::mid
    O2 --- P2(Assembler)
    O2 --- Q2(Tester)
B2 ---- R2(Boucle HVIL):::mid
    R2 --- S2(Identifier module)
    R2 --- T2(Integrer avec controle)


classDef top fill:#F7D59C,stroke:#5E454B,color:#000
classDef mid fill:#CEE5D0,stroke:#5E454B,color:#000
classDef default fill:#F3F0D7,stroke:#5E454B,color:#000

```
