# Sinkless orientation in dynamic-LOCAL

## Context

Distributed graph algorithms; [dynamic-LOCAL model](https://arxiv.org/abs/2109.06593) (edge additions only).

Task: sinkless orientation (find an orientation so that nodes of degree at least 3 have outdegree at least 1).

## Highlight results

The locality of sinkless orientation is:

- $O(\log \log n)$ in deterministic dynamic-LOCAL
- $O(\log \log \log n)$ in randomized dynamic-LOCAL (oblivious adversary).

## Prior work

The same bounds were previously known in SLOCAL and online-LOCAL, but not in dynamic-LOCAL.

## Documents

- [AI-generated write-up](writeup.pdf)
- [Human-written notes](human-notes.md)

## Discovered by

GPT-6 in Codex

## Communicated by

[Jukka Suomela](https://jukkasuomela.fi)

## Confidence

The algorithm idea is simple and makes sense to me.
