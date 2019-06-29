# mui-autocomplete

Simple auto suggestion for REST API requests by using Material-UI components, React hooks and Axios.

## Getting Started

npm install --save mui-autocomplete

### Dependencies

Material UI, React and Axios are needed to use this package.


### Basic Usage

We assume that you have above three dependencies before using this package. After installation you can import this package into your react component Like this:-

```
import React from 'react';
import MuiAutocomplete from 'mui-autocomplete';

function Home () {
    return (
      <div>
        <MuiAutocomplete
          placeholder="Countries"
          name="countries"
          url="https://toecoder.com/mui-autocomplete/data.php?country="
          variant="standard"
          />
      </div>
    );
}

```
### Server Side
Your backend file must return JSON data.
Example:-
* PHP (https://github.com/samrandhawa4/countries/blob/master/countries.php)
```
// onSuccess
echo json_encode(array('status'=> 200, 'posts'=> $posts));

// onError
echo json_encode(array('status'=> 400, 'message'=> 'No record found.'));

```

* Laravel (https://github.com/samrandhawa4/countries/blob/master/countriesController.php)
```
// onSuccess
return response()->json([
    'posts' => $posts,
    'status' => 200
], 200);

// onError
return response()->json([
    'error' => 'No Record Found',
    'status' => 422
], 200);

```
## Built With

* [React](https://reactjs.org/docs/hooks-intro.html) - React Hooks
* [Material-UI](https://material-ui.com) - Material-UI
* [Axios](https://github.com/axios/axios) - Used to handle API calls

## Author

* **H S Randhawa(Summer)**

## License

### LICENSE

The project is licensed under the terms of [MIT license]
