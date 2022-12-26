<script>
      let vUsdC=19.0043;
      let vEurC=21.5561;
      let vCanC=20; //let vCanC=N/E;
      let vGbpC=24.0181;
      let vJpyC=0.1768;
      
      let tiposDeCambio=[1, vUsdC,vEurC,vGbpC, vJpyC, vCanC ];
      let simbolos=["MXN", "USD","EUR","GBP", "JPY", "CAD" ];
  export default {
      name: 'CalculateExchangeRate',
          components: { ExchangeValue }


(document).ready(function(){

      $("#btn-calcular-divisa").click(function(){
        let monedaOrigen=$("#origen").val();
        let monedaDestino=$("#destino").val();
        let cantidadConverion=$("#campo-cantidad").val();
        let precioPesos=cantidadConverion*tiposDeCambio[monedaOrigen];
        let precioResultado=Math.round(precioPesos/tiposDeCambio[monedaDestino] * 100) / 100;
        $("#contenedor-resultado").html(cantidadConverion+" "+simbolos[monedaOrigen]+ " = " + precioResultado+" "+simbolos[monedaDestino]);
      });
    }),
}
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
       <div id="btn-calcular-divisa" style="line-height:36px;font-size:18px;text-align:center;width:200px;background-color:#892110;color:white;display:inline-block;cursor:pointer">
         Calcular
       </div>
     </div>
     <div id="contenedor-resultado" style="text-align:center;font-size: 26px;color: #791F0B;font-weight: 700;line-height: 31px;margin-top:20px;">
     </div>

 </form>
</template>
<style>
.formularioHome {
  background-color: rgba(255, 255, 255, 0.8);
  max-width: 550px;
  width: 100%;
  padding: 35px;
  border-radius: 15px;
}
</style>