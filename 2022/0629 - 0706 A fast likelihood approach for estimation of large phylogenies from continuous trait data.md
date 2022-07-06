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

## 2.2 Root distances


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

![image](https://user-images.githubusercontent.com/90790297/177446539-901184ba-4cd7-4880-9910-aab5b02fa9b9.png)

![image](https://user-images.githubusercontent.com/90790297/177446740-1e1c3126-cbdf-4bbb-a584-5186a54da1d7.png)


