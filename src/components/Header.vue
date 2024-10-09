

<template>
  <header class="header">
    <div class="header__items">
      <img
          src="https://fakeimg.pl/100x50/"
          class="header__items__logo"
          alt=""
        />
      <nav class="nav__bar">
          <ul>
            <li>
              <a href="">HOME</a>
            </li>
          </ul>
          <ul>
            <li>
              <a href="">COMO PARTICIPAR</a>
            </li>
          </ul>
          <ul>
            <li>
              <a href="">PRÊMIOS</a>
            </li>
          </ul>
          <ul>
            <li>
              <a href="">DUVIDAS FREQUENTES</a>
            </li>
          </ul>
          <ul>
            <li>
              <a href="">GANHADORES</a>
            </li>
          </ul>
        <ul>
          <li>
            <button type="button">LOGIN</button>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style scoped>
.header{
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
  background-color: #fff;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  display: flex;
  justify-content: center;
  height: 100px;
  background-color: #d9e1df;
}

a{
  color:black
}

.nav__bar{
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 0 3rem;
}
.header__items{
  display: flex;
  padding-inline: 2rem;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}
.nav__bar ul{
  list-style: none;
}

@media (max-width: 1024px){
  .header__items{
    position: static;
    flex-direction: column;
    gap: 1rem;
  }
  .nav__bar{
    flex-direction: column;
    gap: 1rem;
  }
  .header{
    height: auto;
    position: inherit;
    padding: 1rem 0;
  }
}
</style>
