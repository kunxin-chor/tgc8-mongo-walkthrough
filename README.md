
# Animal Shelter DB
1. View the details of all the animals in the shelter
2. Add in a new animal
3. Update an existing animal
4. View the details of all the vets that are taking care of the animals
5. Keep track of which vet is taking care of which animal

# Animal Document (represent one animal)
```
{
    "_id": ObjectId("1234567"),
    "name": "Fluffy",
    "species":"Dog",
    "breed":"Golden Retriever",
    "microchip":"X123457Z"
}
```

# Vet Document (represent one vet)
```
{
    "_id": ObjectId("55667788"),
    "first_name":"Mary",
    "last_name":"Sue",
    "address":"Telok Blangah Lane 14 #01-01",
    "license":"NAR12345"
}
```

# Checkup 
```
{
    "_id": ObjectId("771777"),
    "animal_id":ObjectId("1234567"),
    "vet_id": ObjectId("55667788"),
    "diagnosis":"Overweight",
    "treatment":"Go on a diet
}

```

# Checkups using embedded documents 
## Animal document
```
{
    "_id": ObjectId("1234567"),
    "name": "Fluffy",
    "species":"Dog",
    "breed":"Golden Retriever",
    "microchip":"X123457Z",
    "checkups":[
        {
            "_id":ObjectId("123454),
            "vet_id":ObjectId("55667788"),
            "vet":"Mary Sue",
            "license_number": "NAR12345".
            "diagnosis":"Overweight",
            "treatment":"Go on a diet",
            "date":"20-01-2020"
        },
        {
            "_id":ObjectId("456778"),
            "vet":"Ching han",
            "license_number":"JAR1234",
            "diagnosis":"Cancer",
            "treatment":"Operation",
            "date":"20-05-2020"
        }
    ]
}
```