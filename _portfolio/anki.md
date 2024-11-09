---
title: Anki Documentation
permalink: /portfolio/anki/
---
# Introduction to Anki
Anki is an open-source flashcard application that allows people to study flashcards on their computer or smartphone (Android or iOS device). It uses a spaced repetition algorithm to aid in memorization. Anki can be used to study anything from languages to anatomy to history. It has a large user base, especially among people in medical school and people learning foreign languages.

This tutorial will be focusing on features of Anki that are especially useful for people learning Japanese. Its covers how to create flashcards and how to add furigana to flashcards. Additionally, there is a list of popular add-ons that are aimed at people learning Japanese.

# Creating Flashcards
There are two ways to create flashcards in Anki. The first way is to create flashcards within Anki. The second way is to create flashcards in a separate program such as Microsoft Excel and import them into Anki.

## Basic Flashcard Creation

## Importing Flashcards

# Furigana
Furigana are small hiragana characters that can be found above or below kanji characters. They are used to help indicate what the pronunciation of a kanji is. Furigana is helpful for both people learning Japanese as a second language as well as children whose first language is Japanese learning how to read. It can be found in textbooks as well as children’s books. It is also used to in newspapers and novels to indicate the pronunciation of uncommon names.

## Adding Furigana to Flashcards
Furigana can be added to flashcards in Anki. To do this a specific format needs to be followed within the flashcard and a line of code needs to be added to the flashcard’s template.

To add furigana to a flashcard the following syntax has to be used: 
`(space)漢字[かんじ]`

There needs to be a space in front of the kanji so that the furigana renders correctly in Anki. For example:

| Raw Text       | Rendered Text             |
| -------------- | ------------------------- |
| `漢字[かんじ]`  | <ruby><rb>漢字</rb><rt>かんじ</rt></ruby> |
| `食[た]べ 物[もの]` | <ruby><rb>食</rb><rt>た</rt></ruby>べ<ruby><rb>物</rb><rt>もの</rt></ruby> |

Note that there is a space between べ 物 which allows the furigana (もの) to render correctly. If the space wasn't there the rendered text would be <ruby><rb>食</rb><rt>た</rt>べ<rb>物</rb><rt>もの</rt></ruby>.

## Formatting Templates

# Popular Add-ons for Japanese Flashcards