# hojaDeCalculoAppScrip
Ejemplo de código en una hoja de calculo
------------------------------------
  /**
 * Calculates the sale price of a value at a given discount.
 * The sale price is formatted as US dollars.
 *
 * @param {number} input The value to discount.
 * @param {number} discount The discount to apply, such as .5 or 50%.
 * @return The sale price formatted as USD.
 * @customfunction
 */
function salePrice(input, discount) {
  let price = input - (input * discount);
  let dollarUS = Intl.NumberFormat("en-US", {
  style: "currency",
    currency: "USD",
});
  return dollarUS.format(price);
}
------------------------------------
En tu hoja de cálculo
En una celda, ingresa =salePrice(100,.2). 
El primer parámetro representa el precio original y el segundo, el porcentaje de descuento. 
Si estás en una ubicación que usa comas decimales, es posible que debas ingresar =salePrice(100;0,2) en su lugar.

------------------------------------
La fórmula que ingreses en la celda ejecutará la función en la secuencia de comandos que creaste en la sección anterior. La función da como resultado un precio de oferta de $80.00.

