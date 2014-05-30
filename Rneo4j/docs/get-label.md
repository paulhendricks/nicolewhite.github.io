---
title: getLabel
layout: rneo4j
---

`getLabel`

# Node Labels

## Description

Get all node labels for a given node object or for the entire graph database.

## Usage

```r
getLabel(object)
```

## Arguments

| Parameter | Description     |
| --------- | --------------- |
| `object`  | An object for which to view all node labels. Accepts a node or graph object (see details). |

## Output

A character vector.

## Details

Supplying a graph object returns all node labels in the graph database. Supplying a node object returns all node labels for the given node.

## Examples

```r
alice = createNode(graph, name = "Alice")
bob = createNode(graph, name = "Bob")

addLabel(alice, "Student")
addLabel(bob, "Person", "Student")
```

Get all labels on the `alice` node.

```r
getLabel(alice)

# [1] "Student"
```

Get all node labels in the graph database.

```r
getLabel(graph)

# [1] "Student" "Person"
```

## See Also

[`addLabel`](add-label.html), [`dropLabel`](drop-label.html)