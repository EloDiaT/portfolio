<template>
  <aside class="ViewScroll">
    <div>
      <span class="ViewScroll_text">Скроль</span>
      <div class="ViewScroll_arrow">
        <div class="arrow-8">
        </div>
      </div>
    </div>
  </aside>
</template>

<style lang="scss">
  .ViewScroll {
    height: 5.5em;
    position: absolute;
    top: 3em;
    @media all and (max-width: 768px) {
      display: none;
    }
    .ViewScroll_text {
      color: $green;
      @extend .font-ml;
    }
    .ViewScroll_arrow {
      margin-left: 1.3em;
      position: relative;
      width: 2em;
      height: 2em;
      &:before,
      &:after {
          content: '';
          position: absolute;
          box-sizing: border-box;
          width: 100%;
          height: 100%;
          border-left: .2em solid $green;
          border-bottom: .2em solid $green;
          animation: arrow-8 3s linear infinite;
      }
      &:after {
        animation: arrow-8 3s linear infinite -1.5s;
      }
    }
  }
@keyframes arrow-8 {
    0% {
        opacity: 0;
        transform: translate(0, -1em) rotate(-45deg);
    }
    10%, 90% {
        opacity: 0;
    }
    50% {
        opacity: 1;  
        transform: translate(0, 0) rotate(-45deg);
    }
    100% {
        opacity: 0;
        transform: translate(0, 1em) rotate(-45deg);
    }
}
</style>