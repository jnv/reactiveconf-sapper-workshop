<script>
  export let segment;
</script>

<style>
  a {
    color: #fff;
    display: inline-block;
    line-height: 1.5;
    font-size: 16px;
    text-decoration: none;
    font-weight: 500;
    padding: 15px 0;
    text-transform: capitalize;
    transition: all 0.2s ease-in-out 0s;
  }

  a:hover {
    color: #bc8d4b;
  }
  nav {
    display: flex;
  }

  ul,
  li,
  a {
    width: 100%;
  }

  .selected {
    color: #bc8d4b;
    position: relative;
  }

  @media only screen and (min-width: 768px) {
    ul {
      display: flex;
      flex-direction: row;
    }

    ul,
    li,
    a {
      width: auto;
    }

    a {
      padding: 16px 25px;
      font-size: 20px;
    }

    .selected::after {
      position: absolute;
      content: '';
      width: calc(100% - 50px);
      height: 2px;
      background-color: #bc8d4b;
      display: block;
      bottom: 0;
    }
  }
</style>

<nav>
  <ul>
    <li on:click>
      <a class={segment === undefined ? 'selected' : ''} href=".">home</a>
    </li>
    <li on:click>
      <a class={segment === 'about' ? 'selected' : ''} href="about">about</a>
    </li>
    <li on:click>
      <a
        rel="prefetch"
        class={segment === 'offer' ? 'selected' : ''}
        href="offer">
        offer
      </a>
    </li>
  </ul>
</nav>
