 <template>
   <button class="button"
   @click="$emit('onClick',label)"
    :class="{double,triple,operation}">
    {{ label }}
   </button>
 </template>
 
 <script>
 export default {
    props:{
        label:{},
        operation:{type:Boolean},
        double:{ type: Boolean},
        triple:{tyṕe: Boolean}
    }
 
 }
 </script>
 
 <style>
 :root{
    --bg-button: #ffffff;
    --border-button: solid 1px #888;

 }
 .button{
    font-size: 1.4em;
    background-color: var(--bg-button);
    border: none;
    border-right: var(--border-button);
    border-bottom: var(--border-button);
   
 }
 .button:active{
    background-color: #ccc;
 }
 .button.double{
    grid-column: span 2;
 }
 .button.triple{
    grid-column: span 3;
 }
 .button.operation{
    background-color: #DA70D6;
    color:#fff
 }
 .button.operation:active{
    background-color: #FF00FF	;
 }
 </style>