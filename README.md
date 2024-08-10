# Python-Tuples
Tuple is one of 4 built-in data types in Python used to store collections of data, the other 3 are List, Set, and Dictionary, all with different qualities and usage

# Tuples في بايثون (Python Tuples)

## مقدمة عن Tuples

Tuples في بايثون هي نوع من أنواع البيانات المدمجة التي تُستخدم لتخزين مجموعة من العناصر في متغير واحد. Tuples تشبه القوائم (Lists) ولكن مع بعض الفروقات الأساسية:

- **مرتبة**: العناصر داخل Tuple تكون مرتبة.
- **غير قابلة للتغيير**: بمجرد إنشاء Tuple لا يمكن تغيير عناصرها.
- **تسمح بالتكرار**: يمكن أن تحتوي على قيم مكررة.

يتم تعريف الـ Tuples باستخدام الأقواس الدائرية `()`.

### إنشاء Tuple
لإنشاء Tuple، يمكن استخدام الأقواس الدائرية ووضع العناصر داخلها مفصولة بفواصل.
```python
mytuple = ("apple", "banana", "cherry")
print(mytuple)
```

## خصائص Tuples

### 1. مرتبة (Ordered)
العناصر داخل الـ Tuple لها ترتيب محدد لا يتغير بعد إنشائها.

### 2. غير قابلة للتغيير (Unchangeable)
بمجرد إنشاء Tuple، لا يمكن تعديل، إضافة، أو حذف العناصر منها.
```python
mytuple = ("apple", "banana", "cherry")
# لا يمكن تغيير أو إضافة أو حذف عناصر
```

### 3. تسمح بالتكرار (Allow Duplicates)
تسمح الـ Tuples بتكرار القيم، أي يمكن أن تحتوي على نفس العنصر أكثر من مرة.
```python
mytuple = ("apple", "banana", "cherry", "apple", "cherry")
print(mytuple)
```

### 4. الطول (Length)
لتحديد عدد العناصر في Tuple، يمكن استخدام الدالة `len()`.
```python
mytuple = ("apple", "banana", "cherry")
print(len(mytuple))  # سيطبع 3
```

## إنشاء Tuple بعنصر واحد
إذا كنت تريد إنشاء Tuple يحتوي على عنصر واحد فقط، يجب إضافة فاصلة بعد العنصر، وإلا فلن يتعرف بايثون على الكيان كـ Tuple.
```python
thistuple = ("apple",)
print(type(thistuple))  # سيطبع <class 'tuple'>

# إذا لم تُضف الفاصلة
thistuple = ("apple")
print(type(thistuple))  # سيطبع <class 'str'>
```

## أنواع البيانات في Tuples

يمكن أن تحتوي Tuples على عناصر من أنواع بيانات مختلفة:
```python
tuple1 = ("apple", "banana", "cherry")
tuple2 = (1, 5, 7, 9, 3)
tuple3 = (True, False, False)
```

يمكن أيضًا للـ Tuple أن تحتوي على أنواع بيانات مختلفة في نفس الوقت.
```python
tuple1 = ("abc", 34, True, 40, "male")
```

## استخدام الـ Constructor لإنشاء Tuples
يمكنك أيضًا إنشاء Tuple باستخدام الدالة المدمجة `tuple()`.
```python
thistuple = tuple(("apple", "banana", "cherry"))  # لاحظ الأقواس المزدوجة
print(thistuple)
```

## مقارنة Tuples مع الأنواع الأخرى من المجموعات

في بايثون، لدينا أربع أنواع من المجموعات:

1. **List**: مجموعة مرتبة وقابلة للتغيير. تسمح بالعناصر المكررة.
2. **Tuple**: مجموعة مرتبة وغير قابلة للتغيير. تسمح بالعناصر المكررة.
3. **Set**: مجموعة غير مرتبة وغير قابلة للتغيير ولا تسمح بالعناصر المكررة.
4. **Dictionary**: مجموعة من أزواج المفتاح والقيمة، مرتبة منذ الإصدار 3.7.

عند اختيار نوع المجموعات، يجب فهم خصائص كل نوع لاختيار النوع المناسب للاستخدام الأمثل.

# الوصول إلى عناصر Tuples

يمكن الوصول إلى عناصر الـ Tuple باستخدام رقم الفهرس داخل الأقواس المربعة.
```python
thistuple = ("apple", "banana", "cherry")
print(thistuple[1])  # سيطبع banana
```

### الفهرسة السلبية
يمكنك أيضًا استخدام الفهارس السلبية للوصول إلى العناصر بدءًا من النهاية.
```python
thistuple = ("apple", "banana", "cherry")
print(thistuple[-1])  # سيطبع cherry
```

### نطاق الفهارس
يمكنك تحديد نطاق من الفهارس لاستخراج جزء من الـ Tuple. سيتم إنشاء Tuple جديدة تحتوي على العناصر ضمن النطاق المحدد.
```python
thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
print(thistuple[2:5])  # سيطبع ('cherry', 'orange', 'kiwi')
```

