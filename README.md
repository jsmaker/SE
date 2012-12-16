SE
==

Simple Events

//create pubsub

var p = pubsub()

function log(msg){
    console.log(msg);
}

//set a once event
p.once('go', log);

//try to fire the events
p.publish('go', 'hi');
p.publish('go', 'hi');
p.publish('go', 'hi');

// output : "hi" 



p.subscribe('go' , log);

p.unsubscribe('go' , log);

p.clear('go'); //only one topic

p.clear(); //all

p.getCache('go') 
p.getCache()

