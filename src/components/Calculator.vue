<template>
  <div class="calculator">
    <div>
      <h1>Knitting Gauge Calculator</h1>
      <h3>You will need:</h3>
      <ul>
        <li>1 - Your pattern</li>
        <li>2 - Your 4 inch (or cm) by 4 inch gauge swatch measurements - length & rows</li>
        <li>3 - Your desired measurements for the garment.</li>
      </ul>
      <h3>How to use the Knitting Gauge Calculator:</h3>
      <p>Simply fill out the form field below. As you type in your input, the information in the 
        "Results" section will auto-fill accordingly.</p>
    </div>
    <form>
      <div>
        <label for="pattern-gauge">Pattern Gauge: </label>
          <input type="text" placeholder="stitches across" v-model="patternGaugeLength">
          &nbsp;x&nbsp;
          <input type="text" placeholder="stitches up and down" v-model="patternGaugeRows">
      </div>
      <br/>
      <div>
        <label for="knitters-gauge">Your Gauge: </label>
          <input type="text" placeholder="stitches across" v-model="knittersGaugeLength">
          &nbsp;x&nbsp;
          <input type="text" placeholder="stitches up and down" v-model="knittersGaugeRows">
      </div>
      <div>
        <p>Now, look at your pattern. Pick a length measurement that will determine the fit of the garment. 
          I recommend picking a measurement, such as "bust" or "body circumference."</p>
          <p>***Keep in Mind*** You are able to check mutliple lengths by just inputting a different length into the "length measurement" field.</p>
        <p>Then, you will need to measure yourself. Compare the masurement you took to the options in the pattern.
          and pick the closest one to yours. If you are off by several inches, you will need to decide if you are 
          ok with either positive or negative ease in your finished garment.
        </p>
      </div>
      <div>
        <label for="lengthMesurement">What is the closest length measurement in your pattern? </label>
        <input type="text" placeholder="length measurement" v-model="lengthMeasurement">
      </div>

    </form>
    <section>
      <h2>Results:</h2>
      <h4>Your Entered:</h4>
      <p>The pattern's gauge is <span> {{ patternGaugeLength }} </span> inches by <span> {{ patternGaugeRows }} </span>inches.</p>
      <p>Your knitting gauge is <span> {{ knittersGaugeLength }} </span> inches by <span> {{ knittersGaugeRows }} </span>inches. </p> 
      <p>Your desired length is <span> {{ lengthMeasurement }} </span>.</p>

      <h4>Based on your measurements:</h4>
      <p>The measurement with pattern gauge (<span> {{ patternGaugeLength }} </span> x <span> {{ patternGaugeRows }} </span>) 
      would be <span> {{ patternStitchesInMeasurement }} </span> stitches.</p>

      <p>With your gauge (<span> {{ knittersGaugeLength }} </span> x <span> {{ knittersGaugeRows }} </span>)
       you end up with <span> {{ knitterStitchesInMeasurement }} </span> stitches.</p> 

      <p>Now, look at your pattern. Find where they define final stitch counts for the final length of area 
      you chose to measure.</p>
      <p>Pick the size of the pattern that is closest to your stitch count of 
      <span> {{ knitterStitchesInMeasurement }} </span>.</p>
          
      <img class="icon" src="@/assets/icon.svg">

    </section>


    
  </div>
</template>

<script>
export default {
  name: 'calculator',
  data() {
        return {
                patternGaugeLength: '',
                patternGaugeRows: '',
                knittersGaugeLength: '',
                knittersGaugeRows: '',
                lengthMeasurement: ''
              
        }
        
    },
    computed: {
      
      stitchesPerInch(gaugeLength) {
        return gaugeLength / 4;
      },

      patternStitchesInMeasurement() {
        return this.lengthMeasurement * (this.patternGaugeLength / 4);
      },

      knitterStitchesInMeasurement() {
        return this.lengthMeasurement * (this.knittersGaugeLength / 4);
      } 
    }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
li {
  list-style: none;
}

</style>
