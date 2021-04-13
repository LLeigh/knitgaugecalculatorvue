<template>
  <div>
    <img class="bitmoji" alt="knitting-bitmoji" src="@/assets/knitbitmoji.png">
    <h1>Welcome to the Knitting Gauge Calculator!</h1>
    <p>Your knitting gauge doesn't match the pattern's gauge... NOW WHAT? All the math involved in 
        figuring out what size you should knit can be daunting. I've created this step-by-step
        guide to help you through it. If you are know exactly what you came here for, smash that 
        "Let's get Started" button below. Confused? Read on!</p>
            <img class="icon" src="@/assets/icon.svg">
    <h3>What is Knitting Gauge and why should I care?</h3>
    <p>Knitting gauge is a term used to describe stitches per inch. Most patterns use a 4-inch gauge 
        swatch to illustrate stitches across (side to side) and stitches in rows (top to bottom). The 
        gauge is defined by length by rows. An example of a knitting gauge swatch would be 16 x 24, 
        which would be 16 stitches per 4 inch in length and 24 rows per 4 inches top to bottom.
    <br>
    <p>Most knitwear designers will suggest a specific yarn and needle size to use when knitting the pattern.
        But, what if you want to use a different yarn? What if you don't like the fabric that the suggested 
        needle size produces? Or, what if your knitting tension just produces a different gauge? Getting 
        comfortable with dealing with knitting in a different gauge than the pattern means you will be less 
        restricted by the pattern's suggestions.</p>
    <a href="#" class="btn-enter">Let's get Started!</a>

  </div>
</template>

<script>
export default {
    name: 'Welcome',


}
</script>

<style> 
.icon {
    max-width: 40px;
    padding: 5px;
}

.btn-enter{
	box-shadow:inset -7px -17px 0px -5px #da397c;
	background-color:#f1468e;
	border-radius:42px;
	display:inline-block;
	cursor:pointer;
	color:#ffffff;
	font-family:Arial;
	font-size:21px;
	padding:12px 43px;
	text-decoration:none;
}
.btn-enter:hover {
	background-color:#f179ab;
  box-shadow:inset -7px -17px 0px -5px #f37eaf;
}
.btn-enter:active {
	position:relative;
	top:1px;
}


</style>