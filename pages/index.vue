<template>
  <header class="site-header">
  <h1 class="site-title">Kids Connect</h1>
</header>
  <div class="page-container">
    
    <!-- Левая колонка -->
    <div class="main-content">
      <!-- Силовой спорт -->
      <h2 class="section-title">Силовой спорт</h2>
      <div v-for="(item, index) in sports.filter(s => strengthCategories.includes(s.category.toLowerCase()))" :key="'strength-' + index" class="card">
        <div class="card-left">
          <div class="image-placeholder" />
        </div>
        <div class="card-content">
          <div class="card-header">
            <div>
              <h3 class="title">
                {{ item.title }}
                <span class="location">{{ item.subtitle }}</span>
              </h3>
              <p class="category">#{{ item.category }}</p>
              <p class="info"><span class="icon">👥</span> {{ item.age }}</p>
              <p class="info"><span class="icon">📍</span> {{ item.address }}</p>
              <p class="info"><span class="icon">🏢</span> {{ item.place }}</p>
              <p class="info"><span class="icon">🕒</span> {{ item.days }}</p>
              <div class="times">
                <span v-for="(time, i) in item.times" :key="i" class="time">{{ time }}</span>
              </div>
            </div>
            <div class="card-actions">
              <div class="labels">
                <span v-if="item.free" class="free-label">Бесплатно</span>
                <span v-if="item.firstFree" class="first-free-label">Первое бесплатно</span>
                <span v-if="item.price" class="price-label">{{ item.price }}</span>
              </div>
              <button class="btn" @click="openModal(item)">Подробнее</button>

            </div>
          </div>
        </div>
      </div>

      <!-- Единоборства -->
      <h2 class="section-title">Единоборства</h2>
      <div v-for="(item, index) in sports.filter(s => combatCategories.includes(s.category.toLowerCase()))" :key="'combat-' + index" class="card">
        <div class="card-left">
          <div class="image-placeholder" />
        </div>
        <div class="card-content">
          <div class="card-header">
            <div>
              <h3 class="title">
                {{ item.title }}
                <span class="location">{{ item.subtitle }}</span>
              </h3>
              <p class="category">#{{ item.category }}</p>
              <p class="info"><span class="icon">👥</span> {{ item.age }}</p>
              <p class="info"><span class="icon">📍</span> {{ item.address }}</p>
              <p class="info"><span class="icon">🏢</span> {{ item.place }}</p>
              <p class="info"><span class="icon">🕒</span> {{ item.days }}</p>
              <div class="times">
                <span v-for="(time, i) in item.times" :key="i" class="time">{{ time }}</span>
              </div>
            </div>
            <div class="card-actions">
              <div class="labels">
                <span v-if="item.free" class="free-label">Бесплатно</span>
                <span v-if="item.firstFree" class="first-free-label">Первое бесплатно</span>
                <span v-if="item.price" class="price-label">{{ item.price }}</span>
              </div>
              <button class="btn" @click="openModal(item)">Подробнее</button>

            </div>
          </div>
        </div>
      </div>

      <!-- Гоночный спорт -->
      <h2 class="section-title">Гоночный спорт</h2>
      <div v-for="(item, index) in sports.filter(s => raceCategories.includes(s.category.toLowerCase()))" :key="'race-' + index" class="card">
        <div class="card-left">
          <div class="image-placeholder" />
        </div>
        <div class="card-content">
          <div class="card-header">
            <div>
              <h3 class="title">
                {{ item.title }}
                <span class="location">{{ item.subtitle }}</span>
              </h3>
              <p class="category">#{{ item.category }}</p>
              <p class="info"><span class="icon">👥</span> {{ item.age }}</p>
              <p class="info"><span class="icon">📍</span> {{ item.address }}</p>
              <p class="info"><span class="icon">🏢</span> {{ item.place }}</p>
              <p class="info"><span class="icon">🕒</span> {{ item.days }}</p>
              <div class="times">
                <span v-for="(time, i) in item.times" :key="i" class="time">{{ time }}</span>
              </div>
            </div>
            <div class="card-actions">
              <div class="labels">
                <span v-if="item.free" class="free-label">Бесплатно</span>
                <span v-if="item.firstFree" class="first-free-label">Первое бесплатно</span>
                <span v-if="item.price" class="price-label">{{ item.price }}</span>
              </div>
              <button class="btn" @click="openModal(item)">Подробнее</button>

            </div>
          </div>
        </div>
      </div>

      <!-- Скоростной спорт -->
      <h2 class="section-title">Скоростной спорт</h2>
      <div v-for="(item, index) in sports.filter(s => speedCategories.includes(s.category.toLowerCase()))" :key="'speed-' + index" class="card">
        <div class="card-left">
          <div class="image-placeholder" />
        </div>
        <div class="card-content">
          <div class="card-header">
            <div>
              <h3 class="title">
                {{ item.title }}
                <span class="location">{{ item.subtitle }}</span>
              </h3>
              <p class="category">#{{ item.category }}</p>
              <p class="info"><span class="icon">👥</span> {{ item.age }}</p>
              <p class="info"><span class="icon">📍</span> {{ item.address }}</p>
              <p class="info"><span class="icon">🏢</span> {{ item.place }}</p>
              <p class="info"><span class="icon">🕒</span> {{ item.days }}</p>
              <div class="times">
                <span v-for="(time, i) in item.times" :key="i" class="time">{{ time }}</span>
              </div>
            </div>
            <div class="card-actions">
              <div class="labels">
                <span v-if="item.free" class="free-label">Бесплатно</span>
                <span v-if="item.firstFree" class="first-free-label">Первое бесплатно</span>
                <span v-if="item.price" class="price-label">{{ item.price }}</span>
              </div>
              <button class="btn" @click="openModal(item)">Подробнее</button>

            </div>
          </div>
        </div>
      </div>
    </div>


  <!-- Правая колонка -->
  <aside class="sidebar">
    <div class="search-panel">
      <input type="text" class="search" placeholder="Поиск" />
      <div class="filter-buttons">
        <button class="filter-btn">Все</button>
        <button class="filter-btn">Платные</button>
        <button class="filter-btn">Бесплатные</button>
      </div>
    </div>

    <div class="filters">
      <h3>Фильтры</h3>
      <label>
        Возраст
        <select>
          <option>Любой</option>
          <option>10-12</option>
          <option>13-15</option>
          <option>16-18</option>
        </select>
      </label>

      <div class="gender">
        <label><input type="checkbox" checked /> Мужской</label>
        <label><input type="checkbox" checked /> Женский</label>
      </div>

      <div class="catalog">
        <p>Каталог</p>
        <ul>
          <li>
            ▸ Силовой спорт <span class="count">3</span>
            <ul>
              <li>- Тяжелая атлетика <span class="count">3</span></li>
              <li>- Пауэрлифтинг <span class="count">1</span></li>
            </ul>
          </li>
          <li>
            ▸ Единоборства <span class="count">2</span>
            <ul>
              <li>- Вольная борьба <span class="count">1</span></li>
              <li>- Дзюдо <span class="count">1</span></li>
            </ul>
          </li>
          <li>
            ▸ Гоночный спорт
            <ul>
              <li>- Картинг</li>
              <li>- Мотокросс</li>
            </ul>
          </li>
          <li>
            ▸ Скоростной спорт
            <ul>
              <li>- Бег 100м</li>
              <li>- Велоспорт</li>
            </ul>
          </li>
          <li>▸ ДПИ и ремесла</li>
          <li>▸ Техническое конструирование</li>
          <li>▸ Словесность</li>
          <li>▸ Иностранные языки</li>
          <li>▸ Развитие интеллекта</li>
        </ul>
      </div>
    </div>
  </aside>
