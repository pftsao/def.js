一个简单的 Ruby 风格的 JavaScript 继承
============================================

## 示例

	def ("Person") ({
		init: function(name){
			this.name = name;
		},
		
		speak: function(text){
			alert(text || "Hi, my name is " + this.name);
		}
	});
	
	def ("Ninja") << Person ({
		init: function(name){
			this._super();
		},
		
		kick: function(){
			this.speak("I kick u!");
		}
	});
	
	var ninjy = new Ninja("JDD");
	
	ninjy.speak();
	ninjy.kick();
