---
uid: Microsoft.Quantum.ResourceEstimation.BeginEstimateCaching
title: BeginEstimateCaching function
ms.date: 6/5/2023 12:00:00 AM
ms.topic: managed-reference
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ResourceEstimation
qsharp.name: BeginEstimateCaching
qsharp.summary: >-
  Informs the resource estimator of the start of the code fragment
  for which estimates caching can be done. This function
  is only available when using resource estimator execution target.
---

# BeginEstimateCaching function

Namespace: [Microsoft.Quantum.ResourceEstimation](xref:Microsoft.Quantum.ResourceEstimation)

Package: [Microsoft.Quantum.QSharp.Foundation](https://nuget.org/packages/Microsoft.Quantum.QSharp.Foundation)


Informs the resource estimator of the start of the code fragmentfor which estimates caching can be done. This functionis only available when using resource estimator execution target.

```qsharp
function BeginEstimateCaching (name : String, variant : Int) : Bool
```


## Input

### name : [String](xref:microsoft.quantum.qsharp.valueliterals#string-literals)

The name of the code fragment. Used to distinguish it from other code fragments.Typically this is the name of the operation for which estimates can be cached.


### variant : [Int](xref:microsoft.quantum.qsharp.valueliterals#int-literals)

Specific variant of the execution. Cached estimates can only be reused if thevariant for which they were collected and the current variant is the same.



## Output : [Bool](xref:microsoft.quantum.qsharp.valueliterals#bool-literals)

`true` indicated that the cached estimates are not yet avialable and the code fragmentneeds to be executed in order to collect and cache estimates.`false` indicates if cached estimates have been incorporated into the overall costsand the code fragment should be skipped.