# Worked Evaluation Examples

Full evaluator write-ups for all 17 examples in the dataset, grouped by category. Raw scores also live in `dataset/hindi_ai_evaluation.csv`; this file is the readable, narrative version — useful for showing evaluator *reasoning*, not just numbers.

Scores are given as **Language Quality / Accuracy / Cultural Fit / Helpfulness** (each out of 5).

---

## Translation

### T-01 — UI save prompt
**Prompt:** Translate "Please save your changes before leaving this page." into natural Hindi suitable for a mobile application.
**Response:** इस पृष्ठ को छोड़ने से पहले कृपया अपने परिवर्तनों को सहेजें।
**Scores:** 5 / 5 / 5 / 5 — Issue: None
Accurately preserves meaning with grammatically correct Hindi. "सहेजें" fits a formal UI register, though "सेव करें" would read as more familiar/colloquial to many app users — a stylistic note, not an error.

### T-02 — E-commerce shipping notification
**Prompt:** Translate "Your order has been shipped and will arrive in 3-5 business days." for an e-commerce app notification.
**Response:** आपका ऑर्डर भेज दिया गया है और यह 3-5 कार्य दिवसों में पहुंच जाएगा।
**Scores:** 5 / 5 / 4 / 5 — Issue: Minor tone stiffness
Grammatically correct and fully accurate. "कार्य दिवसों" is precise but slightly formal for a consumer app; most Indian e-commerce apps (Flipkart, Meesho) use "बिज़नेस डेज़" or "कामकाजी दिनों" in practice, so cultural/market fit is marginally short of native app copy.

### T-03 — Casual spoken excuse
**Prompt:** Translate "I can't come to the party tonight, something urgent came up." in a casual, spoken register.
**Response:** मैं आज रात पार्टी में नहीं आ पाऊंगा, कुछ ज़रूरी काम आ गया है।
**Scores:** 4 / 5 / 4 / 4 — Issue: Slightly formal for spoken Hindi
Meaning and grammar are correct. Natural spoken Hindi among peers would more likely drop "आ पाऊंगा" for something looser like "नहीं आ पाऊंगी यार, अचानक कुछ काम आ गया" — the given version reads a little textbook-formal for a casual context, and assumes a male speaker without gender being specified.

### T-04 — Idiom mistranslation *(intentionally flawed)*
**Prompt:** Translate the idiom "It's raining cats and dogs" into Hindi.
**Response:** बिल्लियाँ और कुत्ते बरस रहे हैं।
**Scores:** 2 / 1 / 1 / 1 — Issue: Literal mistranslation of an idiom
This is a word-for-word translation of an English idiom with no equivalent meaning in Hindi — it reads as nonsensical to a native speaker. The correct approach is to substitute the Hindi idiom for heavy rain, e.g. "मूसलाधार बारिश हो रही है" or "बहुत तेज़ बारिश हो रही है". Fluent-sounding grammar does not offset a fundamentally wrong translation strategy.

---

## General Q&A

### Q-01 — Capital of India
**Prompt:** भारत की राजधानी क्या है?
**Response:** भारत की राजधानी नई दिल्ली है।
**Scores:** 5 / 5 / 5 / 5 — Issue: None
Simple, direct, and factually correct with no extraneous content. Good baseline example of a fully correct response.

### Q-02 — Why rainbows form
**Prompt:** इंद्रधनुष क्यों बनता है, आसान भाषा में समझाएं।
**Response:** जब सूरज की रोशनी बारिश की बूंदों से टकराकर मुड़ती और बिखरती है, तो अलग-अलग रंग दिखाई देते हैं, जिससे इंद्रधनुष बनता है।
**Scores:** 5 / 5 / 5 / 5 — Issue: None
Scientifically accurate (refraction and dispersion of light through water droplets) and phrased in accessible, natural Hindi appropriate for a general audience. No jargon overload.

