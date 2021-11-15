>> ### Opgave 4 - Ultrasone 2-pin mode
>>
>> Sluit de ultrasoon afstandsdetector aan, in 2-pin mode. **[SCHOOL]**
>>
>> ```java
>> public static void main(String[] args) {
>>    BoeBot.setMode(11, PinMode.Input);
>>    BoeBot.setMode(10, PinMode.Output);
>>
>>    System.out.println("Starting....");
>>    while (true) {
>>			BoeBot.digitalWrite(10, true);
>>			BoeBot.wait(1);
>>          BoeBot.digitalWrite(10, false);
>>          int pulse = BoeBot.pulseIn(11, true, 10000);
>>          System.out.println("Pulse: " + pulse);
>>          BoeBot.wait(50);
>>    }
>>}
>> ``` 
>>
>> - **A** Neem het bovenstaande progrmma over, om de lengte van de puls te meten en weer te geven
>> - **B** Sluit een oscilloscoop aan op de signaalpinnen van de detector. Laat een aantal verschillende afbeeldingen van het signaal zien, met verschillende afstanden
>>		- Klopt de gemeten tijd met de tijd van de applicatie?
>>		- Wat is de tijd tussen de uitgezonden puls van de BoeBot en het ontvangen signaal?

>>
>{: .exercise}