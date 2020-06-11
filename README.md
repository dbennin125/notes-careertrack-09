# notes-careertrack-09
### Instance Methods
<p>Instances of "Models" have built-in instance methods since they are documents. You define a schema, assign a function to the methods object, and now that instance is available to use with that schema . This only works if you DO NOT DECLARE with arrow functions.</p>

### Static 
<p>Add a function property to schema.statics. You call function by Schema#static. This only works if you  DO NOT DECLARE with arrow functions.</p>Sample code from website ('https://mongoosejs.com/docs/guide.html#methods'):<br>
<code>
  // you can call `animalSchema.static()`.
  animalSchema.static('findByBreed', function(breed) {
    return this.find({ breed });
  });<br><br>
    const Animal = mongoose.model('Animal', animalSchema);

  animals = animals.concat(await Animal.findByBreed('Poodle'));</code>

### Middleware
4 types: document middleware, model middleware, aggregate middleware, and query middleware.   
Middleware are functions used during asynchronous functions. 
