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

span.slide {
  display: none; /* Скрыть все слайды */
  white-space: pre-wrap; /* Сохранять пробелы и переносы */
  position: relative; /* Чтобы разместить курсор внутри текста */
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

<h4> I turn complex ideas into simple solutions for: 
  <span class="slide">— Food-FMCG and Production Sites 🏭 🏗️ 🥩 🍪 </span>
  <span class="slide">— Transport and Warehouse Logistics 🚛 🚚 🛫 ⛴️ </span>
  <span class="slide">— Retail 🛒 🏪 🛍️ </span>
  <span class="slide">— In-house and Outsource IT Teams 🧑‍💻👩🏼‍💻😀</span>
  <span class="slide">— Software development 🖥️ 📱 💻 </span>
  <span class="slide">— Algorithmic trading 📊 💰 📈</span>
</h4>


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
  I’ve been turning complex ideas into simple solutions for 15+ years 🖥️ 🏭 🤖 📊  
{{< /cards >}} -->

<br clear="left"/>

## Explore Details

{{< cards >}}
  {{< card link="enterprise" title="Enterprise Expertise" icon="user-group" >}}
  {{< card link="personal" title="Personal Projects" icon="user-circle" >}}
{{< /cards >}}


<script>
  const slides = document.querySelectorAll('span.slide');
  let currentIndex = 0; // Текущий слайд
  let typingSpeed = 50; // Скорость появления букв (в миллисекундах)
  let displayInterval = 3000; // Интервал между слайдами (в миллисекундах)

  // Функция для имитации ввода текста
  function typeText(slide, text, callback) {
    let i = 0;
    slide.textContent = ''; // Очищаем текущий текст
    const interval = setInterval(() => {
      slide.textContent += text[i]; // Добавляем следующий символ
      i++;
      if (i === text.length) {
        clearInterval(interval); // Останавливаем, когда весь текст выведен
        if (callback) setTimeout(callback, displayInterval); // Вызываем callback после задержки
      }
    }, typingSpeed);
  }

  // Функция для показа текущего слайда
  function showSlide(index) {
    slides.forEach((slide, i) => {
      slide.style.display = 'none'; // Скрываем все слайды
    });
    const currentSlide = slides[index];
    currentSlide.style.display = 'block'; // Показываем текущий слайд
    typeText(currentSlide, currentSlide.dataset.text, nextSlide); // Анимация ввода текста
  }

  // Переход к следующему слайду
  function nextSlide() {
    currentIndex = (currentIndex + 1) % slides.length; // Переход на следующий слайд
    showSlide(currentIndex);
  }

  // Инициализация: Сохраняем текст слайда и запускаем первый
  slides.forEach(slide => {
    slide.dataset.text = slide.textContent; // Сохраняем оригинальный текст в data-text
    slide.style.display = 'none'; // Скрываем все слайды по умолчанию
  });
  showSlide(currentIndex); // Запускаем анимацию для первого слайда
</script>