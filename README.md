# buybackboss-interfacer
Makes the BuyBackBoss API actually useable

# explanation
(BuyBackBoss)[https://buybackboss.com/] lets you sell phones, etc. to them and they have this really redundant process for choosing how to sell your phone
with no publicly listed API. Let's fix that and make this hopefully as simple as possible.

# todo
- COULD make an npm package
- function that contacts the API to get a specific price given a specific range of data. This is relevant trust me.

# breakdown
(click here)[https://docs.google.com/document/d/1JWG1Xoxt-MvKC1-F8d_P5PS7rEmonS5iTjEeu6E58Xw/edit?usp=sharing]
- for the sake of the document I am using a set of example data and response to explain this
1. send a POST request to the API, with the payload of the specific data about the phone
   - note to self: breakdown the naming scheme
2. recieve a response from the API
3. filter data based on whether the phone is **faulty, fair, average, good, flawless, brand new**.
   - notice the highlighted values, for some reason the fair price doesn't show up?
   - filter the data in the highlighted version to the tailored condition of a given phone
5. return a dollar value
