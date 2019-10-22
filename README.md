# beee-evaluation-phase-1
void setup(){
	  pinMode(13, OUTPUT);
	  pinMode(5,INPUT);
	  pinMode(7,OUTPUT);
	  Serial.begin(9600);
	}
	int time;
	int dis;
	void loop(){
	  
	  
	  digitalWrite(7,LOW);
	  digitalWrite(7,HIGH);
	  delayMicroseconds(10);
	  digitalWrite(7,LOW);
	  time=pulseIn(5,HIGH);
	  dis=time/29/2;
	  if(dis<10){
	  digitalWrite(13, HIGH);
	  delay(2);
	    digitalWrite(13,LOW);
	    delay(1000);
	  }else{
	    digitalWrite(13,LOW);
	}
	}
