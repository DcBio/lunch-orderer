# Exercise

Implement a daily lunch ordering application.

## Specification
Your application should expose three HTTP endpoints:

### API Definition: 

```
/daily/menu
```

### API Input:

This API does not have any input.

### API Response:

For each request executed against the API endpoint, you should return a list of meals that are available to be ordered. 

### Workflow:

When the API is being called, your code should do crawling of table data from the table below:
<table> <tbody>
  <tr>       					
      <td class="rednibroj">1</td>
      <td class="jelo">Varivo od mix mahunarki</td>
      <td class="cijena">3,60€</td>
  </tr>
  <tr>       					
      <td class="rednibroj">2</td>
      <td class="jelo">Pohani file oslića – krumpir salata s rikulom</td>
      <td class="cijena">6,30€</td>
  </tr> 
  <tr>       					
      <td class="rednibroj">3</td>
      <td class="jelo">Pohani file oslića, umak od vlasca i krastavca - slani krumpir</td>
      <td class="cijena">6,30€</td>
  </tr>
  <tr>       					
      <td class="rednibroj">4</td>
      <td class="jelo">Steak tune sa žara, tršćanski umak – blitva s krumpirom</td>
      <td class="cijena">10€</td>
  </tr>
  <tr>       					
      <td class="rednibroj">5</td>
      <td class="jelo">Orada sa žara, tršćanski umak – blitva s krumpirom</td>
      <td class="cijena">7,10€</td>
  </tr>
  <tr>       					
      <td class="rednibroj">6</td>
      <td class="jelo">Crni rižoto od liganja s parmezanom</td>
      <td class="cijena">6,50€</td>
  </tr>
  <tr>       					
      <td class="rednibroj">7</td>
      <td class="jelo">Pureći medaljoni u umaku od pesta s tjesteninom</td>
      <td class="cijena">6€</td>
  </tr>
  <tr>       					
      <td class="rednibroj">8</td>
      <td class="jelo">Juha od rajčice</td>
      <td class="cijena">1,20€</td>
  </tr>
  <tr>       					
      <td class="rednibroj">9</td>
      <td class="jelo">Salata miješana</td>
      <td class="cijena">1,10€</td>
  </tr>
</tbody></table>

Your code should then return a list of meals as the response. The value of **_rednibroj_** would be used as an identifier of the meal that the user wants to order.

### API Definition: 

```
/order
```

### API Input:

This API endpoint takes at least one meal ID as input (more are possible), e.g.:

https://lunch/order?mealIds=5

https://lunch/order?mealIds=4,8,9

### API Output:

Returns the ID of the stored order which will be the input for the third API endpoint.

### Workflow:

When this API is being called new order should be created and the identifier of the newly created order is returned.


## Additional Information
You should use following frameworks for your work.

Spring JPA
H2 database running in memory (data will not be persistent across application restarts)
You are free to add / change any libraries which you might need to solve this exercise, the only requirement is that we do not have to setup / install any external software to run this application.

Running the exercise with maven

```mvn spring-boot:run```

### Commiting
You will provide your solution by creating a feature branch using your name (i.e. feature/ivanhorvat) and pushing it to this repository.
