# pd7
load('Windturbinetests.txt');
load('weatherpaterns.txt');
resistance = input('What is the resistance in Ohms?');
protoblade=input('What is the prototype blade length?');
bladelength=input('What is the blade length?');
velocity=Windturbinetests(:,1);
voltage=Windturbinetests(:,2);
Pobserved=(((voltage).^2)./resistance);
Cp=0.35;
rho=1.2;
Ng=0.80;
p=1.2;
Nb=0.95;
Ptheoretical=0.5*p*Nb*Cp*Ng*A*velocity.^3;
time=(60*weatherpaterns(:,1));
%above we are changing the minutes into seconds so they all agree.
windspeed=((1609.34/3600)*weatherpaterns(:,4));
%changing mph to m/s
