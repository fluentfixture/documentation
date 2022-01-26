# Date Stream

{% hint style="info" %}
The following code snippets contain constructors of the internal classes. In FluentFixture, there is no way to initialize these classes directly, but these code snippets help understand the core concepts of the library. These classes can be initialized by using factory methods, [generators](../generators/).
{% endhint %}

``[`DateStream`](date-stream.md) extends the [`Stream`](stream.md) class for date operations.

* ``[`addMilliseconds()`](date-stream.md#addmilliseconds-value)``
* ``[`subtractMilliseconds()`](date-stream.md#subtractmilliseconds-value)``
* ``[`setMilliseconds()`](date-stream.md#setmilliseconds-value)``
* ``[`getMilliseconds()`](date-stream.md#getmilliseconds)``
* ``[`addSeconds()`](date-stream.md#addseconds-value)``
* ``[`subtractSeconds()`](date-stream.md#subtractseconds-value)``
* ``[`setSeconds()`](date-stream.md#setseconds-value)``
* ``[`getSeconds()`](date-stream.md#getseconds)``
* ``[`addMinutes()`](date-stream.md#addminutes-value)``
* ``[`subtractMinutes()`](date-stream.md#subtractminutes-value)``
* ``[`setMinutes()`](date-stream.md#setminutes-value)``
* ``[`getMinutes()`](date-stream.md#getminutes)``
* ``[`addHours()`](date-stream.md#addhours-value)``
* ``[`subtractHours()`](date-stream.md#subtracthours-value)``
* ``[`setHours()`](date-stream.md#sethours-value)``
* ``[`getHours()`](date-stream.md#gethours)``
* ``[`addDays()`](date-stream.md#adddays-value)``
* ``[`subtractDays()`](date-stream.md#subtractdays-value)``
* ``[`setDaysOfWeek()`](date-stream.md#setdaysofweek-value)``
* ``[`setDaysOfMonth()`](date-stream.md#setdaysofmonth-value)``
* ``[`getDaysOfWeek()`](date-stream.md#getdaysofweek)``
* ``[`getDaysOfMonth()`](date-stream.md#getdaysofmonth)``
* ``[`addMonths()`](date-stream.md#addmonths-value)``
* ``[`subtractMonths()`](date-stream.md#subtractmonths-value)``
* ``[`setMonths()`](date-stream.md#setmonths-value)``
* ``[`getMonths()`](date-stream.md#getmonths)``
* ``[`addYears()`](date-stream.md#addyears-value)``
* ``[`subtractYears()`](date-stream.md#subtractyears-value)``
* ``[`setYears()`](date-stream.md#setyears-value)``
* ``[`getYears()`](date-stream.md#getyears)``

## addMilliseconds (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the add-milliseconds operator.

| Name    | Description                                |
| ------- | ------------------------------------------ |
| `value` | The count of the milliseconds to be added. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .addMilliseconds(10);
    
console.log(stream.single());
// prints the current date plus 10 millisecons
```

## subtractMilliseconds (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the subtract-milliseconds operator.

| Name    | Description                                     |
| ------- | ----------------------------------------------- |
| `value` | The count of the milliseconds to be subtracted. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .subtractMilliseconds(10);
    
console.log(stream.single());
// prints the current date minus 10 milliseconds
```

## setMilliseconds (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the set-milliseconds operator.

| Name    | Description                              |
| ------- | ---------------------------------------- |
| `value` | The value of the milliseconds to be set. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .setMilliseconds(10);
    
console.log(stream.single());
// prints the current date with the milliseconds as 10
```

## getMilliseconds ()

Creates a [`NumberSteam`](number-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the get-milliseconds operator.

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .getMilliseconds();
    
console.log(stream.single());
// prints the milliseconds of the current date
```

## addSeconds (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the add-seconds operator.

| Name    | Description                           |
| ------- | ------------------------------------- |
| `value` | The count of the seconds to be added. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .addSeconds(10);
    
console.log(stream.single());
// prints the current date plus 10 seconds
```

## subtractSeconds (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the subtract-seconds operator.

| Name    | Description                                |
| ------- | ------------------------------------------ |
| `value` | The count of the seconds to be subtracted. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .subtractSeconds(10);
    
console.log(stream.single());
// prints the current date minus 10 seconds
```

## setSeconds (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the set-seconds operator.

| Name    | Description                         |
| ------- | ----------------------------------- |
| `value` | The value of the seconds to be set. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .setSeconds(10);
    
console.log(stream.single());
// prints the current date with the seconds as 10
```

## getSeconds ()

Creates a [`NumberSteam`](number-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the get-seconds operator.

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .getSeconds();
    
console.log(stream.single());
// prints the seconds of the current date
```

## addMinutes (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the add-minutes operator.

| Name    | Description                           |
| ------- | ------------------------------------- |
| `value` | The count of the minutes to be added. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .addMinutes(10);
    
console.log(stream.single());
// prints the current date plus 10 minutes
```

## subtractMinutes (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the subtract-minutes operator.

| Name    | Description                                |
| ------- | ------------------------------------------ |
| `value` | The count of the minutes to be subtracted. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .subtractMinutes(10);
    
console.log(stream.single());
// prints the current date minus 10 minutes
```

## setMinutes (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the set-minutes operator.

| Name    | Description                         |
| ------- | ----------------------------------- |
| `value` | The value of the minutes to be set. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .setMinutes(10);
    
console.log(stream.single());
// prints the current date with the minutes as 10
```

## getMinutes ()

Creates a [`NumberSteam`](number-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the get-minutes operator.

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .getMinutes();
    
console.log(stream.single());
// prints the minutes of the current date
```

## addHours (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the add-hours operator.

| Name    | Description                         |
| ------- | ----------------------------------- |
| `value` | The count of the hours to be added. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .addHours(10);
    
console.log(stream.single());
// prints the current date plus 10 hours
```

## subtractHours (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the subtract-hours operator.

| Name    | Description                              |
| ------- | ---------------------------------------- |
| `value` | The count of the hours to be subtracted. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .subtractHours(10);
    
console.log(stream.single());
// prints the current date minus 10 hours
```

## setHours (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the set-hours operator.

| Name    | Description                       |
| ------- | --------------------------------- |
| `value` | The value of the hours to be set. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .setHours(10);
    
console.log(stream.single());
// prints the current date with the hours as 10
```

## getHours ()

Creates a [`NumberSteam`](number-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the get-hours operator.

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .getHours();
    
console.log(stream.single());
// prints the hours of the current date
```

## addDays (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the add-days operator.

| Name    | Description                        |
| ------- | ---------------------------------- |
| `value` | The count of the days to be added. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .addDays(10);
    
console.log(stream.single());
// prints the current date plus 10 days
```

## subtractDays (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the subtract-days operator.

| Name    | Description                             |
| ------- | --------------------------------------- |
| `value` | The count of the days to be subtracted. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .subtractDays(10);
    
console.log(stream.single());
// prints the current date minus 10 days
```

## setDaysOfWeek (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the set-days-of-week operator.

| Name    | Description                              |
| ------- | ---------------------------------------- |
| `value` | The value of the days of week to be set. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .setDaysOfWeek(5);
    
console.log(stream.single());
// prints the current date with the days of week as 5
```

## setDaysOfMonth (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the set-days-of-month operator.

| Name    | Description                               |
| ------- | ----------------------------------------- |
| `value` | The value of the days of month to be set. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .setDaysOfMonth(5);
    
console.log(stream.single());
// prints the current date with the days of month as 5
```

## getDaysOfWeek ()

Creates a [`NumberSteam`](number-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the get-days-of-week operator.

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .getDaysOfWeek();
    
console.log(stream.single());
// prints the days of week of the current date
```

## getDaysOfMonth ()

Creates a [`NumberSteam`](number-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the get-days-of-month operator.

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .getDaysOfMonth();
    
console.log(stream.single());
// prints the days of month of the current date
```

## addMonths (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the add-months operator.

| Name    | Description                          |
| ------- | ------------------------------------ |
| `value` | The count of the months to be added. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .addMonths(10);
    
console.log(stream.single());
// prints the current date plus 10 months
```

## subtractMonths (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the subtract-months operator.

| Name    | Description                               |
| ------- | ----------------------------------------- |
| `value` | The count of the months to be subtracted. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .subtractMonths(10);
    
console.log(stream.single());
// prints the current date minus 10 months
```

## setMonths (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the set-months operator.

| Name    | Description                        |
| ------- | ---------------------------------- |
| `value` | The value of the months to be set. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .setMonths(10);
    
console.log(stream.single());
// prints the current date with the months as 10
```

## getMonths ()

Creates a [`NumberSteam`](number-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the get-months operator.

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .getMonths();
    
console.log(stream.single());
// prints the months of the current date
```

## addYears (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the add-years operator.

| Name    | Description                         |
| ------- | ----------------------------------- |
| `value` | The count of the years to be added. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .addYears(10);
    
console.log(stream.single());
// prints the current date plus 10 years
```

## subtractYears (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the subtract-years operator.

| Name    | Description                              |
| ------- | ---------------------------------------- |
| `value` | The count of the years to be subtracted. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .subtractYears(10);
    
console.log(stream.single());
// prints the current date minus 10 years
```

## setYears (value)

Creates a [`DateStream`](date-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the set-years operator.

| Name    | Description                       |
| ------- | --------------------------------- |
| `value` | The value of the years to be set. |

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .setYears(2021);
    
console.log(stream.single());
// prints the current date with the years as 2021
```

## getYears ()

Creates a [`NumberSteam`](number-stream.md) with a [`Functional`](../factories/decorators/functional.md) decorator and the get-years operator.

```typescript
const stream = new DateStream(new ValueAdapter(new Date()))
    .getYears();
    
console.log(stream.single());
// prints the years of the current date
```
