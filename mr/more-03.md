---
layout: "lesson"
lang: "mr"
title: "अधिक माहिती: लाटेक्-बीजाविषयी पायाभूत माहिती"
description: "ह्या प्रकरणात लाटेक्-बीजाची रचना कशी केली जाते व त्यातील विशेष चिन्हांचा वापर कसा केला जातो ह्याची माहिती आपण पाहणार आहोत. तसेच बीजधारिकेतून फलित कसे प्राप्त करावे हेदेखील पाहणार आहोत."
toc-anchor-text: "अधिक माहिती: लाटेक्-बीजाविषयी पायाभूत माहिती"
---

## लाटेक् चालवणे

[ह्यापूर्वी](lesson-02) नमूद केल्याप्रमाणे, लाटेक् बीजधारिका ह्या साध्या पाठ्य मजकुराच्या
स्वरूपात असतात. हे समजून घेण्यासाठी तुमची पहिली बीजधारिका एखाद्या मजकूर-संपादकामध्ये उघडून
पाहा. उदा. लिनक्स प्रणालीवर जीएडिट, विंडोज़् प्रणालीवर नोटपॅड. लाटेक्-च्या
मजकूर-संपादकासारखेच पाठ्य इतर ठिकाणीही आढळते.

लाटेक्-बीजावर प्रक्रिया करून पीडीएफ् फलित कोणत्याही संपादकाशिवायही घेता येते. त्याकरिता
आज्ञापटल (टर्मिनल/कमान्ड-प्रॉम्प्ट) वापरावे लागते. आज्ञापटल कसे वापरले जाते हे तुम्हाला माहीत
असेल, तर ज्या पुडक्यामध्ये (फोल्डरमध्ये) तुमची लाटेक्-बीजधारिका (उदा. पहिली.tex) आहे, तिथे
आज्ञापटलातून जा व पुढील आज्ञा चालवा.

`pdflatex पहिली`

अथवा

`pdflatex पहिली.tex`

टेक् हा धारिकेचा प्रत्यय टाकणे पर्यायी आहे. लाटेक् असे गृहीत धरते की ते टेक् प्रत्ययाच्या धारिकेवरच
काम करत आहे.

## विशेष चिन्हे

जर एखादे विशेष चिन्ह दस्तऐवजात छापायचे असेल, तर `\` हे चिन्ह त्या विशेष चिन्हाआधी वापरल्यास
बहुतांश वेळा योग्य फलित मिळते. उदा. `\{` हे आज्ञावलीत लिहिल्यास `{` हे फलितात दिसते. मात्र
काही ठिकाणी पूर्ण आज्ञा लिहायची आवश्यकता असू शकते. विशेष चिन्हांच्या तक्त्यासाठी पुढील कोष्टक
पाहा.

| चिन्ह | आज्ञेचे लघू रूप <br><small>(गणितक्षेत्र व साधा मजकूर)</small> | आज्ञेचे दीर्घ रूप <br><small>(केवळ मजकूर)</small> |
| --- | --- | --- |
| `{`   | `\{` | `\textbraceleft`   |
| `}`   | `\}` | `\textbraceright`  |
| `$`   | `\$` | `\textdollar`      |
| `%`   | `\%` |                    |
| `&`   | `\&` |                    |
| `#`   | `\#` |                    |
| `_`   | `\_` | `\textunderscore`  |
| ``\`` |      | `\textbackslash`   |
| `^`   |      | `\textasciicircum` |
| `~`   |      | `\textasciitilde`  |

शेवटच्या तीन चिन्हांच्या आज्ञांची लघू रूपे नाहीत. कारण `\\` ही आज्ञा ओळतोडीकरिता आहे व `\~`
तसेच `\^` ह्या स्वराघाताच्या चिन्हांसाठीच्या आज्ञा आहेत.