</div>

  <!-- 🟥 МОДАЛКА ПОД СКРИН -->
<div v-if="showModal && selectedItem" class="modal-overlay" @click.self="closeModal">
  <div class="modal-content">
    <header class="modal-header">
      <h1 class="site-title">Kids Connect</h1>
    </header>

    <div class="modal-body">
      <button class="back-btn" @click="closeModal">← Назад</button>

      <h2>{{ selectedItem.title }} ({{ selectedItem.subtitle }})</h2>

<!-- Картинка (пустая заглушка, как на сайте) -->
<div class="section-placeholder">
  <span>Нет изображения</span>
</div>


      <!-- Метки -->
      <div class="labels">
        <span class="badge" v-if="selectedItem.status">Набор открыт</span>
        <span class="badge free" v-if="selectedItem.free">Бесплатно</span>
      </div>

      <!-- Инфо -->
      <div class="info-block">
        <p><strong>👥 Возраст:</strong> {{ selectedItem.age }}</p>
        <p><strong>📍 Адрес:</strong> {{ selectedItem.address }}</p>
        <p><strong>🏢 Место:</strong> {{ selectedItem.place }}</p>
      </div>
      

      <!-- Описание -->
<div class="description-block">
  <h3>ОПИСАНИЕ</h3>
  <p>{{ selectedItem.description || 'Описание секции временно отсутствует.' }}</p>
</div>

<!-- Содержание программы -->
<div class="content-block">
  <h3>СОДЕРЖАНИЕ ПРОГРАММЫ</h3>
  <p>{{ selectedItem.content || 'Информация о содержании программы будет добавлена позже.' }}</p>
