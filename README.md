# Digital-electronics-2

## VUT
AVR-**repository** 10h


Some code
```C
int main(void)
{
    /* Set output pin */
    DDRB |= _BV(LED_PIN);           /* DDRB = DDRB or (0010 0000) */

    /* Turn LED off */
    PORTB &= ~_BV(LED_PIN);         /* PORTB = PORTB and (0010 0000) */

    /* Infinite loop */
    for (;;)
    {
        /* Invert LED and delay */
        PORTB ^= _BV(LED_PIN);      /* PORTB = PORTB xor (0010 0000) */
        _delay_ms(BLINK_DELAY);     /* Wait for several milisecs */
    }

    return (0);
}
```