## التحقق من وجود عنصر في Tuple

للتحقق مما إذا كان عنصر معين موجودًا في الـ Tuple، يمكنك استخدام الكلمة المفتاحية `in`.
```python
thistuple = ("apple", "banana", "cherry")
if "apple" in thistuple:
    print("Yes, 'apple' is in the fruits tuple")
```

# تحديث الـ Tuples في بايثون (Update Tuples)

## تغيير قيم الـ Tuple

بمجرد إنشاء الـ Tuple، لا يمكنك تغيير قيمه مباشرة. ولكن يمكنك تحويل الـ Tuple إلى قائمة (List)، تعديل القائمة، ثم تحويلها مرة أخرى إلى Tuple.
```python
x = ("apple", "banana", "cherry")
y = list(x)
y[1] = "kiwi"  # تغيير "banana" إلى "kiwi"
x = tuple(y)

print(x)  # سيطبع ('apple', 'kiwi', 'cherry')
```

## إضافة عناصر إلى الـ Tuple

### الطريقة الأولى: تحويل الـ Tuple إلى قائمة
بما أن الـ Tuples غير قابلة للتغيير، لا يوجد دالة مدمجة لإضافة عناصر جديدة. ولكن يمكنك تحويل الـ Tuple إلى قائمة، إضافة العناصر المطلوبة، ثم تحويلها مرة أخرى إلى Tuple.
```python
thistuple = ("apple", "banana", "cherry")
y = list(thistuple)
y.append("orange")  # إضافة "orange" إلى القائمة
thistuple = tuple(y)

print(thistuple)  # سيطبع ('apple', 'banana', 'cherry', 'orange')
```

### الطريقة الثانية: إضافة Tuple إلى Tuple
يمكنك أيضًا إضافة Tuple إلى Tuple آخر. إذا كنت ترغب في إضافة عنصر أو أكثر، يمكنك إنشاء Tuple جديد يحتوي على العنصر (أو العناصر) المراد إضافتها، ثم جمعها مع الـ Tuple الأصلي.
```python
thistuple = ("apple", "banana", "cherry")
y = ("orange",)
thistuple += y  # جمع الـ Tuples

print(thistuple)  # سيطبع ('apple', 'banana', 'cherry', 'orange')
```
**ملاحظة:** عند إنشاء Tuple يحتوي على عنصر واحد فقط، تأكد من إضافة فاصلة بعد العنصر، وإلا فلن يتم التعرف عليه كـ Tuple.

## إزالة عناصر من الـ Tuple

### ملاحظة:
لا يمكنك إزالة عناصر من الـ Tuple بشكل مباشر لأنها غير قابلة للتغيير. ولكن يمكنك استخدام نفس الحل الذي استخدمناه لتغيير أو إضافة عناصر: تحويل الـ Tuple إلى قائمة، حذف العنصر المطلوب، ثم تحويلها مرة أخرى إلى Tuple.
```python
thistuple = ("apple", "banana", "cherry")
y = list(thistuple)
y.remove("apple")  # إزالة "apple" من القائمة
thistuple = tuple(y)

print(thistuple)  # سيطبع ('banana', 'cherry')
```

### حذف الـ Tuple بالكامل
يمكنك حذف الـ Tuple بالكامل باستخدام الكلمة المفتاحية `del`.
```python
thistuple = ("apple", "banana", "cherry")
del thistuple
# print(thistuple)  # سيؤدي إلى خطأ لأن الـ Tuple لم يعد موجودًا
```

# فك تجميع (Unpacking) الـ Tuples

عند إنشاء Tuple، يمكن تعيين قيمه إلى متغيرات فردية، وهذا يسمى "فك التجميع".
```python
fruits = ("apple", "banana", "cherry")
(green, yellow, red) = fruits

print(green)
print(yellow)
print(red)
```
**ملاحظة**: يجب أن يتطابق عدد المتغيرات مع عدد العناصر في الـ Tuple.

### استخدام النجمة (Asterisk)
إذا كان عدد المتغيرات أقل من عدد العناصر، يمكن استخدام النجمة `*` لتجميع العناصر المتبقية في قائمة.
```python
fruits = ("apple", "banana", "cherry", "strawberry", "raspberry")
(green, yellow, *red) = fruits

print(green)
print(yellow)
print(red)  # سيطبع ['cherry', 'strawberry', 'raspberry']
```

# دمج (Join) الـ Tuples

## دمج اثنين أو أكثر من الـ Tuples
يمكنك دمج الـ Tuples باستخدام المعامل `+`.
```python
tuple1 = ("a", "b", "c")
tuple2 = (1, 2, 3)
tuple3 = tuple1 + tuple2
print(tuple3)
```

