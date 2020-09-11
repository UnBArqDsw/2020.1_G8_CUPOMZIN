  <h2>Arquitetura e desenho de software</h2>
  <h3>Sobre o projeto</h3>

  <p>Cuponzim é um projeto que busca facilitar a maneira de você comprar dentro de shoppings,outlets e feiras. Por meio do nosso aplicativo o cliente vai poder encontrar cupons exclusivos para comprar produtos variados com descontos de maneira simplificada. O varejista vai poder cadastrar suas promoções por meio de uma plataforma web voltada para lojas. 
  </p>

  <h3>Membros da equipe</h3>

  <div class="members">
    <div class="member">
      <img src="./assets/img/members/wictor.JPG" alt="member name" style="object-fit: cover;">
      <p>Wictor Girardi<p>
    </div>
    <div class="member">
      <img src="./assets/img/members/zarbielli.jpg" alt="member name" style="object-fit: cover;">
      <p>João Lucas Zarbiélli<p>
    </div>
    <div class="member">
      <img src="./assets/img/members/Ganda.jpg" alt="member name" style="object-fit: cover;">
      <p>Lucas Ganda<p>
    </div>
    </div>
    <div class="member line2">
    <div class="member">
      <img src="./assets/img/members/joao.jpg" alt="member name" style="object-fit: cover;">
      <p>João de Assis<p>
    </div>
    <div class="member">
      <img src="./assets/img/members/andre.jpeg"alt="member name" style="object-fit: cover;">
      <p>André Freitas<p>
    </div>
   
  </div>
  <p align="center"><a href="https://fga.unb.br" target="_blank"><img width="230"src="https://4.bp.blogspot.com/-0aa6fAFnSnA/VzICtBQgciI/AAAAAAAARn4/SxVsQPFNeE0fxkCPVgMWbhd5qIEAYCMbwCLcB/s1600/unb-gama.png"></a></p>
  </p>
</div>

<style>
  .members {
    display: grid; 
    grid-template-columns: auto auto auto;
    margin-top: 20px;
  }
  .member img{
    position: relative;
    height: 200px;
    width: 200px;
    opacity: 1;
    border-style: solid;
    border-radius: 100px;
    border-width: 1px; 
    border-color: rgba(0,0,0,0.3);
    z-index: 3;
    transition: opacity 0.5s !important;
  }
  .member img:hover{
    opacity: 0.4;
    z-index: 1;
  }
  
 .member{
   margin: 20px;
   display: flex;
   justify-content: center;
  }
 
 .member p{
    position: absolute;
    transform: translate(0, 70px);
    z-index: 2;
    color: #fff;
    font-weight: bold;
    font-family: Montserrat;
  }

  h2, p {
    font-family: Montserrat !important;
    font-weight: 500;
  }

  h3 {
    font-family: Montserrat !important;
    font-weight: bold;
  }
</style>
