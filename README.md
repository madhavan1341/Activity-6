# Activity-6

1.Movie 

class Movie {
  constructor(title, studio, rating = "PG") {
    this.title = title;
    this.studio = studio;
    this.rating = rating;
  }

  static getPG(movies) {
    return movies.filter(movie => movie.rating === "PG");
  }
}
const casinoRoyale = new Movie("Casino Royale", "Eon Productions", "PG-13");
const movies = [
  casinoRoyale,
  new Movie("Iron Man", "Marvel Studios", "PG-13"),
  new Movie("Hulk", "Marvel Studios", "PG"),
  new Movie("Captain America", "Marvel Studios", "PG"),
  new Movie("Marvels", "Marvel Studios", "PG"),
  new Movie("Guardians", "Marvel Studios", "PG")
];

const pgMovies = Movie.getPG(movies);
console.log(pgMovies);

2.Class Person

class Person {
  constructor(Name, age, address, phoneNumber, email) {
    this.firstName = firstName;
    this.age = age;
    this.address = address;
    this.phoneNumber = phoneNumber;
    this.email = email;
  }

  getName() {
    return this.Name;
  }

  getAge() {
    return this.age;
  }

  getAddress() {
    return this.address;
  }

  getPhoneNumber() {
    return this.phoneNumber;
  }

  getEmail() {
    return this.email;
  }
}

const person = new Person("Madhavakumaran", 23, 'pondy', '123456789', 'mad@gmail.com');

console.log(person.getName());
console.log(person.getAge());
console.log(person.getAddress());
console.log(person.getPhoneNumber());
console.log(person.getEmail());

3.uber price

class UberPriceCalculator {
  constructor(baseFare, costPerKm, costPerMinute) {
    this.baseFare = baseFare;
    this.costPerKm = costPerKm;
    this.costPerMinute = costPerMinute;
  }

  calculatePrice(distance, duration) {
    const fare = this.baseFare + (this.costPerKm * distance) + (this.costPerMinute * duration);
    return fare;
  }
}

const calculator = new UberPriceCalculator(200, 1.5, 0.25);
const distance = 5; // in kilometers
const duration = 15; // in minutes
const fare = calculator.calculatePrice(distance, duration);
console.log(`The uber price is: Rs.${fare}`);