</div>


      <!-- Группы -->
      <div class="group-block">
        <h3>ГРУППЫ</h3>
        <div class="group-info">
          <p><strong>Этап:</strong> Этап начальной подготовки</p>
          <p><strong>Тренер:</strong> Петрова Елена Александровна</p>
          <p><strong>Время:</strong> 15 и 20</p>
          <p><strong>Срок обучения:</strong> 12 месяцев</p>
        </div>
      </div>

      <!-- Расписание -->
      <div class="schedule-block">
        <h3>РАСПИСАНИЕ ЗАНЯТИЙ</h3>
        <div class="days">
          <p>📅 Пн, Вт, Чт, Сб</p>
          <div class="times">
            <span class="time-tag">08:00 - 10:00</span>
            <span class="time-tag">18:00 - 19:30</span>
          </div>
        </div>
      </div>

      <!-- Действия -->
      <div class="action-block">
        <button class="btn primary">Записаться</button>
        <button class="btn ghost">На карте 📍</button>
      </div>
    </div>
  </div>
</div>


</template>

<script setup>
const strengthCategories = ['тяжелая атлетика', 'пауэрлифтинг', 'армреслинг']
const combatCategories = ['дзюдо', 'вольная борьба', 'каратэ', 'бокс']
const raceCategories = ['картинг', 'мотокросс']
const speedCategories = ['бег', 'велоспорт']

const sports = [
  { title: 'Тяжелая атлетика', subtitle: '(в Юбилейном мкр.)', category: 'тяжелая атлетика', age: '10-18 лет', address: 'г. Иркутск, Юбилейный мкр., стр. 49/1', place: 'ФОК "Юбилейный"', days: 'Пн, Ср, Пт', times: ['09:00 - 10:30', '12:00 - 13:30', '18:00 - 19:30'], free: true },
  { title: 'Тяжелая атлетика', subtitle: '(на ул. Боткина)', category: 'тяжелая атлетика', age: '10-18 лет', address: 'г. Иркутск, ул. Боткина, 15', place: 'СК "Атлет"', days: 'Пн, Ср, Пт', times: ['09:00 - 10:30', '12:00 - 13:30'], firstFree: true, price: '500 руб.' },
  { title: 'армреслинг', subtitle: '(в Юбилейном мкр.)', category: 'армреслинг', age: '10-18 лет', address: 'г. Иркутск, Юбилейный мкр., стр. 49/1', place: 'ФОК "Юбилейный"', days: 'Пн, Ср, Пт', times: ['09:00 - 10:30', '12:00 - 13:30', '18:00 - 19:30'], free: true },
  { title: 'Дзюдо', subtitle: '', category: 'дзюдо', age: '6–18 лет', address: 'г. Иркутск, ул Трудовая, д 115А', place: 'СК "Рингспец"', days: 'Пн, Ср, Пт', times: ['09:00 - 10:30', '12:00 - 13:30'], free: true },
  { title: 'Каратэ', subtitle: '', category: 'каратэ', age: '8–16 лет', address: 'г. Иркутск, ул Спортивная, 22', place: 'ДЮСШ "Спарта"', days: 'Вт, Чт', times: ['17:00 - 18:30'], price: '1000 руб.', firstFree: true },
  { title: 'Бокс', subtitle: '', category: 'бокс', age: '12–18 лет', address: 'г. Иркутск, ул Ленина, 9', place: 'СК "Чемпион"', days: 'Пн, Ср, Пт', times: ['16:00 - 17:30'], free: true },
  { title: 'Картинг', subtitle: '', category: 'картинг', age: '10–17 лет', address: 'г. Иркутск, ул Дорожная, 30', place: 'Автодром Юниор', days: 'Сб, Вс', times: ['11:00 - 13:00'], price: '1500 руб.' },
  { title: 'Мотокросс', subtitle: '', category: 'мотокросс', age: '12–18 лет', address: 'г. Иркутск, ул Окружная, 9', place: 'Трасса "Вихрь"', days: 'Сб', times: ['14:00 - 16:00'], firstFree: true },
  { title: 'Бег 100м', subtitle: '', category: 'бег', age: '10–16 лет', address: 'г. Иркутск, ул Ленина, 2', place: 'Стадион "Центральный"', days: 'Вт, Чт', times: ['17:00 - 18:30'], free: true },
  { title: 'Велоспорт', subtitle: '', category: 'велоспорт', age: '10–17 лет', address: 'г. Иркутск, ул Байкальская, 45', place: 'Спортпарк "Байкал"', days: 'Ср, Пт', times: ['10:00 - 11:30'], price: '800 руб.' }
]


import { ref } from 'vue'

const selectedItem = ref(null)
const showModal = ref(false)

function openModal(item) {
  selectedItem.value = item
  showModal.value = true
}

function closeModal() {
  showModal.value = false
}

import "../assets/styles.css"
</script>