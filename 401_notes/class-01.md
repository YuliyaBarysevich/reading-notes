# Map, Reduce, Superagent, Promises & Callbacks


1. Describe (in plain English) what Array.map() does
    - **Map()** method is similar to `for loop`, it iterates over an array and calls provided function for each element. After iteration is ended it returns a new array. Given array stays the same.

2. Describe (in plain English) what Array.reduce() does
    - The **reduce()** method is used to apply a provided function to each element in the array to reduce the array to a single value. For example, it can be used to calculate a sum of all elements in the array.

3. Provide code snippets showing how to use superagent() to fetch data from a URL and log the result

```javascript 

// normal Promise .then() syntax

superagent.get('https://api.weatherbit.io/v2.0/forecast/daily?city=CITY_NAME&key=API_KEY')
    .then(weatherData => {
      // const weatherObject = weatherData.body.data;
      console.log(weatherData.body.data)
    })
    .catch(error =>{
      console.log(error);
      res.status(500).send(`Sorry something went wrong`);
    })

``` 

```javascript 

// async / await syntax

async function getWeather(city){
  let data = await superagent.get(`https://api.weatherbit.io/v2.0/forecast/daily?city=${city}&key=${API_KEY}`);
  console.log(weatherData.body.data)
}

``` 

4. Explain promises as though you were mentoring a Code 301 level student
    - Promise object is data returned by asynchronous function. It can be a resolve if the function returned successfully or a reject if function returned an error.
    - Promises allow to concentrate on what each step of a process should do, rather than worrying about in what order these steps should be called.

5. Are all callback functions considered to be Asynchronous? Why or Why Not?
    - Callbacks can be synchronous or asynchronous.
    - When we use callback functions in array methods (such as array.map(), array.for Each), these callbacks are not Asynchronous. 
    - For a function to be Asynchronous it needs to perform an asynchronous operation.(usually when they rely on an API)