<template>
<div>
    <h1>Vue Js Events</h1>

    <button @click="GetData('welcome to parameter passsing')">Get Data 1</button>
</div>
<button @click="ClickMe()">click me</button>
<button @mouseover="HoverMe()">Hover me</button>
<div>
    <button @click="GetData('welcome to Second parameter passsing')">Get Data 2</button>
</div>
<button @dblclick="DoubleClickMe()">Double click me</button>
<button @mouseover="HoverMe()">Mouse Move</button>
<button @click="Count()">Count Addition</button>
<div>
    <button @click="CountMinus()">Count Subtraction</button>
</div>
<h1>{{count}}</h1> <br />
<div>
    <h2>Two Way binding using model and vue</h2>
    <input type="text" v-model="text" />
    <p>{{text}}</p>
</div>

<div>
    <input type="text" placeholder="username" v-model="username" />
    <br>
    <input type="password" placeholder="password" v-model="password" />
    <br>
    <button @click="getFormData()" type="button"> submit</button>
</div>

<div>
    <h2>technologies checkboxes</h2>
    <label for="java">Java</label>
    <input type="checkbox" value="java" v-model="technologies" id="java" />
    <br />
    <label for="python">Python</label>
    <input type="checkbox" value="python" v-model="technologies" id="python" />
    <br />
    <label for="javascript">JavaScript</label>
    <input type="checkbox" value="javascript" v-model="technologies" id="javascript" />
    <br />
    <div>
        <h3> Gender</h3> <br />
        <label for="male">Male</label>
        <input type="radio" value="Male" v-model="gender" id="male" />
        <br />
        <label for="female">Female</label>
        <input type="radio" value="Female" v-model="gender" id="female" />
    </div>

    <h2>You know Technologies: {{technologies}}</h2>
    <h2> Your Gender is : {{gender}}</h2>
</div>

<div>
    <h2>Conditions If Else</h2>
    <h3 v-if="show">If Condition</h3>
    <h3 v-else>Else Condition</h3>
    <button @click="show=!show"> Show </button>
</div>
<h2> For Loop in VUE JS</h2>
<ul>
    <li v-for="items in languages" :key="items">
        {{items}}
    </li>
</ul>
<h2> For Loop in VUE JS with array object</h2>
<ul v-for="items in user" :key="items">
    <li>
        your name is {{items.name}} and your email is {{items.email}}<br />
    </li>
</ul>
<ChildModule name="hlo this is props" :userdata="userdata" :getData="getData" />
<div class="rr">
    New Child Here
    <ul>
        <li v-for="lists in datauser" :key="lists">
            <NewChild :data="lists" :nameData="nameData" />
        </li>
    </ul>
</div>
<HtmlBinding name="akshay" />
<h1>{{DataName}}</h1>
<ChildtoParent :GetUserr="GetUser" />
<br />
<br />
<input type="text" ref="text" />
<input type="text" ref="pass" />
<button type="submit" @click="RefData">Ref Using Button</button>
<br />
<br />
<div>

<RegistrationForm />

</div>

</template>

<script>
import ChildtoParent from './ChildtoParent.vue'
import ChildModule from './ChildModule.vue'
import NewChild from './NewChild.vue'
import HtmlBinding from './HtmlBinding.vue'
import RegistrationForm from './RegistrationForm.vue'
export default {
    name: 'HelloWorld',
    components: {
        ChildModule,
        NewChild,
        HtmlBinding,
        ChildtoParent,
        RegistrationForm,
    },

    data() {
        return {
            DataName: "",
            count: 0,
            text: 'write here',
            username: null,
            password: null,
            technologies: [],
            gender: null,
            show: true,
            languages: ['hindi', 'english', 'punjabi', 'French'],
            userdata: {
                name: 'akshay',
                email: 'ak@test.com'
            },
            datauser: [{
                    name: 'akshay',
                    email: 'ak@email.com'
                },
                {
                    name: 'vishal',
                    email: 'vk@email.com'
                },
                {
                    name: 'aprita',
                    email: 'ap@email.com'
                },
                {
                    name: 'sanjay',
                    email: 'sanjay@email.com'
                },
                {
                    name: 'prateek',
                    email: 'prateek@email.com'
                },
            ],
            user: [{
                    name: 'akshay',
                    email: 'akshay@me.com'
                },
                {
                    name: 'abhay',
                    email: 'abhay@me.com'
                },
                {
                    name: 'aprita',
                    email: 'aprita@me.com'
                },
                {
                    name: 'vishal',
                    email: 'vishal@me.com'
                }
            ],
        }
    },
    methods: {
        nameData(name) {
            alert(this.userName = name);
        },
        GetUser(names) {
            this.DataName = names;
        },
        RefData() {
             this.$refs.text.style.background='black'
             this.$refs.text.style.color='white'
             this.$refs.pass.style.background='green'
              this.$refs.text.focus()
             let val = this.$refs.text.value
             let pass = this.$refs.pass.value
             console.log(val,pass);
            

        },
        getData() {
            console.warn("you bro your program is running");
            alert("hey buddy parent function called");
        },
        ClickMe() {
            alert("On Click working properly");
        },
        getFormData() {
            console.log("your username is", this.username, "your password is", this.password);
        },
        HoverMe() {
            alert("Hover Working Man");
        },
        GetData(data) {
            alert(data);
        },
        DoubleClickMe() {
            alert("Double Clicked event");
        },
        Count() {
            this.count = this.count + 1;
        },
        CountMinus() {
            this.count = this.count - 1;
        }
    }
}
</script>

<style scoped>
h3 {
    margin: 40px 0 0;
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
    display: inline-block;
    margin: 0 10px;
}

a {
    color: #42b983;
}

.rr {
    background-color: red;
}
</style>
