<template>
    <div class="filter_side_bar">

        <div class="items" v-for="item, index of filtersData" :key="index">

            <span v-if="item.filter_lable == 'Category'">
            <div v-on:click="dropDownMenu(item)">{{ item.filter_lable }}</div>
            <span v-bind:class="{'Category': Categorystate}" class="dropdown-menu">
                <ul v-for="(item, index) of item.options" :key="index">
                    <input type="checkbox" /> {{ item.value }}
                </ul>
            </span>
        </span>

            <span v-if="item.filter_lable == 'Price'" >
               <div v-on:click="dropDownMenu(item)">{{ item.filter_lable }}</div>
                <span v-bind:class="{'Price': PriceState}" class="dropdown-menu">
                    <ul v-for="(item, index) of item.options" :key="index">
                        <input type="checkbox" />{{ item.value }}
                    </ul>
                </span>
            </span>

            <span v-if="item.filter_lable == 'Discount'" >
               <div v-on:click="dropDownMenu(item)">{{ item.filter_lable }}</div>
                <span v-bind:class="{'Discount': DiscountState}" class="dropdown-menu">
                    <ul v-for="(item, index) of item.options" :key="index">
                        <input type="checkbox" />
                        {{ item.value }}
                    </ul>
                </span>
            </span>

            <span v-if="item.filter_lable == 'Colour'" >
               <div v-on:click="dropDownMenu(item)">{{ item.filter_lable }}</div>
                <span v-bind:class="{'Colour': ColourState}" class="dropdown-menu">
                    <ul v-for="(item, index) of item.options" :key="index">
                        <input type="checkbox" />
                        {{ item.value }}
                    </ul>
                </span>
            </span>

            <span v-if="item.filter_lable == 'Size'" >
               <div v-on:click="dropDownMenu(item)">{{ item.filter_lable }}</div>
                <span v-bind:class="{'Size': SizeState}" class="dropdown-menu">
                    <ul v-for="(item, index) of item.options" :key="index">
                        <input type="checkbox" />
                        {{ item.value }}
                    </ul>
                </span>
            </span>

            <span v-if="item.filter_lable == 'Neck Type'" >
               <div v-on:click="dropDownMenu(item)">{{ item.filter_lable }}</div>
                <span v-bind:class="{'NeckType': NeckTypeState}" class="dropdown-menu">
                    <ul v-for="(item, index) of item.options" :key="index">
                        <input type="checkbox" />
                        {{ item.value }}
                    </ul>
                </span>
            </span>

            <span v-if="item.filter_lable == 'Sleeve'" >
               <div v-on:click="dropDownMenu(item)">{{ item.filter_lable }}</div>
                <span v-bind:class="{'Sleeve': SleeveState}" class="dropdown-menu">
                    <ul v-for="(item, index) of item.options" :key="index">
                        <input type="checkbox" />
                        {{ item.value }}
                    </ul>
                </span>
            </span>

            <span v-if="item.filter_lable == 'Occasion'" >
               <div v-on:click="dropDownMenu(item)">{{ item.filter_lable }}</div>
                <span v-bind:class="{'Occasion': OccasionState}" class="dropdown-menu">
                    <ul v-for="(item, index) of item.options" :key="index">
                        <input type="checkbox" />
                        {{ item.value }}
                    </ul>
                </span>
            </span>

            <span v-if="item.filter_lable == 'Length'" >
               <div v-on:click="dropDownMenu(item)">{{ item.filter_lable }}</div>
                <span v-bind:class="{'Length': LengthState}" class="dropdown-menu">
                    <ul v-for="(item, index) of item.options" :key="index">
                        <input type="checkbox" />
                        {{ item.value }}
                    </ul>
                </span>
            </span>

            <span v-if="item.filter_lable == 'Fastening/Closure'" >
               <div v-on:click="dropDownMenu(item)">{{ item.filter_lable }}</div>
                <span v-bind:class="{'Fastening': FasteningState}" class="dropdown-menu">
                    <ul v-for="(item, index) of item.options" :key="index">
                        <input type="checkbox" />
                        {{ item.value }}
                    </ul>
                </span>
            </span>

            <span v-if="item.filter_lable == 'Pattern'" >
               <div v-on:click="dropDownMenu(item)">{{ item.filter_lable }}</div>
                <span v-bind:class="{'Pattern': PatternState}" class="dropdown-menu">
                    <ul v-for="(item, index) of item.options" :key="index">
                        <input type="checkbox" />
                        {{ item.value }}
                    </ul>
                </span>
            </span>

            <span v-if="item.filter_lable == 'Ornamentation'" >
               <div v-on:click="dropDownMenu(item)">{{ item.filter_lable }}</div>
                <span v-bind:class="{'Ornamentation': OrnamentationState}" class="dropdown-menu">
                    <ul v-for="(item, index) of item.options" :key="index">
                        <input type="checkbox" />
                        {{ item.value }}
                    </ul>
                </span>
            </span>

            <span v-if="item.filter_lable == 'Fabric Family'" >
               <div v-on:click="dropDownMenu(item)">{{ item.filter_lable }}</div>
                <span v-bind:class="{'FabricFamily': FabricFamilyState}" class="dropdown-menu">
                    <ul v-for="(item, index) of item.options" :key="index">
                        <input type="checkbox" />{{ item.value }}
                    </ul>
                </span>
            </span>

            <span v-if="item.filter_lable == 'Closure'" >
               <div v-on:click="dropDownMenu(item)">{{ item.filter_lable }}</div>
                <span v-bind:class="{'Closure': ClosureState}" class="dropdown-menu">
                    <ul v-for="(item, index) of item.options" :key="index">
                        <input type="checkbox" />
                        {{ item.value }}
                    </ul>
                </span>
            </span>

            
            







        </div>

      <!-- <div v-for="item of filtersData" :key="item.id">
        <div v-on:click="dropDownMenu(item)">{{ item.filter_lable }}</div>
        <div v-if="classItem == 'Category'">
            <div>
                <span v-bind:class="item.filter_lable" class="dropdown-menu">
                <ul v-for="(item, index) of item.options" :key="index">
                    <input type="checkbox" />
                    {{ item.value }}
                </ul>
            </span>
            </div>
        </div>  
        <div v-if="classItem == 'Price'">
            <div>
                <span v-bind:class="item.filter_lable" class="dropdown-menu">
                <ul v-for="(item, index) of item.options" :key="index">
                    <input type="checkbox" />
                    {{ item.value }}
                </ul>
            </span>
            </div>
        </div>  
      </div> -->

    </div>

