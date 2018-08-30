let store = {drivers:[], passengers:[], trips:[]};
let driId = 0;
let paseId = 0;
class Driver{
  constructor(name){
    this.id = ++driId;
    this.name = name;
    store.drivers.push(this);
  };
  trips(){
    return store.trips.filter(
      trip =>{ return trip.driverId === this.id; }
    );
  };
  passengers(){
    return store.passengers.filter(passenger => {return passenger.driverId === this.id})
  };
};
class Passenger{
  constructor(name){
    this.id= ++paseId;
    this.name = name;
    store.passengers.push(this);
  };
  trips(){
    return store.trips.filter(
      trip =>{ return trip.passengerId === this.id;}
    );
  };
  drivers(){
    return store.drivers.filter(driver => {return drivers.driverId === this.id})
  }
};
class Trips{
  constructor(driver, passenger){
    this.id = ++tripId;
    this.driverId = driver.id;
    this.passengerId = passenger.id;
    store.trips.push(this);
  };
  driver(){
    return store.drivers.filter( driver => {
      return driver.id === this.id;}
    );
  };
  passenger(){
    return store.passengers.filter(passenger => {return passenger.driverId === this.id})
  }
};
