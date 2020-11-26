<template>
  <footer class="footer">
    <div class="footer__inner">

      <div class="footer__company">
        ООО “Нейрософт”, 2020
        <br>
        Медицинское оборудование
      </div>

      <div class="footer__social">
        <!-- В классе у span не придумал ничего лучше,
         поэтому решил оставить просто text -->
        <span class="footer__text">Подписывайся в соц сетях</span> 

        <div class="footer__icon-wrap">
          <a href="#" class="footer__link">
            <i class="fab fa-instagram"></i>
          </a>
        </div>

        <div class="footer__icon-wrap">
          <a href="https://vk.com/neurosoft" class="footer__link">
            <i class="fab fa-vk"></i>
          </a>
        </div>
      </div>

    </div>
  </footer>
</template>

<style lang="scss" scoped>
  .footer {
    height: 152px;

    color: white;
    background: rgba(53, 61, 84, 0.85);

    margin-top: 104px;
  }

  .footer__inner {
    max-width: 1309px;
    height: 100%;

    font-size: 15px;
    line-height: 22px;

    display: flex;
    justify-content: space-between;
    align-items: center;

    margin: 0 auto;
  }

  .footer__icon-wrap {
    width: 30px;
    height: 30px;
    border-radius: 50%;

    display: inline-flex;
    justify-content: center;
    align-items: center;

    background: white;
    color: rgba(53, 61, 84, 0.85);

    &:first-of-type {
      margin-right: 6px;
    }
  }

  .footer__text {
    margin-right: 21px;
  }

  .fa-instagram {
    font-size: 17px;
  }

  .footer__link {
    color: rgba(53, 61, 84, 0.85);

    &:hover {
      cursor: pointer;
      color: rgba(53, 61, 84, 0.85);
    }
  }
</style>