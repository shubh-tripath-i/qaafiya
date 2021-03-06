# Qaafiya
It is a project to encourage the use of ML in field of literature.

## Introduction

In this era of data science, use of it is increasing day by day. Several researches are going on several fields and things are just getting more and more automated day by day. Be it autonomous cars or automatic poetry generation, ML models capability of mimcing the humans is improving every moment and in several fields have even outperformed humans.

So, i thought to automate some literature things up. There have been lot of work done on poetry generation of different languages but no work has been done in ML regarding urdu poetry. So, I thought to be the first one to do that. Also, I love poetry and so thought to use my knowledge to make it more fun.

Urdu poetry like other language's poetry has it's different form,pattern and rules. 'Qaafiya' is a project to take ML in field of urdu literature. The model takes a '_ghazal_' as an input and outputs whether the '_ghazal_' follows the rules of urdu ghazal writing. It is a sub-model of my project '_Urdu ghazal generator_' which generates ghazal of any length. It checks whether the ghazal generated by the '_Urdu ghazal Generator_' follows the rules of urdu ghazal writing or not. If it not, the model discards the '_sher_' which doesn't follow the rules and generates an another one.

## Dataset

Dataset was made by taking ghazals of 8 revolutionary poets of urdu language. The ghazals were taken from https://www.rekhta.org/ . The model is trained on ghazals written in '_devanagari lipi_' instead of english to respect the literature and not to use any foreign language. It is stored in '_poetry_' folder.

## Features

1. **First work in ML regarding urdu literature.**
2. Predicts with 99.85% accuracy(Accuracy on testing data).
3. Prediction within milliseconds.
4. Tells not only yes or no but also which line is creating the problem if no.
5. Handles whitespaces and unnecessary line breaks too.

## Examples

**Input -** 

"_वस्ल-ऐ-अहद  फ़ुरक़तों में तोड़ तो नहीं दोगी_

_तुम कहीं मुझे छोड़ तो नहीं दोगी_


_आसां नही था इसे बारिश से यूँ बचा लाना_ 

_इस मिटटी के गुलदस्तां को तुम फोड़ तो नहीं दोगी_


_ख़ुशी है हर्फ़-ऐ -प्यार की सजावट देख_

_डर ये है तुम इन्हे मोड़ तो नहीं दोगी_


_तुम कहीं कोई तबीब तो नहीं_

_तुम कहीं मेरा दिल जोड़ तो नहीं दोगी_


_ये कहानियां जो मेरी आँखों में हैं_

_लफ़्ज़ों में दाल तोड़ मरोड़ तो नहीं दोगी_ "

**Output -** 'The ghazal follows the rules of urdu ghazal writing.'

**Note -** This ghazal is written by me. And as it follows the rules, the model predicts yes.

**Input -**

"_वस्ल-ऐ-अहद  फ़ुरक़तों में तोड़ तो नहीं दोगी_

_तुम कहीं मुझे छोड़ तो नहीं दोगी_


_आसां नही था इसे बारिश से यूँ बचा लाना_

_इस मिटटी के गुलदस्तां को तुम फोड़ तो नहीं दोगी_


_ख़ुशी है हर्फ़-ऐ -प्यार की सजावट देख_

_डर ये है तुम इन्हे मोड़ दोगी_


_तुम कहीं कोई तबीब तो नहीं_

_तुम कहीं मेरा दिल जोड़ तो नहीं दोगी_


_ये कहानियां जो मेरी आँखों में हैं_

_लफ़्ज़ों में दाल तोड़ मरोड़ तो नहीं दोगी"_

**Output -** "The ghazal doesn't follows the rules of urdu ghazal writing. The problem firstly occurs in the line- डर ये है तुम इन्हे मोड़ दोगी"

**Note -** I just removed two words from the previous ghazal and we can see it outputs no with the line from which i removed the words.

**input -**

"_वस्ल-ऐ-अहद  फ़ुरक़तों में तोड़ तो नहीं दोगी_

_तुम कहीं मुझे छोड़ तो नहीं दोगी_


_आसां नही था इसे बारिश से यूँ बचा लाना_

_इस मिटटी के गुलदस्तां को तुम फोड़ तो नहीं दोगी_


_ख़ुशी है हर्फ़-ऐ -प्यार की सजावट देख_

_डर ये है तुम इन्हे मोड़ तो नहीं लोगी_ 


_तुम कहीं कोई तबीब तो नहीं_

_तुम कहीं मेरा दिल जोड़ तो नहीं दोगी_


_ये कहानियां जो मेरी आँखों में हैं_

_लफ़्ज़ों में दाल तोड़ मरोड़ तो नहीं दोगी_ "

**Output -** "The ghazal follows the rules of urdu ghazal writing".

**Note -** Here I changed the last word of line 6 to show it that it not only checks last rhymes but the whole structure. As it still follows structure of urdu ghazal writing, the model preducts yes.

## Future plans

1. To include other poetic forms of urdu literature like '_nazms_', '_qita_', etc too.
