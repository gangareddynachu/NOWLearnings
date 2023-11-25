//Parent
var Calculator = Class.create();
Calculator.prototype = {
    initialize: function() {
    },
	add: function(a,b){
		return a+b;
	},
	subtract: function(a,b){
         return a-b;
	},

    type: 'Calculator'
};


//Child
var calculatorChild = Class.create();
calculatorChild.prototype = Object.extendsObject(Calculator,{
    initialize: function() {
    },

	div: function(a,b){
		return a/b;
	},
	add: function(a,b){
		return 100+a+b;
	},

    type: 'calculatorChild'
});



var calobj =  new Calculator() // parent
var calobj1 =  new calculatorChild() //child
gs.info(calobj.add(2,3))  // parent add method
gs.info(calobj1.add(2,3)) //override the parent add method
gs.info(calobj1.div(2,3)) // access the div method available in child 

*** Script: 5
*** Script: 105
*** Script: 0.6666666666666666
