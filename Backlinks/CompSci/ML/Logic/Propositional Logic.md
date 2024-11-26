[[Logic]] used to verify the correctness of computer hardware. 

Representations in propositional logic often have a large number of proposition symbols, which represent something that is true or false about a scenario. 

Reasoning algorithms for propositional logic are extremely efficient even the high number of symbols. 

Syntax of propositional logic defines what is allowed and what isn't. 

Atomic sentences are made up of a single preposition symbol which stand for true or false, these are also the two proposition symbols with fixed meaning. 

Complex sentences are made of simple sentences linked with connectives. 

The 5 connectives are:
1. ¬ (not). A sentence such as ¬W1,3 is called the negation of W1,3. A literal is either an atomic sentence (a positive literal) or a negated atomic sentence (a negative literal).
2. ∧ (and). A sentence whose main connective is ∧, such as W1,3 ∧ P3,1, is called a conjunction; its parts are the conjuncts.
3. ∨ (or). A sentence whose main connective is ∨, such as (W1,3 ∧ P3,1) ∨ W2,2, is a disjunction; its parts are disjuncts—in this example, (W1,3 ∧ P3,1) and W2,2.
4. ⇒ (implies). A sentence such as (W1,3 ∧ P3,1) ⇒ ¬W2,2 is called an implication (or conditional). Its premise or antecedent is (W1,3 ∧ P3,1), and its conclusion or consequent is ¬W2,2. Implications are also known as rules or if–then statements. The implication symbol is sometimes written in other books as ⊃ or →.
5. ⇔ (if and only if). The sentence W1,3 ⇔ ¬W2,2 is a biconditional.

# Inference 
Before using automated inference on propositional logic, we need to express the formulas in CNF which has only conjunction, disjunction or literals. 

### Forward chaining

### Backward chaining

### Horn Clauses

