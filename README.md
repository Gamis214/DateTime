# DateTime
Ejemplo de uso del Datetime 

```java
public class DateFormatExample {

    public static void main(String[] args) {
        // Make a new Date object. It will be initialized to the
        // current time.
        Date now = new Date();

        // Print the result of toString()
        String dateString = now.toString();
        System.out.println(" 1. " + dateString);

        // Make a SimpleDateFormat for toString()'s output. This
        // has short (text) date, a space, short (text) month, a space,
        // 2-digit date, a space, hour (0-23), minute, second, a space,
        // short timezone, a final space, and a long year.
        SimpleDateFormat format =
            new SimpleDateFormat("EEE MMM dd HH:mm:ss zzz yyyy");

        // See if we can parse the output of Date.toString()
        try {
            Date parsed = format.parse(dateString);
            System.out.println(" 2. " + parsed.toString());
        }
        catch(ParseException pe) {
            System.out.println("ERROR: Cannot parse \"" + dateString + "\"");
        }

        // Print the result of formatting the now Date to see if the result
        // is the same as the output of toString()
        System.out.println(" 3. " + format.format(now));
    }
}
```

Al ejecutar el codigo nos da el siguiente resultado
```
1. Tue Nov 04 21:53:43 EST 2003
2. Tue Nov 04 21:53:43 EST 2003
3. Tue Nov 04 21:53:43 EST 2003
```

###Tabla de Formatos para un date:
![Image of Yaktocat](http://i.imgur.com/Ub1ts8S.png)
