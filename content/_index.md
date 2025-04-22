---
title: Hey, I'm Denis
toc: false
---

<style>
table {
    border-collapse: collapse;
}
table, tr, td {
   border: none;
   vertical-align: top;
}
.ss {
  padding-top: 0px  !important;
}

h4 {
  position: relative; /* Чтобы абсолютно позиционированные слайды не выходили за рамки h4 */
}

/* Контейнер для слайдов внутри h4 */
.slide-container {
  position: relative;
  min-height: 1.5em; /* Начальная минимальная высота, будет изменена JavaScript'ом */
  display: block;
  margin-top: 0.5em; /* Отступ от заголовка */
}

span.slide {
  display: none; /* Скрыть все слайды */
  white-space: pre-wrap; /* Сохранять пробелы и переносы */
  position: absolute; /* Абсолютное позиционирование */
  left: 0; /* Привязка к левому краю */
  top: 0; /* Привязка к верхнему краю */
  width: 100%; /* Полная ширина */
}

span.slide::after {
  content: ''; /* Псевдоэлемент для курсора */
  position: absolute;
  bottom: 0;
  width: 2px;
  height: 1em; /* Высота курсора */
  font-size: 1.2em; /* Размер курсора */
  background-color: #1e90ff; /* Цвет курсора */
  animation: blink 0.8s step-end infinite; /* Анимация мерцания */
  transform: translateY(-10%) translateX(5px); /* Слегка приподнять курсор и отодвинуть на 5px вправо */
}

@keyframes blink {
  50% {
    opacity: 0;
  }
}
</style>

![](/images/main.svg)

<h4> I turn complex ideas into simple solutions for: </h4>
<div class="slide-container">
  <span class="slide">— Food-FMCG and Production Sites </span>
  <span class="slide">— Transport and Warehouse Logistics </span>
  <span class="slide">— Retail and E-Commerce </span>
  <span class="slide">— In-house and Outsource IT Teams </span>
  <span class="slide">— Software development </span>
  <span class="slide">— Algorithmic trading </span>
</div>


<!-- <img style="float: left" src="/images/me-2-200.png"> -->
<!-- <table>
  <tr>
    <td>
      <img src="/images/me-2-200.png">
    </td>
    <td class="ss">
      <h5> I turn complex ideas into simple solutions for: 
      <span class="slide">— Production Sites 🏭 🏗️ 🥩 🍪 </span>
      <span class="slide">— Transport and Warehouse Logistics 🚛 🚚 🛫 ⛴️ </span>
      <span class="slide">— Retail 🛒 🏪 🛍️ </span>
      <span class="slide">— In-house and Outsource IT Teams 🧑‍💻👩🏼‍💻😀</span>
      <span class="slide">— Software development 🖥️ 📱 💻 </span>
      <span class="slide">— Algorithmic trading 📊 💰 📈</span>
      </h5>
    </td>
  </tr>
</table> -->

<!-- {{< cards >}}
  {{< card link="https://kislitsyn.me" title="" image="/images/me.png" subtitle="" >}}
  I've been turning complex ideas into simple solutions for 15+ years 🖥️ 🏭 🤖 📊  
{{< /cards >}} -->

<br clear="left"/>

## Explore Details

{{< cards cols="1">}}
  {{< card link="enterprise" title="Enterprise Expertise" icon="user-group" >}}
  {{< card link="personal" title="Freelance Projects" icon="user-circle" >}}
{{< /cards >}}


<script>
document.addEventListener('DOMContentLoaded', function() {
  const slides = document.querySelectorAll('span.slide');
  let currentIndex = 0;
  let typingSpeed = 50; // Скорость появления букв (в миллисекундах)
  let displayInterval = 3000; // Интервал между слайдами (в миллисекундах)

  // Создаем контейнер с фиксированной высотой
  const slideContainer = document.querySelector('.slide-container');
  
  // Найдем максимальную высоту среди всех слайдов
  let maxHeight = 0;
  
  // Сначала отобразим все слайды, чтобы измерить их высоту
  slides.forEach(slide => {
    slide.style.display = 'block';
    slide.style.visibility = 'hidden'; // Делаем их невидимыми, но измеряемыми
    const height = slide.offsetHeight;
    maxHeight = Math.max(maxHeight, height);
    slide.style.display = 'none';
    slide.style.visibility = 'visible';
  });
  
  // Установим минимальную высоту для контейнера слайдов
  slideContainer.style.minHeight = maxHeight + 'px';

  // Функция для имитации ввода текста
  function typeText(slide, text) {
    let i = 0;
    slide.textContent = ''; // Очищаем текущий текст
    slide.style.display = 'block'; // Показываем текущий слайд
    
    const interval = setInterval(() => {
      if (i < text.length) {
        slide.textContent += text[i]; // Добавляем следующий символ
        i++;
      } else {
        clearInterval(interval); // Останавливаем, когда весь текст выведен
        setTimeout(() => {
          slide.style.display = 'none'; // Скрываем слайд через displayInterval
          nextSlide(); // Переходим к следующему слайду
        }, displayInterval);
      }
    }, typingSpeed);
  }

  // Переход к следующему слайду
  function nextSlide() {
    currentIndex = (currentIndex + 1) % slides.length; // Переход на следующий слайд
    const currentSlide = slides[currentIndex];
    typeText(currentSlide, currentSlide.textContent);
  }

  // Инициализация: запускаем первый слайд
  if (slides.length > 0) {
    // Скрываем все слайды по умолчанию
    slides.forEach(slide => {
      slide.style.display = 'none';
    });
    
    // Запускаем анимацию для первого слайда
    const firstSlide = slides[0];
    typeText(firstSlide, firstSlide.textContent);
  }
});
</script>