</template>

<script>
import axios from 'axios';
export default {
    name: 'SideNav',
    data() {
        return {
            filtersData: null,
            dropDownMenuState: false,
            classItem: null,
            Categorystate: false,
            PriceState: false,
            DiscountState: false,
            ColourState: false,
            SizeState: false,
            NeckTypeState: false,
            SleeveState: false,
            OccasionState: false,
            LengthState: false,
            FasteningState: false,
            PatternState: false,
            OrnamentationState: false,
            FabricFamilyState: false,
            ClosureState: false,
        }
    },

    created(){
        axios.get('https://pim.wforwoman.com/pim/pimresponse.php/?service=category&store=1&url_key=top-wear-kurtas&page=1&count=20&sort_by=&sort_dir=desc&filter=').
        then(resp => {
         this.filtersData = resp.data.result.filters
         console.log("the filters respinse in created hook is", this.filtersData)
        })
    },

    methods: {
        dropDownMenu(item){
            // this.dropDownMenuState = !this.dropDownMenuState
            // console.log("the index is", index)
            // this.indexItem = index
            this.classItem =  item.filter_lable
            console.log("the ote, value is", item.filter_lable)

            if(item.filter_lable == 'Category') {
                this.Categorystate = !this.Categorystate
            }
            else if(item.filter_lable == 'Price'){
                this.PriceState = !this.PriceState
            }
            else if(item.filter_lable == 'Discount'){
                this.DiscountState = !this.DiscountState
            }
            else if(item.filter_lable == 'Colour'){
                this.ColourState = !this.ColourState
            }
            else if(item.filter_lable == 'Size'){
                this.SizeState = !this.SizeState
            }
            else if(item.filter_lable == 'Neck Type'){
                this.NeckTypeState = !this.NeckTypeState
            }
            else if(item.filter_lable == 'Sleeve'){
                this.SleeveState = !this.SleeveState
            }
            else if(item.filter_lable == 'Occasion'){
                this.OccasionState = !this.OccasionState
            }
            else if(item.filter_lable == 'Length'){
                this.LengthState = !this.LengthState
            }
            else if(item.filter_lable == 'Fastening/Closure'){
                this.FasteningState = !this.FasteningState
            }
            else if(item.filter_lable == 'Pattern'){
                this.PatternState = !this.PatternState
            }
            else if(item.filter_lable == 'Ornamentation'){
                this.OrnamentationState = !this.OrnamentationState
            }
            else if(item.filter_lable == 'Fabric Family'){
                this.FabricFamilyState = !this.FabricFamilyState
            }
            else if(item.filter_lable == 'Closure'){
                this.ClosureState = !this.ClosureState
            }
            
            
        }

    }

}



</script>

<style scoped>

