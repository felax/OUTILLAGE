# PERT
``` mermaid
graph LR
    A(Plans de test<br>source) --> |1| B(Validation<br>Khaled Arfa)
    B --> |1| C(Plan de tests <br>source révisés)
    C --> |1| D(Tests avec<br>technicien)
    E(Modalités test) --> |1| D
    F(Commande de <br>la source) ----> |4| D
    D --> |2| G

    H(Analyse durée<br>de vie) --> |1| G(Rédaction <br> rapport final)
    I(Vérification<br>RoHS) --> |1| G
    J(Recherche <br> Homologation) --> |1| G
    K(Transition <br> proto-final) --> |1| G

    L(Schéma états) --> |1| M(Implémentation)
    M --> |1| N(Tests module <br> contrôle)
    N --> |1| D
    g(Commande <br> PCB isolement) -->|3| O
    O(Assemblage <br> mesure isolement) --> |1| N
    P(Plans de test <br> mesure isolement) --> |1| N
    Q(Identifier <br> module HVIL) --> |1| R(Intégration <br> HVIL-MD4)
    R --> |1| N
    S(Schéma <br> communication <br> source-MD4) --> |1| T(Implémentation <br> communication)
    T --> |1| N

    U(Design <br> caps HVIL) --> |1| V(Impression <br> caps HVIL)
    V --> |1| Y(Test boite <br> jonction)
    W(Usinage, assemblage <br> boite jonction) --> |1| Y
    e(Choix boite <br>jonction) --> |1| f(Commande <br> boite jonction)
    f --> |1| W
    X --> |1| Y
    Y --> |1| G

    Z(Design <br> boîtier PCB) --> |1| a(Impression, <br> assemblage <br> boîtier PCB)
    a --> |1| G
    b(Choix PDB) --> |1| c(Commande PDB)
    c --> G

    G --> |2| d(Remise <br> rapport final)
```

# Source
``` mermaid
graph LR
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
graph LR
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
graph LR
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
