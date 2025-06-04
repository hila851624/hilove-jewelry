# hilove-jewelry

תכשיטים שמתאהבים בהם מהרגע הראשון ב־Hilove Jewellery תמצאו תכשיטים בעיצוב ייחודי שמשלבים בין יופי, נוחות ואיכות – במחירים הכי נגישים שיש. כל תכשיט נבחר בקפידה כדי להעניק לך מראה זוהר, אלגנטי וסטייל שאין לאף אחת אחרת.
בין אם את מחפשת משהו יומיומי ועדין או תכשיט שיגנוב את ההצגה – אצלנו תמצאי בדיוק את מה שחלמת עליו
mport json

def parse_products(filename):
    products = []
    with open(filename, 'r', encoding='utf-8') as f:
        lines = f.readlines()

    current_product = {}
    for line in lines:
        line = line.strip()
        if not line:
            # שורה ריקה מסמנת מעבר למוצר חדש
            if current_product:
                products.append(current_product)
                current_product = {}
            continue

        # נניח שכל שורה היא "שדה: ערך"
        if ':' in line:
            key, value = line.split(':', 1)
            key = key.strip()
            value = value.strip()
            current_product[key] = value

    # הוספת המוצר האחרון אם קיים
    if current_product:
        products.append(current_product)

    return products

def save_as_json(products, output_filename):
    with open(output_filename, 'w', encoding='utf-8') as f:
        json.dump(products, f, ensure_ascii=False, indent=4)
        <!DOCTYPE html>
<html lang="he">
<head>
  <meta charset="UTF-8">
  <title>קטלוג המוצרים של Hilove Jewellery</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      direction: rtl;
      background-color: #fffafc;
      padding: 20px;
    }
    h1 {
      text-align: center;
      color: #d36c8c;
    }
    .product {
      border: 1px solid #ffc8dd;
      border-radius: 12px;
      padding: 15px;
      margin-bottom: 20px;
      background-color: #fff0f5;
      max-width: 400px;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }
    .product img {
      width: 100%;
      border-radius: 8px;
    }
    .product h2 {
      margin: 10px 0 5px;
    }
    .product p {
      margin: 5px 0;
    }
  </style>
</head>
<body>

  <h1>קטלוג המוצרים שלי 💖</h1>

  <div class="product">
    <img src="https://via.placeholder.com/400x300.png?text=צמיד+חמסה" alt="צמיד חמסה">
    <h2>צמיד חמסה כסף</h2>
    <p><strong>מחיר:</strong> 99 ש"ח</p>
    <p><strong>תיאור:</strong> צמיד עדין עם תליון חמסה, מתאים לכל מידה.</p>
  </div>

  <div class="product">
    <!DOCTYPE html>
<html lang="he">
<head>
  <meta charset="UTF-8">
  <title>HiLove Jewellery</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      direction: rtl;
      background-color: #fff8f5;
      padding: 20px;
    }
    h1 {
      text-align: center;
      color: #d47d96;
    }
    .product {
      border: 1px solid #ffd5dd;
      border-radius: 15px;
      padding: 15px;
      margin: 15px 0;
      background-color: #fff;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
      display: flex;
      gap: 20px;
      align-items: center;
    }
    .product img {
      max-width: 150px;
      border-radius: 10px;
    }
    .details {
      flex: 1;
    }
    .details h2 {
      margin: 0 0 10px;
      color: #d47d96;
    }
    .details p {
      margin: 5px 0;
    }
    .price {
      font-weight: bold;
      color: #333;
    }
    .collection {
      font-style: italic;
      color: #777;
    }
  </style>
</head>
<body>
  <h1>קטלוג תכשיטים - HiLove Jewellery</h1>

  <!-- הדבקתי פה רק דוגמה של מוצר אחד לדוגמה -->
  <div class="product">
    <img src="https://example.com/image.jpg" alt="שם המוצר">
    <div class="details">
      <h2>שם המוצר</h2>
      <p>תיאור קצר של המוצר</p>
      <p class="price">₪99</p>
      <p class="collection">קולקציה: קיץ 2025</p>
    </div>
  </div>

  <!-- פה ייכנסו שאר המוצרים שלך -->

</body>
</html>
    <img src="https://via.placeholder.com/400x300.png?text=טבעת+לב" alt="טבעת לב">
    <h2>טבעת לב פתוח</h2>
    <p><strong>מחיר:</strong> 85 ש"ח</p>
    <p><strong>תיאור:</strong> טבעת פתוחה בעיצוב לב כסופה ואלגנטית.</p>
  </div>

</body>
