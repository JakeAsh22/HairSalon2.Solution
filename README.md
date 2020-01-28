# Eau Claire's Salon

#### _C#, .NET: Eau Claire's Salon, Jake Ash, 1/17/2020_

## Description
Create a MVC application with a database to allow users to input names of stylists and clients, and be able to track which stylists have which clients.

## Application should have:
- Interact with user and create new customers, and the stylists they have.
- Separate frontend and backend logic.

## Unit Testing
| User input | Expected output |
| :------------- | :------------- |
| Stylist: Hannah.  Clients: Steve, Bob, Claire | Hannah - Steve, Bob, Claire |
| Stylists: Hannah, Claire, Matt, Wei | Hannah - Claire - Matt - Wei  |
| Add new Stylist: Will | Stylists: Hannah - Claire - Matt - Wei - Will |
| Client: Jake - adding to stylist Will | Will - Jake |

## Setup/Installation Requirements

1. Clone this repo:
```
https://github.com/JakeAsh22/HairSalon
```

2. Build the database:
```
CREATE DATABASE jake_ash;
USE jake_ash;
CREATE TABLE `clients` (
  `ClientId` int(11) NOT NULL AUTO_INCREMENT,
  `Description` varchar(255) DEFAULT NULL,
  `StylistId` int(11) DEFAULT '0',
  PRIMARY KEY (`ClientId`)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;
CREATE TABLE `stylists` (
  `StylistId` int(11) NOT NULL AUTO_INCREMENT,
  `Name` varchar(255) DEFAULT NULL,
  `ClientId` int(11) DEFAULT '0',
  PRIMARY KEY (`StylistId`)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

```

3. Go into the repo and run this application: 
```
$ dotnet build
$ dotnet run
```

## Known Bugs
* No known bugs at this time.

## Support and contact details
 jacob.ash1998@gmail.com

## Technologies Used
_Git, GitHub, MySQL, C# and .NET Core_


## License
Copyright © 2020 under the MIT License
