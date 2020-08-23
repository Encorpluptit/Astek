# tests-unitaires-tests-fonctionnels

## Tester un programme.

### Pourquoi ?

Voir que tout fonctionne correctement dans son pgrm.

Filet de sécurité avant chaque push, pour vérifier simplement que l'implémentation du module n'interfère pas avec les autres.

Facilement Intégrable dans de la CI / CD qui de plus en plus accessible.


### Principes de base

4 étapes de tests (lower to upper) :
- Unit Tests (1 component)
    ```text
    UNIT TESTING is a level of software testing where individual units/ components of a software are tested.
    The purpose is to validate that each unit of the software performs as designed.
    A unit is the smallest testable part of any software. It usually has one or a few inputs and usually a single output.
    In procedural programming, a unit may be an individual program, function, procedure, etc.
    In object-oriented programming, the smallest unit is a method, which may belong to a base/ super class, abstract class or derived/ child class.
    (Some treat a module of an application as a unit.    
    This is to be discouraged as there will probably be many individual units within that module.) Unit testing frameworks, drivers, stubs, and mock/ fake objects are used to assist in unit testing.
    ```
- Integration Tests (2 or 3 components)
    ```text
    INTEGRATION TESTING is a level of software testing where individual units are combined and tested as a group.
    The purpose of this level of testing is to expose faults in the interaction between integrated units.
    Test drivers and test stubs are used to assist in Integration Testing
    ```
- System Testing 
   ```text
    SYSTEM TESTING is a level of software testing where a complete and integrated software is tested.
    The purpose of this test is to evaluate the system’s compliance with the specified requirements.
   ```
- Acceptance Testing
   ```text
  ACCEPTANCE TESTING is a level of software testing where a system is tested for acceptability.
  The purpose of this test is to evaluate the system’s compliance with the business requirements and assess whether it is acceptable for delivery.
  ```

http://softwaretestingfundamentals.com/unit-testing/

2 - 3 Citations:

2 Types de tests :
    - Unitaire
    - Fonctionnel


### Test Unitaires

Ideas :

    42 sh - test:
    https://www.youtube.com/watch?v=YvJ6KRrM-tM&list=PLkfO7ZPVsThvW3XRH-Ajp3jk61rz5TgkD&index=6&t=0s

    TDD, Where Did It All Go Wrong:
    https://www.youtube.com/watch?v=EZ05e7EMOLM

#### Principes

Principe :
Unit Tests
    Impératif : Petites Fonctions
    OOP: Méthodes.
    Services: 1 Service

Integration Tests:
    Impératif : Functions de modules (GetFile dans Bsq, Parser dans 42sh, ... )
    OOP: Classe.
    Services: 2 ou 3 Services mis ensembles
    

    
Coder en Pensant à la facilité pour les tests :
    - Arguments
    - Retours
    - Single Responsibility
    - Simplicité de comportement (Facilement testable)
    - Ne pas tester les petites functions qui sont susceptibles de changer mais tester sur les fonctions du dessus dont le comportement est sûr.
    

#### Coverage

- Présentation du report
- Lignes :
    - Exemple avec une condition de return qui n'éxécute pas du code 
- Branches :
    - Exemple de syntaxe if avec 1 condition, puis 2 conditions, ...
    - Voir que c'est puissance de 2 -> Conditions doivent rester simples
- Formats :
    - terminal
    - HTML
    - ...
- Tools: Gcov, (Go), (Haskell)

#### TDD

Principe de coder un test avant même de coder la fonction.

Plus lent à coder la fonction en elle-même,
Plus lent, mais la fonction est déjà réfléchie pour être testée.



TDD, Where Did It All Go Wrong:
    https://www.youtube.com/watch?v=EZ05e7EMOLM

#### Outils

Framework de Test:
    - C: Criterion, CTest, ...
    - C++: Criterion
    - Python: Pytest, unittest, ...
    - Haskell: UnitTest, HUnit, HSpec, ...


### Test Fonctionnels

- System Tests :
Tester le comportement d'un programme.

Qui permettent :
- Acceptance Tests :
Tester / Décider si le programme est prêt pour la release.

#### Principes



#### Outils

Principalement des scripting langages :

    - Bash
    - Python
    - CodeBaseManager

# Contributors
 - Quentin Veyrenc
 - Damien Bernard
 - Mouad Berrehal
 - Benoit Stephant ???
 