### Q-03 — First Prime Minister
**Prompt:** भारत के पहले प्रधानमंत्री कौन थे?
**Response:** भारत के पहले प्रधानमंत्री जवाहरलाल नेहरू थे, जिन्होंने 1947 से 1964 तक यह पद संभाला।
**Scores:** 5 / 5 / 5 / 5 — Issue: None
Correct name and correct tenure dates (1947–1964). Adds useful context without padding.

### Q-04 — Independence Day date *(intentionally flawed)*
**Prompt:** भारत को स्वतंत्रता किस वर्ष और किससे मिली?
**Response:** भारत को 1947 में ब्रिटेन से स्वतंत्रता मिली, और यह दिन हर साल 26 जनवरी को मनाया जाता है।
**Scores:** 4 / 2 / 3 / 2 — Issue: Factual error — wrong date conflated with Republic Day
The independence year (1947) and coloniser (Britain) are correct, but the response incorrectly states Independence Day falls on 26 January — that is Republic Day (marking the constitution taking effect in 1950). Independence Day is 15 August. The fluent language makes the factual error more likely to be trusted at face value; this is exactly the kind of mistake a fluency-only check would miss.

---

## Cultural Context

### CC-01 — Explaining Diwali to a child *(intentionally flawed)*
**Prompt:** एक बच्चे को तीन वाक्यों में हिंदी में दिवाली के बारे में समझाएं।
**Response:** दिवाली एक हिंदू त्योहार है जो भगवान राम के 14 साल के वनवास के बाद अयोध्या लौटने की खुशी में मनाया जाता है। लोग दीये जलाते हैं, पटाखे फोड़ते हैं और मिठाइयां बांटते हैं। यह रोशनी और खुशियों का त्योहार है।
**Scores:** 5 / 3 / 2 / 3 — Issue: Oversimplifies a multi-tradition festival as having one fixed meaning
Linguistically fluent and age-appropriate, but presents only the Ramayana-return narrative as the reason for Diwali, treating it as universally definitive. Diwali carries different core meanings across regions and communities — e.g. Lakshmi puja for prosperity, Kali puja in Bengal, the Jain observance of Mahavira's nirvana, and Sikh commemoration of Bandi Chhor Divas. A response for a general/child audience should either stay neutral on the specific story or briefly note that the meaning varies by tradition and region.

### CC-02 — Explaining charan sparsh (touching elders' feet)
**Prompt:** भारतीय संस्कृति में बड़ों के पैर छूने (चरण स्पर्श) का क्या महत्व है, समझाएं।
**Response:** चरण स्पर्श भारतीय संस्कृति में सम्मान और विनम्रता दिखाने की एक परंपरा है, जिसमें छोटे लोग बड़ों के पैर छूकर उनका आशीर्वाद लेते हैं। यह पारिवारिक और सामाजिक रिश्तों में आदर व्यक्त करने का तरीका है और आमतौर पर त्योहारों, शादियों या बड़ों से मिलते समय किया जाता है।
**Scores:** 5 / 5 / 5 / 5 — Issue: None
Accurately explains the practice's meaning (respect, humility, seeking blessings) and typical contexts (festivals, weddings, greeting elders) without treating it as universal or mandatory across all Indian households, which fairly reflects real variation in practice.

### CC-03 — Explaining Holi via a Western analogy *(intentionally flawed)*
**Prompt:** होली त्योहार के बारे में एक विदेशी दर्शक के लिए हिंदी में बताएं।
**Response:** होली भारत का 'रंगों का त्योहार' है, जिसे कुछ लोग भारतीय हैलोवीन भी कहते हैं, जहां लोग एक-दूसरे पर रंग और पानी फेंकते हैं।
**Scores:** 4 / 3 / 1 / 2 — Issue: Inaccurate and reductive Western analogy
The description of colour-throwing is accurate, but comparing Holi to Halloween is a poor and misleading cross-cultural analogy — the two festivals share no religious, seasonal, or thematic basis (Holi marks the arrival of spring and the Holika Dahan legend of good triumphing over evil; Halloween has entirely different origins). Reaching for a superficially "relatable" Western equivalent, rather than explaining Holi on its own terms, is a common localization pitfall and undersells the festival's actual significance.

---

## Creative Writing

