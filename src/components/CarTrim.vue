<script setup>
import { ref } from 'vue';


const props = defineProps({
    vehicle: Object,
    modelName: String,
    trimName: String,
    inList: Boolean,
    thumbnail: String,
    sellingPrice: String,
    includes: String,
    carImg: String,
    defaultTrim: String,
    infoVisible: Boolean
});

const infoIsVisible = ref(props.infoVisible);

const currentTrim = ref(props.vehicle[props.defaultTrim]);

const showTrimInfo = () => {
    infoIsVisible.value = !infoIsVisible.value;
};

const setTrim = (e) => {
    currentTrim.value = props.vehicle[e.target.value];
    console.log(e.target.value)
}

</script>

<template>

    <div class="car-trim" :data-vehicle="vehicle">
        <div v-if="inList" class="list-info">
            <img :src="thumbnail" v-on:click="showTrimInfo"/>
            <h3>{{ modelName }}</h3>
        </div>
       
        <div v-if="infoIsVisible" class="car-trim-info">
            <div class="car-img">
                <h2>{{ modelName + ' ' + trimName }}</h2>
                <img :src="currentTrim" />
                <div class="trim-selector">
                    <button :class="{'selected': currentTrim === vehicle.blackTrim}" v-on:click="setTrim" id="black" class="trim-btn" value="blackTrim">Black</button>
                    <button :class="{'selected': currentTrim === vehicle.silverTrim}" v-on:click="setTrim" id="silver" class="trim-btn" value="silverTrim">Silver</button>
                    <button :class="{'selected': currentTrim === vehicle.redTrim}" v-on:click="setTrim" id="red" class="trim-btn" value="redTrim">Red</button>
                    <button :class="{'selected': currentTrim === vehicle.whiteTrim}" v-on:click="setTrim" id="white" class="trim-btn" value="whiteTrim">White</button>
                </div>
            </div>
            <div class="info">
                <span>Selling Price<br/>
                    <span class="selling-price">{{ sellingPrice }}</span>
                </span>
                <span class="includes">{{ includes }}</span>
            </div>
        </div>
    </div>

</template>

<style scoped>

.list-info{
    align-items: center;
    display: flex;
    flex-direction: column;
    gap: 0px;
}

.car-trim{
    cursor: pointer;
}

.car-trim-info{
    background: #FFF;
    border: 1px solid #E1E1E1;
    border-radius: 6px;
    display: flex;
    flex-direction: column;
    gap: 40px;
    left: -10px;
    margin: 40px;
    position: absolute;
    padding: 40px;
    top: 200px;
    width: 850px; 
    z-index: 99;
}

.car-trim-info span{
    display: block;
}

.selling-price{
    font-size: 22px;
    font-weight: 600;
}

.includes{
    font-size: 12px;
    font-weight: 300;
}

.car-img img{
    display: block;
    width: auto;
    height: 100%;
}

.trim-selector{
    display: flex;
    gap: 20px;
}

.trim-btn{
    border-radius: 50%;
    border: none;
    cursor: pointer;
    display: block;
    height: 62px;
    width: 62px;
}

.selected {
    border: 4px solid #399be4 !important;
}

#silver{
    background: #2B2D30;
    color: #FFF;
}

#red{
    background: #82001D;
    color: #FFF;
}

#black{
    background: #000000;
    color: #FFF;
}

#white{
    background: #FFFFFF;
    border: 1px solid #000;
    color: #000;
}


</style>