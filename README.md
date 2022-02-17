# Source
``` mermaid
graph TD
A(Source):::top 
A --- B(Source proto):::mid
    B --- C(Quote pour une source)
    B --- D(Passer la commande)
    B --- E(Plans de test):::mid
        E --- F(Plan de tests temp):::mid
            F --- G(Puissance maximale)
            F --- H(Ondulations de tension)
            F --- I(Réponse transitoire)
            F --- J(Temps de monté)
            F --- K(Surcharge/court-circuit)
        E --- L(Validation<br>Khaled Arfa)
        E --- M(Plans de tests finaux)
    B --- N(Tester la source):::mid
        N --- O(Modalités de test<br>Khaled Arfa)
        N --- P(Effectuer les tests<br>technicien)
A --- Q(Solution finale):::mid
    Q --- R(Analyse durée de vie <br>composants)
    Q --- S(Vérification RoHS)
    Q --- T(Recherche homologation )
    Q --- U(Transition<br>prototype->final)

classDef top fill:#F7D59C,stroke:#5E454B,color:#000
classDef mid fill:#CEE5D0,stroke:#5E454B,color:#000
classDef default fill:#F3F0D7,stroke:#5E454B,color:#000
```

# Contrôle
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

# Mécanique
``` mermaid
graph TD
a(Mécanique):::top
a --- b(Caps HVIL):::mid
    b --- c(Design)
    b --- d(Impression)
    b --- e(Test)
a --- f(Boîte de jonction):::mid
    f --- g(Machinage)
    f --- h(Assemblage)
    f --- i(Tester):::mid
        i --- j(Connecteurs)
        i --- k(Rigidité)
a --- l(Housing PCB):::mid
    l --- m(Design)
    l --- n(Impression)
    l --- o(Assemblage)
a --- p(Wiring):::mid
    p --- q(Power Distribution Block)
    p --- r(Crimping)
    
classDef top fill:#F7D59C,stroke:#5E454B,color:#000
classDef mid fill:#CEE5D0,stroke:#5E454B,color:#000
classDef default fill:#F3F0D7,stroke:#5E454B,color:#000
```