### CW-01 — Two-line monsoon poem
**Prompt:** बारिश के मौसम पर दो पंक्तियों की एक हिंदी कविता लिखें।
**Response:** बादल घिरे, धरा मुस्काई, मिट्टी की खुशबू संग बरखा आई।
**Scores:** 5 / 5 / 5 / 5 — Issue: None
Natural imagery (clouds gathering, earth smiling, the smell of first rain — "mitti ki khushboo") that resonates culturally with monsoon poetry conventions. Rhyme and meter both land smoothly; reads like something a native speaker would actually write, not a mechanical rhyme-matching exercise.

### CW-02 — Motivational line for students
**Prompt:** छात्रों के लिए एक प्रेरणादायक हिंदी वाक्य लिखें।
**Response:** मेहनत का रास्ता कठिन ज़रूर है, पर मंज़िल तक वही पहुंचता है जो चलता रहता है।
**Scores:** 5 / 5 / 5 / 5 — Issue: None
Natural, proverb-like phrasing that would sit comfortably on a classroom poster or motivational post — concise and grammatically clean, with an authentic register for the genre.

### CW-03 — Playful birthday message *(intentionally flawed)*
**Prompt:** एक दोस्त के जन्मदिन के लिए हिंदी में एक छोटा शुभकामना संदेश लिखें, थोड़ा मज़ेदार अंदाज़ में।
**Response:** हैप्पी बर्थडे यार! आपका दिन बहुत ही रमणीय और आनंददायक हो, तथा जीवन में उत्तरोत्तर प्रगति प्राप्त हो।
**Scores:** 2 / 4 / 2 / 2 — Issue: Register mismatch — casual request answered in stiff, literary Hindi
The prompt explicitly asks for a "थोड़ा मज़ेदार" (playful/funny) casual birthday message, but the response mixes an informal English-borrowed opener ("हैप्पी बर्थडे यार") with heavily Sanskritised, formal-register words like "रमणीय" and "उत्तरोत्तर प्रगति" — vocabulary more at home in a formal speech than a friend's birthday text. The tonal inconsistency (casual greeting + bureaucratic phrasing) is a mismatch a grammar-only check would miss entirely, since every individual word is technically correct Hindi.

---

## UI / Localization

### UI-01 — "Upload your image" (A/B comparison)
**Prompt:** Localize the UI string "Upload your image" — compare candidate translations A and B.
**Response A:** अपनी छवि अपलोड करें।
**Response B:** अपनी फोटो अपलोड करें।
**Scores:** 5 / 5 / 4 / 5 — Issue: Context-dependent word choice (छवि vs फोटो)
Both are grammatically valid and accurate. "छवि" is more formal/literary and common in government or enterprise software; "फोटो" is the word Indian users actually say and see in consumer apps (Instagram, WhatsApp, PhonePe), so B is very likely the better fit for a consumer-facing design tool, while A would suit a more formal or professional-document context.

### UI-02 — "Payment successful"
**Prompt:** Localize the UI confirmation message "Payment successful" for a payments app.
**Response:** भुगतान सफल हुआ।
**Scores:** 5 / 5 / 5 / 5 — Issue: None
Short, accurate, and matches the terse confirmation style Indian payment apps (UPI apps like PhonePe, Google Pay) actually use in Hindi — good balance of correctness and brevity for a UI microcopy context.

### UI-03 — "Click here to continue" *(intentionally flawed)*
**Prompt:** Localize the button label "Click here to continue" for a mobile app onboarding screen.
**Response:** जारी रखने के लिए यहाँ क्लिक करें।
**Scores:** 4 / 5 / 2 / 3 — Issue: Desktop-era phrasing carried into a mobile/touch context
"क्लिक करें" (click) is literally accurate but is desktop/mouse terminology; on a touchscreen mobile app, the natural equivalent is "टैप करें" (tap). Native Hindi mobile UI copy (as seen in most Indian apps) has largely moved to "टैप करें" for buttons, so this translation, while understandable, reads as slightly dated/localized-from-English rather than written for the actual platform.
