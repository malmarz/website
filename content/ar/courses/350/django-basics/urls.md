---
# Page title
title: URLs

# Title for the menu link if you wish to use a shorter link title, otherwise remove this option.
linktitle: URLs

# Date page published
date: 2021-03-23

# Academic page type (do not modify).
type: book

# Position of this page in the menu. Remove this option to sort alphabetically.
weight: 6

draft: False


---

تسمح لنا عناوين URL لـ Django بربط المسارات في تطبيق الويب الخاص بنا بوظيفة العرض. لا يمكن لمستخدمي تطبيق الويب الخاص بنا استخدام وظيفة العرض إذا لم تكن مرتبطة بمسار. على سبيل المثال ، ذكرنا من[آخر تمرين معروض] ({{<ref "views.md">}})سيسمح هذا العرض المفصل لمستخدمي تطبيقاتنا بتحديد المنشور الذي يريدون عرضه باستخدام عنوان URL. المثال الذي استخدمناه هو أنه إذا فتح المستخدم المسار`/ post / 1`، ثم يمكنهم عرض تفاصيل المنشور الأول. باستخدام مسارات url ، يمكننا إخبار django أن ملف`/ post /` يتم استخدام المسار لفتح العرض التفصيلي.

مسار urls.py الرئيسي هو المسار الموجود في "mysite / urls.py". يوضح هذا الملف ما هو المسار الموجود في تطبيقنا. يتضمن بالفعل معلومات عن واجهة المسؤول ويمكننا معرفة ذلك المسار`/ admin /`ستكون مرتبطة بواجهة الإدارة. سنتبع اتفاقية Django في تنظيم عناوين url لتطبيق المدونة الخاص بنا عن طريق إنشاء ملف urls.py أولاً في تطبيق المدونة الخاص بنا. لذا قم بإنشاء ملف`/ blog / urls.py` وقم بتحديثه ليبدو كالتالي:

"python"
من عند . استيراد طرق العرض # 1
من مسار استيراد django.urls # 2

أنماط عنوان url = [# 3
 المسار ('' ، views.PostListView.as_view () ، الاسم = 'المنزل') ، # 4
 المسار ('<slug: slug> /'، views.PostDetailView.as_view ()، name = 'post_detail')، # 5
] # 6
""

