---
title: "Thinking in Letters: Why Word Processors are Anti-Words"
date: 2020-02-27T20:00:30-05:00
draft: true
---

Word processors have monopolized the domain of text composition for the last quarter century. At their core, these programs involve text entry at the cursor, but with this function comes a wrapper of features: formatting, grammar and spell checking, support for annotation. The core however is simple: move the cursor with the mouse or the arrow keys and type letters at the cursor. Although some word processors promise features which approach a publishing suite, the average use case is the simple entry and manipulation of text. 



The largest unit of text that Google Docs understands is a sentence. For the most, part sophisticated spelling and grammar checking tools. Where docs fails is the user interaction with the text. We don’t think in letters we think in sentences and paragraphs, but we edit text in characters. Word processing forces the brain to descend to the level of the character while editing the document. 


Language is only reductively defined by a sequence of characters. We are all authors and we think in words and sentences. Vim addresses the text document completely and allows the author to edit the text with the same patterns which they produce language naturally.

There is a great tradition of editors which hold interfaces close to human understanding of text. Since the inception of the personal computer, users have stretched the conceptual bounds of editing text and continued to hone the tools which they use.

The tool which we will examine today is Vim. It has been around for decades and has a loyal userbase. Vim is an idiosyncratic editor which focuses on efficient text editing and conferability. Vim users use the keyboard to move the cursor around the document and make changes to the text. These commands rarely focus on a single character 
Take this passage as an example


“The killer was wearing a blue ski mask. He got away.” said Liam. Liam walked out into the hall.


“Not on my watch,” answered Sheila. 

Imagine an author wants to delete the sentence after Liam's dialogue. From the beginning of the line, the author can press ) to move forward a sentence and then das (Delete Around Sentence) to delete the sentence. In Google docs the author must select the text with the mouse and use the backspace or delete keys. Although at first the Vim inputs seem foreign, they map onto the authors understanding of the text. The text has structure in the authors mind and the inputs reflect that structure. 

Now the author wants to change Sheila's dialogue to avoid cliché. The input di" (Delete In Quote) will delete the contents of the quote but not the quotation marks. Vim understands the difference between the contents of the quote and the full clause. 

Vim consist of nouns and verbs. Nouns are logical text objects which represent well defined stings that exist in a document. For instance a word is a text object (characters enclosed in two spaces), a quotation is a text object (a set of words enclosed in quotation marks). There are also text objects for sentences and paragraphs and the community around Vim constantly creating new text objects. You can install text plugins that support many parts of sentence composition and even define your own.

In order to tap the immense power of text objects we must combine them with Vim verbs or operators. Operators describe actions to perform on a section of text. For instance deletion is a operator and surrounding text is an operator. 

To round out our discussion we must address a third element of Vim syntax

The power comes from composing verbs and nouns to make precise and sophisticated changes to text documents. Below are several increasingly powerful examples.

To delete a word you can compose the operator 'd' for delete and the text object 'w' for word as dw to delete word at your cursor. The command requires the cursor to be pointed at the start of the word, if you want to delete the word from any location you must diw.

To delete the contents of a quotation you can compose delete and the quotation text object di". This command will leave the quotation. If you want to delete the quotation entirely you can compose da".


For the sake of completeness, I should add that there exist many plain text formatting tools which support every thing from font changes to sophisticated reader-facing formatting. 
