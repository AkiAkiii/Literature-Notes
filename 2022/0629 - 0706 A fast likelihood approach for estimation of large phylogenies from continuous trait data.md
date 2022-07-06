# Overview

## Goal

developing methods for for phylogenetic inference using continuous trait data (can we understand it as a classification problem?)

## Method Mechanism

The approximation works by first computing the maximum likelihood estimates of some internal branch lengths, and then inferring the tree-topology using these estimates

## Fill in gap: 
1. more computationally efficient than existing methods for such data while still achieving comparable accuracy

2. Though distance and parsimony methods are computationally fast, they can *produce incorrect estimates of the topology* when **the rates of 
evolution are unequal across lineages**, even with an infinite number of 
sites
## Innovation:
use of the mathematical properties of tree-topologies for inference, and thus serves as a useful addition to the collection of methods available for estimating phylogenies from continuous trait data. 

## Background

- Inference of phylogenies from genetic data


# Methods

## 2.1 The Brownian motion model for continuous trait evolution 

ref reading: https://lukejharmon.github.io/pcm/chapter3_bmintro/#:~:text=We%20can%20use%20Brownian%20motion,distance%2C%20over%20any%20time%20interval

### What is this model doing? 
--> transformation of the observed values of the continuous traits so that the trandsformed values are about normal.

### Common transformation function g: 

a) angular transformation. (remove inhomogeneity of the variance, generally performs well when gene frequencies are not extreme)

b) logistic transformation

### what is the optimal tree?

The tree that maximizes the likelihood based on the normal distribution above

## 2.2 Root distances

### What is part doing? 

use a property of a tree-topology that it is completely characterized by what we call the root distances, defined as follows. (for the proposed approximate likelihood method to infer phylogenies)

In details, the method estimate the covariance matrix of the Brownian motion model in `2.1`. That is:

R is a PxP matrix with RD_x,y as its elements. the covariance matrix of the Brownian motion model = R


## 2.3 Root Distance Method (RDM) 

### Step 1:  Estimating the differences ΔRDx:y,z

MLE of covariance matrix in (2.1) from the allele frequency data

MLE of ΔRDx:y,z :  ̂ ΔRDx:y,z

### Step 2: Determining the ̂ ΔRDx:y,z values closest to zero

set the lowest H of the observed Δ̂RDk:i,j to 0 for each triplet, and these are used as input to Step 3

### Step 3: Identifying the splits from zero-valued Δ̂RD.

By comparing the taxa involved in splits identified by zero-valued ΔRD, one can identify splits that are equivalent. Once all 
equivalencies are determined, a set of distinct splits is identified. 

result: reduced set G (the set of all distinct splits)

add any missing two-taxon splits to G 

### Step 4: Estimating the tree-topology from the splits

#### What is this step doing?

assemble the split set G into a resolved binary tree

#### transform G into a split indicator matrix

## 2.4 simulation

1. `rtree()` simulate an unrooted tree

2. compute the R matrix by calculating the root distances (defination see 2.2)

3. simulate allele frequencies r based on Brownian Motion model.

4. Estimate the tree from (3) simulated data using RDM.

5. repeat 1-4

# Defination

## 0. what is 'phylogenies'?

Phylogenies are important for studying the relationships among taxa of interest, thus providing insight into the historical processes that have contributed to their evolution.

## How are taxa related to each other?

Terminal taxa are connected by branches. The branches are the line segments that make up the tree. Branches come together at branching points called nodes. Each nodes represents a common ancestor shared by two or more terminal taxa.

Recommand reading to learn more background knowledge: Reading Trees  https://www.digitalatlasofancientlife.org/learn/systematics/phylogenetics/reading-trees/#:~:text=Terminal%20taxa%20are%20connected%20by,two%20or%20more%20terminal%20taxa.

## 1. what is 'continuous trait data'?

A continuous trait displays a range of expression (such as weight, height, etc.) rather than an all-or-none appearance (such as white or red). Continuous traits are usually under polygenic control and subject to substantial environmental influence in expression.

## 2. what is 'allele frequency data'?

An allele frequency is calculated by dividing the number of times the allele of interest is observed in a population by the total number of copies of all the alleles at that particular genetic locus in the population. Allele frequencies can be represented as a decimal, a percentage, or a fraction.

Allele: one of two or more alternative forms of a gene that arise by mutation and are found at the same place on a chromosome.

## 3. Multivariate normal distribution (joint normal distribution)

a random vector is said to be k-variate normally distributed if every linear combination of its k components has a univariate normal distribution. Its importance derives mainly from the multivariate central limit theorem. The multivariate normal distribution is often used to describe, at least approximately, any set of (possibly) correlated real-valued random variables each of which clusters around a mean value.

## 4. What does 'tips' mean?

## 5. What is 'most recent common ancestor (MRCA)' ?

## 6. What is taxa?

## 7. What is 'locus'?

A locus, as related to genomics, is a physical site or location within a genome (such as a gene or another DNA segment of interest), somewhat like a street address. The plural of locus is loci. （https://www.genome.gov/genetics-glossary/Locus ）

## 8. tips of the tree

the end of the tree

https://www.nature.com/scitable/topicpage/reading-a-phylogenetic-tree-the-meaning-of-41956/

![image](https://user-images.githubusercontent.com/90790297/177446453-ca0a502a-ae4b-4aa6-809d-a9709e94d798.png)


![image](https://user-images.githubusercontent.com/90790297/177447148-faf308c0-a2b0-42d7-8aa8-e359a60a3a72.png)

![image](https://user-images.githubusercontent.com/90790297/177447449-d6a340e7-2088-4a27-b21b-c451c67bc773.png)

Regardless of their rank, the taxa depicted in a phylogenetic tree are often called terminal taxa, because they occur at the tips of the tree. They are sometimes referred to as "terminals" or "leaves."

![image](https://user-images.githubusercontent.com/90790297/177446740-1e1c3126-cbdf-4bbb-a584-5186a54da1d7.png)

## 9. What is tree-topology?

## 10. What is outgroup?





