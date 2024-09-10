---
title: GAN についてまとめてみた
emoji: 
type: tech (or idea)
topics: ['GAN', '機械学習', 'Python']
published: False
---

# Generative Adversarial Networks についてまとめてみた
## まずは GAN の基本から
- GANとは以下の2つを基本としている
  - Generator(生成器)
    - 入力として無作為な分布を受け取り、何らかのデータを出力する
    - 新しい画像などの生成のために使うことができる
  - Discriminator(識別機)
    - 入力として生成器が作った偽のデータか訓練データものか判断する
- それぞれの役割は相反している
  - 判別機は本物のデータと偽物のデータを見分けようとする
  - それに対し、生成期はよりリアルなデータを生成しようとする
- 2つに分かれた訓練イテレーション
  - 

### Discriminator の学習
- 