.filter_heading{
    font-size: 20px;
    font-weight: 600;
}
  .filter_side_bar {
    position: relative;
    display: flex;
    flex-direction: column;
    flex: block;
    margin-left: 20px;
  }

  .filter_side_bar .items {
    border: 0.5px solid rgb(195, 192, 192);
    display: flex;
    /* margin:5px; */
    padding: 20px;
    /* height: 30px; */
    /* display: flex; */
    /* flex-direction: column; */
    align-items:flex-start;
    /* justify-content: flex-start; */
  }



 .dropdown-menu {
  display: none;
}

.Category{
    display: block;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    margin-top: 0px;
    margin-left: 0px;
    padding: 0px;
}

.Category ul {
    margin: 5px;
    padding: 0px;
}

.Category ul input {
    align-items: flex-start;
    justify-content: flex-start;
    margin-right: 7px ;
}



.Price{
    display: block;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    margin-top: 0px;
    margin-left: 0px;
    padding: 0px;
}

.Price ul {
    margin: 5px;
    padding: 0px;
}

.Price ul input {
    align-items: flex-start;
    justify-content: flex-start;
    margin-right: 7px ;
}


.Discount{
    display: block;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    margin-top: 0px;
    margin-left: 0px;
    padding: 0px;
}

.Discount ul {
    margin: 5px;
    padding: 0px;
}

.Discount ul input {
    align-items: flex-start;
    justify-content: flex-start;
    margin-right: 7px ;
}

.Colour{
    display: block;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    margin-top: 0px;
    margin-left: 0px;
    padding: 0px;
}

.Colour ul {
    margin: 5px;
    padding: 0px;
}

.Colour ul input {
    align-items: flex-start;
    justify-content: flex-start;
    margin-right: 7px ;
}

.Size{
    display: block;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    margin-top: 0px;
    margin-left: 0px;
    padding: 0px;
}

.Size ul {
    margin: 5px;
    padding: 0px;
}

.Size ul input {
    align-items: flex-start;
    justify-content: flex-start;
    margin-right: 7px ;
}


.NeckType{
    display: block;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    margin-top: 0px;
    margin-left: 0px;
    padding: 0px;
}

.NeckType ul {
    margin: 5px;
    padding: 0px;
}

.NeckType ul input {
    align-items: flex-start;
    justify-content: flex-start;
    margin-right: 7px ;
}

.Sleeve{
    display: block;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    margin-top: 0px;
    margin-left: 0px;
    padding: 0px;
}

.Sleeve ul {
    margin: 5px;
    padding: 0px;
}

.Sleeve ul input {
    align-items: flex-start;
    justify-content: flex-start;
    margin-right: 7px ;
}

.Occasion{
    display: block;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    margin-top: 0px;
    margin-left: 0px;
    padding: 0px;
}

.Occasion ul {
    margin: 5px;
    padding: 0px;
}

.Occasion ul input {
    align-items: flex-start;
    justify-content: flex-start;
    margin-right: 7px ;
}

.Length{
    display: block;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    margin-top: 0px;
    margin-left: 0px;
    padding: 0px;
}

.Length ul {
    margin: 5px;
    padding: 0px;
}

.Length ul input {
    align-items: flex-start;
    justify-content: flex-start;
    margin-right: 7px ;
}

.Fastening{
    display: block;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    margin-top: 0px;
    margin-left: 0px;
    padding: 0px;
}

.Fastening ul {
    margin: 5px;
    padding: 0px;
}

.Fastening ul input {
    align-items: flex-start;
    justify-content: flex-start;
    margin-right: 7px ;
}

.Pattern {
    display: block;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    margin-top: 0px;
    margin-left: 0px;
    padding: 0px;
}

.Pattern ul {
    margin: 5px;
    padding: 0px;
}

.Pattern ul input {
    align-items: flex-start;
    justify-content: flex-start;
    margin-right: 7px ;
}

.Ornamentation{
    display: block;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    margin-top: 0px;
    margin-left: 0px;
    padding: 0px;
}

.Ornamentation ul {
    margin: 5px;
    padding: 0px;
}

.Ornamentation ul input {
    align-items: flex-start;
    justify-content: flex-start;
    margin-right: 7px ;
}

.FabricFamily{
    display: block;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    margin-top: 0px;
    margin-left: 0px;
    padding: 0px; 
}

.FabricFamily ul {
    margin: 5px;
    padding: 0px;
}

.FabricFamily ul input {
    align-items: flex-start;
    justify-content: flex-start;
    margin-right: 7px ;
}

.Closure{
    display: block;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    margin-top: 0px;
    margin-left: 0px;
    padding: 0px; 
}

.Closure ul {
    margin: 5px;
    padding: 0px;
}

.Closure ul input {
    align-items: flex-start;
    justify-content: flex-start;
    margin-right: 7px ;
}






</style>
