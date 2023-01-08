<template>
    <div class="currencyConverterStructure">
        <form class="frConverter">
<div>
	<span>Yo tengo</span>
	<select name="base_currency"></select>
	<input type="hidden" name="default_base" value="usd"/>
	<input type="text" name="base_value" size="5" value="1"/>
</div>
<div>
	<span>Yo quiero</span>
	<select name="target_currency" onChange="frExCalc();"></select>
	<input type="hidden" name="default_target" value="eur"/>
	<input type="text" name="target_value" size="5" value=""/>
</div>
<br/><a class="frLink" href="//www.floatrates.com/"></a>
</form>
    </div>
</template>

<script type="text/javascript">
  (function() {
    var js = document.createElement('script'); js.type = 'text/javascript'; js.async = true;
    js.src = '//www.floatrates.com/scripts/converter.js';
    var sjs = document.getElementsByTagName('script')[0]; sjs.parentNode.insertBefore(js, sjs);
  })();
</script>
<style lang="css">

span {
  color: white;
}
.currencyConverterStructure  {
    justify-content:center;
    align-items:center;
    display:flex;

}
a, #frLink1 {
background-color: rgb(44, 44, 45);;
}
</style>