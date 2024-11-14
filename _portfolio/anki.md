---
title: Anki Documentation
permalink: /portfolio/anki/
toc: true
toc_sticky: true
---
[Anki](https://apps.ankiweb.net/) is an open-source flashcard application that allows people to study flashcards on their computer or smartphone (Android or iOS device). It uses a spaced repetition algorithm to aid in memorization. Anki can be used to study anything from languages to anatomy to history. It has a large user base, especially among people in medical school and people learning foreign languages.

This tutorial is focused on features of Anki that are especially useful for people learning Japanese. It covers how to create flashcards and how to add furigana to flashcards. Additionally, there is a list of popular add-ons that are aimed at people learning Japanese.

# Create Flashcards
There are two ways to create flashcards in Anki. The first way is to create flashcards within Anki. The second way is to create flashcards in a separate program such as LibreOffice and import them into Anki.

## Basic Flashcard Creation
![Main anki window](/assets/images/anki/ankimain.png)
The most basic way of creating flashcards is to create them within Anki itself. To do this click the **Add** button at the top of the window. 

![Window to create flashcards](/assets/images/anki/ankiadd.png)
Once Add has been clicked a small window will open. In this window you will find:
1. The type of flashcard you are adding and the deck deck that the flashcard will be in (these can be changed by clicking the buttons)
2. Text editing options
3. The fields of the card

 To create a new flashcard, enter the text that you want to see in the individual fields of the card and click **Add**.
> &#128221; **Note:** The type of flash card in the picture above only has two fields which are labeled front and back. To add text to the front side of the card (which is the first side that you will see when learning or reviewing the card) enter text into the textbox under “Front”. To add text to the back side of the card (which is the second side that you will see when learning or reviewing the card) enter text into the textbox under “Back”.

## Import Flashcards
To import flashcards that you have made into Anki, the file needs to be saved as a CSV file in a “UTF-8 encoding”. For that reason, Anki recommends that people create flashcards this by using [Libreoffice](https://www.libreoffice.org/) to create a spreadsheet. Anki treats each column of the spreadsheet as a text field and each new row as a new card.

![Screenshot of spreadsheet with six rows of text](/assets/images/anki/spreadsheet.png)

In the image above, Anki will default to mapping column A as the “front” field and column B as the “back” field. 

![CSV options](/assets/images/anki/csvoptions.png)

To save the spreadsheet as a CSV in LibreOffice, go to *File>Save As* and  select CSV as the file type.\
 After the file name and location have been chosen and save has been clicked, a window like the above will appear. This shows the default CSV options. The default field delimiter is a comma (,). This can be changed to a semi-colon (;), colon (:), tab, or a space. If your definition field has commas you will want to change the delimiter, ideally to a semi-colon, colon, or tab.

To import the saved CSV file open the Anki application and go to *File>Import*, select the CSV file, and click **Open**.

![Anki import window](/assets/images/anki/importfilewindow.png)

After clicking open you will see a window similar to the above. Here you will see:
1. The field separator – this allows you to choose what separates different fields within the file. It will default to what was chosen as the delimiter when the CSV file was created.
2. A visual representation in the form of a table of what Anki recognizes as flash cards. This should look similar to the spreadsheet that was created in LibreOffice.
3. The import options. These options allow you to choose what notetype and deck the notes should be assigned to, what Anki should do if it finds duplicate flashcards (these are called “notes” by Anki), and what tags should be added to the flashcards (the default is to not add tags).
4. What fields each column maps to. These can be changed by clicking the drop-down menus on the right.

When you are satisfied with the settings in the Import File window, click **Import** to add the files to your chosen deck.

# Furigana
Furigana are small hiragana characters that can be found above or below kanji characters. They are used to help indicate what the pronunciation of a kanji is. Furigana is helpful for both people learning Japanese as a second language as well as children whose first language is Japanese and are learning how to read. It can be found in textbooks as well as children’s books. It is also used to in newspapers and novels to indicate the pronunciation of uncommon names.

## Add Furigana to Flashcards
Furigana can be added to flashcards in Anki. To do this a specific format needs to be followed within the flashcard and a line of code needs to be added to the flashcard’s template.

To add furigana to a flashcard the following syntax has to be used: 
`(space)漢字[かんじ]`

There needs to be a space in front of the kanji so that the furigana renders correctly in Anki. For example:

| Raw Text       | Rendered Text             |
| -------------- | ------------------------- |
| `漢字[かんじ]`  | <ruby><rb>漢字</rb><rt>かんじ</rt></ruby> |
| `食[た]べ 物[もの]` | <ruby><rb>食</rb><rt>た</rt></ruby>べ<ruby><rb>物</rb><rt>もの</rt></ruby> |

>&#128221; **Note:** There is a space between べ and 物 which allows the furigana (もの) to render correctly. If the space wasn't there the rendered text would be <ruby><rb>食</rb><rt>た</rt>べ<rb>物</rb><rt>もの</rt></ruby>.

## Edit Flashcard Templates to Show Furigana
In order for furigana that has been added in flashcards to be rendered by Anki, the template for the flashcard has to be edited.

![Template window](/assets/images/anki/template.png)
Step 1: Click the **Cards** button in the window that is used to add new cards. Once this button is clicked a window will open that allows you to edit the front and back sides of the card, as well as the CSS for the cards. 

![The template window with furigana applied](/assets/images/anki/templatefurigana.png)
Step 2: Add `furigana:` inside of the double brackets of the field you want furigana to be in. 
Step 3: Click **Save** to apply the changes that have been made.