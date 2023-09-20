<template>
    <article v-for="item in filterItems(items)">
        <h3>{{ item.id }}</h3>
        <h3>{{ item.name }}</h3>
        <h3>{{ item.description }}</h3>
        <h3 class="stock">{{ item.availability }}</h3>
        <h3 class="price">{{ item.price }}</h3>
    </article>
</template>

<script>
export default {
    props: ["items", "searchText"],
    methods:{
        filterItems(items){
            const searchText = this.searchText;
            if (searchText ===""){
                return items;
            }
           return items.filter((item) => {
                if (item.name.indexOf(searchText) !== -1)

                return true;

                if (item.description.indexOf(searchText) !== -1)

                return true;   

                if (item.availability.indexOf(searchText) !== -1)

                return true;

                if (new String(item.price).indexOf(searchText) !== -1)

                return true;
                
                if (new String(item.id).indexOf(searchText) !== -1)
                
                return true;

                return false;

            })
        }
    }
};
</script>