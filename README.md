# CarGameH

Ling to itch:
https://m-h-a.itch.io/carsgame

תמונת רקע:

![image](https://github.com/hodwys/CarGameH/assets/92233601/9d434aa7-462f-4b02-af4c-3eba9b597bab)




במשחק זה המטרה היא לנהוג מבלי להתנגש במכוניות הבאות ממול. ברגע שהשחקן מתנגש ב"אוייבים" אז השחקן מושמד והמשחק נגמר.
לכל אחד מהאוייבים קיים Collider 2D, Rigidbody 2D, Sprite Renderer, Move, Time Spawner Random
לרכיבי ה  Move וה Time Spawner Random הוספתי להם סריפטים.

רכיב הMove: מעדכן את המיקום של המודל, נדרש להוסיף בשביל ה Time Spawner Random

![image](https://github.com/hodwys/CarGameH/assets/92233601/f39efb7a-0979-49a1-af3a-d259d3589c65)


רכיב הTime Spawner Rando: 
הגדרתי 2 משתנים מינים ומקסימום זמנים שצריך לחכות בין כל יצירת אוייב.
![image](https://github.com/hodwys/CarGameH/assets/92233601/a4b88a9b-eb60-4e11-be6d-db57d7cc34e1)


בפונקציה זו נוצר האוייב בזמן רנדומלי בין המינימום למקסימום זמן.
![image](https://github.com/hodwys/CarGameH/assets/92233601/d2ae4c41-73f3-47cf-8e87-a45198a844e7)

על מנת שלא יווצרו מלא אויביים שאנחנו לא צריכים וגם כתוצאה מזה המחשב יתקע בשלב מסויים נרדש להשמיד את האוייבים לאחר שיצאו מגבולות המלצמה ולכן הוספתי את התנאי הבא:

![image](https://github.com/hodwys/CarGameH/assets/92233601/63b6e57a-dfd6-4a4e-827f-2f900ae07a52)

כך לאחר שאותו אוייב ספציפי כבר לא יהיה רלוונטי הוא יושמד.

לשחקן יש סריפט של GameOver וסריפט של DestroyOnTrigger2D:
קוד DestroyOnTrigger2D:

![image](https://github.com/hodwys/CarGameH/assets/92233601/b5f4f3d5-fc4f-4923-9fd5-b7198fedffb8)

הפונקציה בודקת אם השחקן התנגש ברכיב שהוגדר ואם כן השחקן מושמד.


קוד GameOver:

![image](https://github.com/hodwys/CarGameH/assets/92233601/5cceb7f2-6be2-4569-bb08-6fab0445b7ca)


הפונקציה בודקת אם השחקן התנגש ברכיב שהוגדר ואם כן מודפס שהמשחק נגמר והמשחק נעצר.
במטלה זאת השתמשתי במה שלמדנו בשיעור. 


