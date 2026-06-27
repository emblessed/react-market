# 🛒 React Market - Маркетплейс

Полнофункциональный маркетплейс с React фронтендом и Node.js бэкендом.

## 🚀 Быстрый старт

### Бэкенд

1. Перейдите в папку сервера:
```bash
cd server
```

2. Установите зависимости:
```bash
npm install
```

3. Создайте файл `.env` на основе `.env.example`:
```bash
cp .env.example .env
```

4. Настройте переменные окружения в `.env`

5. Убедитесь, что MongoDB запущена

6. (Опционально) Заполните базу тестовыми данными:
```bash
npm run seed
```

7. Запустите сервер:
```bash
npm run dev
```

Сервер запустится на http://localhost:5000

### Фронтенд

1. Перейдите в папку клиента:
```bash
cd client
```

2. Установите зависимости:
```bash
npm install
```

3. Запустите приложение:
```bash
npm run dev
```

фронтенд откроется на порту http://localhost:5173



## 👥 Пользователи

-  (buyer) - может просматривать товары, добавлять в корзину, оформлять заказы
-  (seller) - может создавать и управлять своими товарами
-  (admin) - полный доступ ко всем функциям

## npm run seed
добавляет следующие данные:

**Пользователи:**
- Админ: `login=admin`, `password=admin123`
- Продавец: `login=seller1`, `password=seller123`
- Покупатель: `login=buyer1`, `password=buyer123`

**Товары:**
- 8 тестовых товаров в категории электроника

## 🔗 API Endpoints

### Аутентификация
- `POST /api/auth/register` - Регистрация
- `POST /api/auth/login` - Авторизация
- `GET /api/auth/profile` - Профиль пользователя
- `PUT /api/auth/profile` - Обновление профиля

### Товары
- `GET /api/products` - Все товары
- `GET /api/products/popular` - Популярные
- `GET /api/products/new` - Новые
- `GET /api/products/:id` - Товар по ID
- `POST /api/products` - Создать товар
- `PUT /api/products/:id` - Обновить товар
- `DELETE /api/products/:id` - Удалить товар

### Корзина
- `GET /api/cart` - Получить корзину
- `POST /api/cart` - Добавить в корзину
- `PUT /api/cart/:productId` - Обновить количество
- `DELETE /api/cart/:productId` - Удалить из корзины
- `DELETE /api/cart` - Очистить корзину

### Заказы
- `POST /api/orders` - Создать заказ
- `GET /api/orders` - Заказы пользователя
- `GET /api/orders/:id` - Заказ по ID
- `PUT /api/orders/:id/pay` - Отметить как оплаченный
- `PUT /api/orders/:id/cancel` - Отменить заказ
- `GET /api/orders/all/admin` - Все заказы (админ)
- `PUT /api/orders/:id/status` - Обновить статус (админ)