## تكرار الـ Tuples
إذا كنت تريد تكرار محتويات Tuple عددًا معينًا من المرات، يمكنك استخدام المعامل `*`.
```python
fruits = ("apple", "banana", "cherry")
mytuple = fruits * 2
print(mytuple)  # سيطبع ('apple', 'banana', 'cherry

', 'apple', 'banana', 'cherry')
```

# طرق الـ Tuples

بايثون يحتوي على طريقتين مدمجتين يمكنك استخدامها مع الـ Tuples:

| الطريقة    | الوصف                                        |
|------------|-----------------------------------------------|
| `count()`  | يعيد عدد مرات تكرار قيمة محددة داخل الـ Tuple |
| `index()`  | يبحث عن قيمة محددة ويعيد فهرس أول ظهور لها   |

### مثال على `count()`:
```python
mytuple = ("apple", "banana", "cherry", "apple")
print(mytuple.count("apple"))  # سيطبع 2
```

### مثال على `index()`:
```python
mytuple = ("apple", "banana", "cherry")
print(mytuple.index("cherry"))  # سيطبع 2
```

# الواجب المنزلي حول Tuples في بايثون

## المهمة 1: إنشاء وتعديل الـ Tuples

1. **إنشاء Tuple بسيط:**
   - قم بإنشاء Tuple يحتوي على أسماء ثلاث فواكه.
   - قم بطباعة طول الـ Tuple باستخدام `len()`.

2. **إنشاء Tuple بأكثر من نوع بيانات:**
   - قم بإنشاء Tuple يحتوي على رقم صحيح، قيمة منطقية، ونص.
   - اطبع جميع العناصر في الـ Tuple باستخدام حلقة `for`.

3. **تعديل الـ Tuple:**
   - قم بتحويل الـ Tuple الذي يحتوي على أسماء الفواكه إلى قائمة.
   - قم بتغيير اسم الفاكهة الثانية إلى "مانجو".
   - أعد تحويل القائمة إلى Tuple واطبع النتيجة.

## المهمة 2: إضافة وإزالة عناصر من الـ Tuples

1. **إضافة عناصر إلى الـ Tuple:**
   - قم بإنشاء Tuple يحتوي على أسماء ثلاث ألوان.
   - أضف لونًا رابعًا باستخدام الطريقة التي تعلمتها في الدرس، واطبع الـ Tuple بعد الإضافة.

2. **إزالة عنصر من الـ Tuple:**
   - قم بتحويل الـ Tuple الذي يحتوي على الألوان إلى قائمة.
   - قم بإزالة اللون الأول من القائمة.
   - أعد تحويل القائمة إلى Tuple واطبع النتيجة.

## المهمة 3: فك تجميع ودمج الـ Tuples

1. **فك تجميع الـ Tuple:**
   - قم بإنشاء Tuple يحتوي على أسماء ثلاث دول.
   - فك تجميع الـ Tuple في ثلاث متغيرات منفصلة واطبع كل متغير.

2. **استخدام النجمة في فك التجميع:**
   - قم بإنشاء Tuple يحتوي على أسماء خمس مدن.
   - فك تجميع الـ Tuple بحيث تكون المدينة الأولى في متغير منفصل، والمدينة الأخيرة في متغير منفصل، وباقي المدن في قائمة. 
   - اطبع جميع المتغيرات الناتجة.

3. **دمج الـ Tuples:**
   - قم بإنشاء Tuple يحتوي على أسماء ثلاث لغات برمجة.
   - قم بإنشاء Tuple آخر يحتوي على أسماء ثلاث تقنيات ويب.
   - قم بدمج الـ Tuples في Tuple واحد واطبع النتيجة.

## المهمة 4: البحث في الـ Tuples

1. **البحث عن عنصر:**
   - قم بإنشاء Tuple يحتوي على أسماء خمس فواكه.
   - تحقق مما إذا كانت "تفاح" موجودة في الـ Tuple باستخدام `in`.
   - اطبع نتيجة التحقق.

2. **البحث عن الفهرس:**
   - قم بإنشاء Tuple يحتوي على أسماء خمس فواكه مختلفة.
   - استخدم دالة `index()` للبحث عن فهرس فاكهة معينة واطبع الفهرس.

3. **حساب التكرار:**
   - قم بإنشاء Tuple يحتوي على بعض الأسماء المكررة.
   - استخدم دالة `count()` لحساب عدد مرات تكرار اسم معين في الـ Tuple واطبع النتيجة.

## المهمة 5: تطبيق عملي

1. **إدارة قائمة مهام ثابتة:**
   - قم بإنشاء Tuple يحتوي على قائمة مهامك اليومية.
   - حاول إضافة مهمة جديدة باستخدام الطريقة التي تعلمتها.
   - إذا كانت قائمة المهام تحتوي على مهمة تم الانتهاء منها، قم بإزالتها.
   - اطبع قائمة المهام المحدثة.
