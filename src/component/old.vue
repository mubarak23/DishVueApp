components:{
    'app-spice':Spice,
    'app-header': Header,
    'app-footer': Footer

  },
  
  data () {
    return {
        spices:[
        {name: 'Shawarma', Audience:'Young Ladies', show:false },
        {name: 'Snacks', Audience:'Young Guys', show:false },
        {name: 'Chicken', Audience:'Young Ladies, Guys and Children', show:false },
        {name: 'Pizza', Audience:'Working Class', show:false }
          ],
       title:"The Spice App Home"   
    }
  },

  methods:{
    updateTitle:function(updateTitle){
        this.title = updateTitle
    }
  }
    

    <div>
  <form-helper>
    <div slot="form-header">
      <h2>Review Form</h2>
    </div>
    <div slot="form-field">
      <input type="text" placeholder="Name" required />
      <input type="password" placeholder="Password" required />
    </div>
    <div slot="form-control">
    <button v-on:@click="handleSubmit">Login</button>
    </div>
  </form-helper>
  </div>