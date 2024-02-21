<script setup>
import { reactive } from 'vue';

const quote = reactive({
    id: "",
    quote: "",
    anime: "",
    character: ""
});

const fetchQuote = async () => {
  try {
    const response = await fetch('https://animechan.xyz/api/random');
    const data = await response.json();
    quote.id = data.id;
    quote.quote = data.quote;
    quote.anime = data.anime;
    quote.character = data.character;
  } catch (error) {
    // Handle error
    console.log('Error fetching quote:', error);
  }
};
fetchQuote();
</script>

<template>
    <div>
      <div v-if="quote.id">
        <ul class="d-flex flex-col gap-5">
            <li class="text-left text-1xl flex gap-2">
                <span class="font-bold uppercase">ID:</span> {{ quote.id }}
            </li>
            <li class="text-left text-1xl flex gap-2 mt-2">
                <span class="font-bold uppercase">quote:</span> {{ quote.quote }}
            </li>
            <li class="text-left text-1xl flex gap-2 mt-2">
                <span class="font-bold uppercase">anime:</span> {{ quote.anime }}
            </li> 
            <li class="text-left text-1xl flex gap-2 mt-2">
                <span class="font-bold uppercase">character:</span> {{ quote.character }}
            </li>
        </ul>
        </div>
    </div>
</template>