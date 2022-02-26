# PERT
``` mermaid
graph LR
    A(Plans de test<br>source):::prog
    B(Validation<br>Khaled Arfa):::prog
    C(Plan de tests <br>source révisés)
    D(Tests avec<br>technicien)
    E(Modalités test):::prog
    F(Commande de <br>la source):::prog
    G(Rédaction <br> rapport final)
    H(Analyse durée<br>de vie):::prog
    I(Vérification<br>RoHS):::prog
    J(Recherche <br> Homologation):::prog
    K(Transition <br> proto-final):::prog
    L(Schéma états):::prog
    M(Implémentation)
    N(Tests module <br> contrôle)
    O(Assemblage <br> mesure isolement)
    P(Plans de test <br> mesure isolement):::done
    Q(Identifier <br> module HVIL):::prog
    R(Intégration <br> HVIL-MD4)
    S(Schéma <br> communication <br> source-MD4):::prog
    T(Implémentation <br> communication)
    U(Choix fusibles <br> et intégration):::prog
    V(Design, impression <br> caps HVIL)
    W(Usinage, assemblage <br> boite jonction)
    Y(Test boite <br> jonction)
    Z(Design <br> boîtier PCB):::done

    a(Impression, <br> assemblage <br> boîtier PCB)
    b(Choix PDB):::prog
    c(Commande PDB)
    e(Adapter boite <br>jonction):::prog
    d(Remise <br> rapport final)
    f(Commande <br> boite jonction)
    g(Commande <br> PCB isolement):::prog
    h(Commande <br> connecteurs):::prog
    
    B --> |1| C
    C --> |1| D
    E --> |1| D
    F ----> |4| D
    D --> |1| G
    H --> |1| G
    I --> |1| G
    J --> |1| G
    K --> |1| G
    L --> |1| M
    M --> |1| N
    N --> |1| D
    O --> |1| N
    P --> |1| N
    Q --> |1| R
    R --> |1| N
    S --> |1| T
    T --> |1| N
    h --> |2| V
    V --> |1| Y
    W --> |1| Y
    e --> |1| f
    f --> |1| W
    Y --> |1| G
    Z --> |1| a
    a --> |1| G
    b --> |1| c
    c --> G
    g -->|3| O
    A --> |1| B
    G --> |1| d
    U --> |1| Y

classDef done stroke:MediumSeaGreen,stroke-width:2px;
classDef prog stroke:Orange,stroke-width:2px;
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
