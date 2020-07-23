## Client Requirements:

Without using code or anything more advanced than the WYSIWYG tools available within marketing cloud please enable dynamically populated email content based on a number of criteria.

The criteria are as follows:



*   The colour of their more recent car rental
    *   Options:
        *   Red
        *   Blue
        *   Grey
        *   Green
*   The year of their most recent car rental ranging from 2015 to 2019
*   The length of their recent rental by cluster category
    *   1 day
    *   2-7 days
    *   8-14 days
    *   Long term rentals

The client has agreed to provide the following data to support these requirements in a Data Extension:



*   Subscriber Key
*   Email Address
*   Recent Car Hire Start Date
*   Recent Car Hire Duration (Days)
*   Recent Car Hire Model
*   Recent Car Hire Colour
*   Recent Car Hire Price
*   Rental Customer Name


## Abstract

Using the native Dynamic Content block capabilities within Content Builder we would be able to provide some of the simple dynamic content requirements. There will be some limitations in terms of the complexities and some of the specifics of the requirements (for example: is the requirement to just change an image or do we need to change subject line?)

Using the scenario of: The person who receives this email previously rented a car of a specific model from our range, we should showcase an image of that same vehicle model in the email header. We should also include the vehicle model in the subject line: for example “Michael, your Fiat 500 is waiting for your next rental” and then continue with a picture of a Fiat 500 in the header image spot in the email.


## Process

As part of this scenario, we will assume that the Rental Company currently stocks the following vehicles for rental purposes:



*   Fiat 500
*   Ford Fiesta
*   Toyota Camry
*   Nissan QASHQAI

In order to complete this we will need to create an Image Content Block for each of these vehicles.

Example:

![alt_text](https://res.cloudinary.com/howtosfmc/image/upload/v1595488832/articles/WYSIWYG/Anonymous/G9pYVkxDeTsAXKBes9_ODvd9Dzp-u25KMjoIWUVGBCbsaMvJa5XKlxqtHfF3m0wTIEE7S4PFjwcwL-zkNgLcpUfvz-jrefsMVqnTtDDLVrAeUguW71d_o4uDDVlHmaEjlzm-pBmg_gqkafq.png "Vehicle Image: By EurovisionNim - Own work, CC BY-SA 4.0, https://commons.wikimedia.org/w/index.php?curid=72089491")


With each of these completed, we will then create the Dynamic Content Block.

As part of the creation of the Dynamic Content Block, we need to consider a default content to use in the situation where either data is missing or that the data does not comply with the 4 models listed above. For example, if the Rental Company previously supplied Nissan Leaf, it may be the most recent vehicle a customer has rented but it is not available now. We will make the assumption that the vehicle that the Rental Company currently has the most availability of is the Ford Fiesta and therefore we will use it as the backup image in the email placement.

We will create the rules from the Data Extension or Audience for this Dynamic Content block, like this:


![alt_text](https://res.cloudinary.com/howtosfmc/image/upload/v1595488844/articles/WYSIWYG/Anonymous/oZW-RytOGf79elxzHNumEIzbwrUUoEcrwhwz3Cluj8GzvunFQHelwi8y7DVl7Bwv2MONeQzviDgcr_O2bHGFpjEEE1PRlnPmJ8mU8ewL_lidjbu.png "Choose Data Extension or Audience")


We select the correct Data Extension (Car Rentals) and select the attribute within: Recent Car Hire Model and set the requirement to be Ford Fiesta



![alt_text](https://res.cloudinary.com/howtosfmc/image/upload/v1595488858/articles/WYSIWYG/Anonymous/p_EL1lwQg-Aa0KnEQIDz1Zrh6VsHrH8dM1jFHP1tdwZwvgb_sXK9Rh0TOF1eaUjd-R1c0IP5ZRwPWQEP8NsdtWM877uYwQaIBZN69CeY-qgBWoSiFQ7vu4rssCsD2GfjqYgRlZgb_lkigmr.png "Dynamic Content Rule")


We complete this for all models and then we add the Dynamic Content Block to an email and can preview the results:


![alt_text](https://res.cloudinary.com/howtosfmc/image/upload/v1595488872/articles/WYSIWYG/Anonymous/U291cFR_r4r-BHlLXcRNLVl7L-xkOAG5-YkWMhJQ4mZkSALMEpXGNaWAUSaM-8a0P-l4E4YGub0HgaMpD_C1-Pze_mf9IzGS2kiUk2O_UN1uvhavqqp9tQ3UGpISQkykM_0z3DjT_dbb1r3.png "Vehicle Image: By Pava, Milano ( from IT WIKI ) - Own work, CC BY-SA 3.0 it, https://commons.wikimedia.org/w/index.php?curid=41882808")




![alt_text](https://res.cloudinary.com/howtosfmc/image/upload/v1595488882/articles/WYSIWYG/Anonymous/K5RMRxWZ0gxNZBpapTWXiz61EX-6hOAGb6X3T7ZNPiNEKhsPfVHzWOB4Xj4f1rkXNLAOyZ8APnJnWtKgUIlYYMpmEAAdUxj3FiHwqoFhoDiY_6u6GwmAz0UlH8lExG-1TyQSsTx1_fhzzzd.png "Vehicle Image: By Vauxford - Own work, CC BY-SA 4.0, https://commons.wikimedia.org/w/index.php?curid=62811564")




![alt_text](https://res.cloudinary.com/howtosfmc/image/upload/v1595488910/articles/WYSIWYG/Anonymous/jew-5Q-QDCmJVYCGzQAlMTD9HKpvaDWqt6-4TPW2hV2HYmDTMwYrOcN1711NCtjbYfAh7Vu4zCoIqza1o4FBhxY1TTHEFOU8Fl_MTnMl_wzg4d0.png "Vehicle Image: By EurovisionNim - Own work, CC BY-SA 4.0, https://commons.wikimedia.org/w/index.php?curid=72089491")



![alt_text](https://res.cloudinary.com/howtosfmc/image/upload/v1595488935/articles/WYSIWYG/Anonymous/G1gnnq_dBuuZwgWwSC3omwJS5Mdds7iULDAXF-Y5KKiyStxK9-vxWfmPYSWT5wph4mO4GLdFhMkI-xkCh4xiMBClDpjicuttiD8OtaWw_wnost5.png "Vehicle Image: By Vauxford - Own work, CC BY-SA 4.0, https://commons.wikimedia.org/w/index.php?curid=75410329")



![alt_text](https://res.cloudinary.com/howtosfmc/image/upload/v1595488949/articles/WYSIWYG/Anonymous/PSm48Rfn7K2ybTCcG1Oio80TI6xG7lNbHEeHjQVuRyHFmy5YaG1p3anpBBYLbyPhfLjSk5VdpAJwRc7mYS_a0ns3O-xbFi16MKUyWm3-eiF9nccNcJtic5c80RbQZvQYXvboGTbz_x3toya.png "Vehicle Image: By Vauxford - Own work, CC BY-SA 4.0, https://commons.wikimedia.org/w/index.php?curid=62811564")


## Detailed View: 
Import valid data into the Sendable Data Extension and create Image Blocks relating to the dynamic content rules to include. Deploy a dynamic content block against that Sendable Data Extension to create a dynamic hero image, including a fallback for relevant scenarios. This will give a customer a unique experience based on what is known as well as what the business needs to achieve.

## Brief Overview:

Create a DE, populate it well & cater for when data goes wrong
