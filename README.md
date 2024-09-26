# Interpretable_ML_Classification
Explanation for each interpretable machine learning method

## RuleTrees
Reference: https://techdocs.akamai.com/property-mgr/reference/rule-trees

Every rule tree opens with a top-level rules element that specifies a mandatory default rule object. If you want to further adjust how your content is served over the edge network, you can add a children array of nested rule objects, where you specify individual behaviors and optional criteria. PAPI supports a catalog of writable behaviors and criteria with templated values that offer guide rails for easier implementation. However, if you need additional dedicated settings that regular behaviors can't express, an Akamai representative can build a custom feature in XML for you.

Rules are evaluated from top to bottom.
* A rule first evaluates its criteria, then, if the set of criteria matches, executes its behaviors and nested children.
* If any behavior is specified more than once within a set of executing rules, the last one overrides those that precede it.
* In some cases the ordering of different behaviors that perform similar functions may also matter.
* In other cases you can re-use the same behavior to do different things that don't conflict with each other, for example, by modifying one HTTP header and then a different one.

## Greedy Rule List
Reference: https://csinva.io/imodels/rule_list/greedy_rule_list.html


A greedy rule list is a machine learning algorithm that splits on one feature at a time along a single path to find rules that maximize the probability of class 1. It is currently only supported for binary classification. 

## OneR
Reference: https://www.saedsayad.com/oner.htm 
For each predictor,
     For each value of that predictor, make a rule as follows;
           Count how often each value of target (class) appears
           Find the most frequent class
           Make the rule assign that class to this value of the predictor
     Calculate the total error of the rules of each predictor
Choose the predictor with the smallest total error.
