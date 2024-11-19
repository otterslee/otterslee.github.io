---
title: Generative Model 이란?
categories: [Computer vision, Generative model]
tags: [generative model, discriminative model]
use_math: true
---
## Introduction

---



AI 분야에서 생성모델에 대한 연구가 활발합니다. 이제는 많이들 사용하고 계실 OpenAI의 chatGPT부터 원하는 이미지를 만들고 편집할 수 있는 Stable Diffusion까지 연구 뿐만 아니라 산업이나 응용 측면에서도 활용되고 있습니다. 이 Diffusion 모델이란 무엇일까에 대해 공부한 내용을 정리해 공유하려 합니다. 이번 글에서는 생성모델이 무엇인지, 그 종류에는 무엇이 있는지 살펴본 뒤, 가장 자주 쓰이는 구조인 GAN과 VAE까지 살펴보도록 하겠습니다.

## Discriminative VS Generative

---

#### 판별 모델

판별 모델(Discriminative model)은 데이터 $X$가 주어졌을 때 label $Y$가 나타날 조건부확률 $p(Y \vert X)$를 예측하는 모델을 의미하며, 분류모델이라고 불리기도 합니다. label $Y$가 사용되므로 지도학습(Supervised Learning)에 포함됩니다.

#### 생성 모델

생성 모델(Generative model)을 한마디로 정리하면, <mark style='background-color: #dcffe4'> input $x$의 데이터 분포 $p(x)$를 추정</mark>하는 모델입니다.
