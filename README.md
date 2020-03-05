# ltlrewrite
Rewriting Based Finite Trace Checker for LTL 

# Usage

```./ltlrewrite.native "F (q -> G r)" ```

You can then feed the events and see the corresponding rewritten formula and simplication formula.

```
./ltlrewrite.native "F (q -> G r)"
======================================== 
Entered LTL Formula: F (q -> G r)
======================================== 
Enter the Event: p q
======================================== 
Pure Rewrite Step: ((- (True) | (False & G r)) | F (q -> G r))
Simplified Form: F (q -> G r)
======================================== 
 Enter the Event: p
======================================== 
Pure Rewrite Step: ((- (False) | (False & G r)) | F (q -> G r))
Simplified Form: True
======================================== 
**** STOPPING: Further rewriting will not change the evaluation **** 
```
