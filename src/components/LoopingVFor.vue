<template>
    <div>
        <h1>Looping with v-for</h1>
        <!-- <ul>
         <li v-for="(item, index) in items" :key="item.id">
            {{ index }} - {{ item.text }}
        </li>
        </ul> -->
        <!-- kebab-case -->
        <child-component 
        v-for="(item, index) in items"
         :key="item.id"
         :text="item.text" 
         :index="index"
         ></child-component>
    </div>
</template>
<script>
import ChildComponent from './ChildComponent.vue';

export default {
    components: {
        ChildComponent
    },  // components
    data() {
        return {
            items: [
                { id: 1, text: 'Item 1' },
                { id: 2, text: 'Item 2' },
                { id: 3, text: 'Item 3' }
            ]
        }
    }
}
</script>