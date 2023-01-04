<script setup>




</script>

<template>
  
  <form id="contact-form" method="post" action="contact.php" role="form" class="formularioHome" novalidate="true">
         <div class="messages"></div>
          <div class="form-group">
              <input id="campo-cantidad" type="number" step="0.01" name="cantidad" class="form-control" placeholder="Cantidad *" required="required" data-error="Escribe la cantidad a convertir.">
              <div class="help-block with-errors"></div>
          </div>
          <div class="form-group">
            <select id="origen" style="border: 1px solid #ced4da;padding: 0.375rem 0.75rem;font-size: 1rem;line-height: 1.5;color: #495057;border-radius: 0.25rem;width:100%">
              <option value="0">Peso Mexicano</option>
              <option value="1">Dólar Estadounidense</option>
              <option value="2">Euro</option>
              <option value="3">Libra</option>
              <option value="4">Yen</option>
              <option value="5">Dólar Canadiense</option>
            </select>
            <div class="help-block with-errors"></div>
          </div>
          <div class="form-group">
            <select id="destino" style="border: 1px solid #ced4da;padding: 0.375rem 0.75rem;font-size: 1rem;line-height: 1.5;color: #495057;border-radius: 0.25rem;width:100%">
              <option value="0">Peso Mexicano</option>
              <option value="1">Dólar Estadounidense</option>
              <option value="2">Euro</option>
              <option value="3">Libra</option>
              <option value="4">Yen</option>
              <option value="5">Dólar Canadiense</option>
            </select>
            <div class="help-block with-errors"></div>
          </div>
          <div style="text-align:right;">
            <div id="btn-calcular-divisa" style="line-height:36px;font-size:18px;text-align:center;width:200px;background-color:#495057;color:white;display:inline-block;cursor:pointer">
              Calcular
            </div>
          </div>
          <div id="contenedor-resultado" style="text-align:center;font-size: 26px;color: #791F0B;font-weight: 700;line-height: 31px;margin-top:20px;">
          </div>

      </form>
</template>

<style scoped>

h1  {
  color: antiquewhite;
}

.item {
  margin-top: 3rem;
  display: flex;
}

.details {
  flex: 1;
  margin-left: 1rem;
}

i {
  display: flex;
  place-items: center;
  place-content: center;
  width: 32px;
  height: 32px;

  color: let(--color-text);
}

h3 {
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: let(--color-heading);
}

@media (min-width: 1024px) {
  .item {
    margin-top: 0;
    padding: 0.4rem 0 1rem calc(let(--section-gap) / 2);
  }

  i {
    top: calc(50% - 25px);
    left: -26px;
    position: absolute;
    border: 1px solid let(--color-border);
    background: let(--color-background);
    border-radius: 8px;
    width: 50px;
    height: 50px;
  }

  .item:before {
    content: ' ';
    border-left: 1px solid let(--color-border);
    position: absolute;
    left: 0;
    bottom: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:after {
    content: ' ';
    border-left: 1px solid let(--color-border);
    position: absolute;
    left: 0;
    top: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:first-of-type:before {
    display: none;
  }

  .item:last-of-type:after {
    display: none;
  }
}
</style>
