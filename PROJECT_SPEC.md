# Project Specification

This app must be a Klauer/Phye inductive reasoning trainer, not a generic ARC viewer.

## Core Method

Klauer/Phye inductive reasoning is based on six operations:

| Branch | Similarity | Difference | Similarity + Difference |
|---|---|---|---|
| Attributes | Generalization | Discrimination | Cross-classification |
| Relations | Recognizing relationships | Differentiating relationships | System construction |

Every task mode must explicitly map to one of these six operations.

## Data Source

Primary source:

- ARC-AGI JSON tasks from ARC-AGI-1.0.2/data/training
- ARC-AGI JSON tasks from ARC-AGI-1.0.2/data/evaluation

Reference only:

- ARC-AGI-1.0.2/apps
- ARC-AGI-1.0.2/apps/testing_interface.html if present
- ARC-AGI-1.0.2/apps/js if present

Future optional source:

- Re-ARC generated JSON packs

## Important Principle

The app must not be a simple ARC puzzle viewer.

It must use ARC-AGI tasks as raw material for a full Klauer/Phye inductive reasoning training system.

The user must train all six operations:

1. Generalization
2. Discrimination
3. Cross-classification
4. Recognizing relationships
5. Differentiating relationships
6. System construction

## Required App

Build a single-file index.html containing HTML, CSS, and JavaScript.

The app must work by opening index.html directly in the browser.

No backend.
No build step.
No paid APIs.
No external dependencies unless absolutely necessary.

## Required Modes

### 1. Generalization Mode

The user identifies the common rule across train examples.

### 2. Discrimination Mode

The user identifies a corrupted example, wrong output, or rule-violating case.

### 3. Cross-classification Mode

The user classifies transformations, objects, or rules by two axes.

### 4. Recognizing Relationships Mode

The user identifies the input-output relation.

### 5. Differentiating Relationships Mode

The user finds which relation or transformation differs from the others.

### 6. System Construction Mode

The user solves a full ARC task by constructing the output grid.

## Required Features

- ARC grid renderer
- ARC JSON loading
- Manual output grid editor
- Multiple-choice rule questions
- Task metadata inference
- Adaptive difficulty engine for adults
- Error journal
- Statistics by Klauer operation
- LocalStorage progress saving
- Explanation after answer
- Review mode for failed task types
- Difficulty should increase by rule complexity, grid complexity, number of objects, number of colors, distractor strength, and answer format.

## Adaptive Difficulty

Difficulty must not simply increase by task count.

It should adapt using:

- accuracy
- response time
- operation type
- number of failed attempts
- rule complexity
- grid size
- distractor strength
- whether the user solved by multiple choice or manual output construction

## Metadata

Each task should internally track:

- id
- source
- Klauer operation
- branch: attributes or relations
- comparison type: similarity, difference, or similarity+difference
- rule type
- difficulty
- distractor type
- explanation
- user error type

## Final Goal

Create a serious adult-level inductive reasoning trainer that fully operationalizes Klauer/Phye using ARC-AGI/Re-ARC-style tasks.