لذلك دعونا نشرح ما يحدث هنا:
- ** في السطر رقم 1 **، نقوم باستيراد جميع وظائف العرض التي أنشأناها من الخطوة السابقة ، لأننا نريد ربطها بالمسارات.
- ** في السطر رقم 2 **، نحن مهمون لوظيفة المسار التي سنستخدمها لربط المسارات لعرض الوظيفة كما سنرى في السطور رقم 4 و 5
- ** في السطر رقم 3 **، هذه هي الطريقة التي يتخذ بها Django المسارات. يجب علينا استخدام المتغير ** urlspattens ** ، وهو متغير Django عالمي ، وتحديثه بأنماط ** list ** التي نريد استخدامها للمسارات في تطبيقاتنا.
- ** في السطر رقم 4 **، هذا هو المسار الأول الذي نريد إنشاءه ، المسار هو مجرد وظيفة تقبل 3 وسيطات ، الأولى هي المسار ، وهنا يعني المسار الفارغ إذا ذكرنا للتو `/ مدونة /`المسار دون أي إضافة إليه ، سيتم عرض PostListView (هذه هي الوسيطة الثانية). الوسيطة الأخيرة هي مجرد اسم فريد نطلقه على هذا المسار لنجعل من السهل علينا إنشاء رابط إلى هذا المسار.
- ** في السطر رقم 5 **، هذا هو نفس السطر 4. لاحظ أن المسار هو الآن `<slug: slug> /`. تُستخدم العلامة <> لإخبار Django أننا نتوقع سبيكة (سلسلة خاصة) هنا ونريد استخراج تلك سبيكة من المسار وإنشاء متغير يُسمى أيضًا slug بمحتويات المسار وإرساله إلى العرض وظيفة. إذا غيرناه إلى شيء مثل`<int: sid> /`يعني توقع عدد صحيح وأننا نريد استخراج هذا العدد الصحيح من المسار وإرسال القيمة كمتغير يسمى sid إلى وظيفة العرض. ولكن بما أننا نستخدم. الأتى[قسم من توثيق Django على عناوين URL] (https://docs.djangoproject.com/en/3.1/topics/http/urls/#how-django-processes-a-request) يجب أن توضح كيفية كتابة المسارات.
- ** في السطر رقم 6 **، تذكر أن هذه قائمة بيثون ، علينا إغلاق القائمة بقوس.

ماذا يفعل هذا الملف؟ حسنًا ، نحن هنا نقول لـ Django إذا فتح المستخدم ملف`/ مدونة /`المسار دون أي نص إضافي في المسار ، سيعرض تطبيق الويب الخاص بنا قائمة بالمنشورات. إذا فتح المستخدم`/ blog / title-of-post`ثم سيبحث django عن منشور يحتوي على slug ** title-of-post ** ويعرضه. تذكر أن السبيكات هي مجرد أوتار خاصة بدون مسافات. يتم استخدامه بشكل شائع لجعل عناوين url إلى المدونات ذات مغزى. وبالتالي"/ blog / my-first-python-program" من الواضح أنه منشور عن البرمجة كما هو مناسب `/ مدونة / 1` الذي لا يمكننا إخباره سيكون حول ماذا.

لكننا لم ننتهي بعد بشكل كامل ، يجب أن نربط ملف urls.py هذا في تطبيق المدونة الخاص بنا بـ ** mysite / urls.py ** الرئيسي. يتم تحقيق ذلك عن طريق تحديث ** mysite / urls.py ** على النحو التالي:

"python"
من django.contrib استيراد المسؤول
من مسار استيراد django.urls ، قم بتضمين # مضاف يشمل

أنماط عنوان url = [
 المسار ("admin /" ، admin.site.urls) ، 
 path ('blog /' ، بما في ذلك ('blog.urls')) ، # تمت إضافة هذا السطر
]
""

لاحظ أننا قمنا بتحديث سطرين. أول واحد في الاستيراد ، أضفنا وظيفة التضمين التي سيتم استخدامها لجلب مسارات url التي أنشأناها في ** blog / urls.py **. السطر الثاني الذي أضفناه هو مجرد وظيفة مسار مرة أخرى ، ولكن مع اثنين فقط من المعلمات. اول واحد هومدونة / `، نحن هنا نقول لـ Django أن جميع مسارات مدونتنا ستبدأ بها مدونة / `. الحجة الثانية هي الطريق إلى"blog / urls.py"، لكننا أزلنا الجزء .py واستبدلنا / بـ .. لذلك كل المسارات التي حددناها"blog / urls.py"يتم تضمينها الآن كجزء من تطبيق الويب الخاص بنا. لذا انطلق وقم بتشغيل خادم التطوير وسترى شاشة مختلفة تظهر:

{{<figure src = "course / 350 / urls1.png" caption = "توقع الخطأ بعد توصيل عناوين URL بشكل صحيح">}}

هنا يخبرنا Django أنه لا يمكنه العثور على أي شيء للخدمة في / (المعروف باسم مسار الجذر) ، لأننا حددنا فقط `المشرف /` و مدونة / `. في واقع الأمر ، كجزء من مساعدة Django ، فإنه يعرض قائمة المسارات التي تم التعرف عليها في تطبيق الويب الخاص بنا ويظهر بالفعل كلاً من`المشرف /` و مدونة / `. تذكر استخدام هذه المعلومات لفهم ما يحدث. حتى الآن أضف المسار`/ مدونة /`إلى عنوان url لتطبيق الويب الخاص بك. إذا تم كل شيء بشكل صحيح ، يجب أن ترى الخطأ التالي:

{{<figure src = "course / 350 / urls2.png" caption = "توقع الخطأ المتعلق بالقوالب">}}

يخبرنا Django هنا أنه نجح في تشغيل وظيفة عرض PostList التي أنشأناها ولكن لا يمكنه العثور على القالب post_list.html. ستكون هذه آخر قطعة متبقية لإكمال وظائف تطبيق الويب الخاص بنا في قوائم المنشورات ، والتي سنشرحها في القسم التالي.
