DESCRIPTION

Many people across the globe are getting sick due to food hygiene. A better tracking technique is required to trace back the origin of the food item so that the end-user can authenticate that food item and consume that without any worry.

 

Background of the problem statement:

Food quality and safety are important topics today as everyone is concerned about the quality of the food that is being consumed.

Food items like fruits and vegetables generally do not have any expiry date mentioned so it becomes really important to understand the origin of these food items and know when was it sent to the distributor from the farmer and so on. The following cycle is generally followed in the fruit supply chain:

Producer: The producer can harvest fruits and vegetables, sell them to a distributor, and track authenticity.
Distributor: The distributor can buy and distribute the fruits and track authenticity.
Retailer: The retailer can buy and put the fruits for sale and track authenticity.
Consumer: The consumer can buy the fruits and track authenticity.
Features of the application:

      1. Farm Product has the following parameters:

productId: Asset Id
productDescription: Description of the asset
producerName: Name of the producer or farmer
producerAddress: Address of the producer or farmer
harvestDate: Date of the harvest
distributerName: Name of the distributer
distributerAddress: Address of the distributer
prodToDistDate: Date of transfer from producer to distributer
retailerName: Name of the retailer
retailerAddress: Address of the retailer
distToRetaDate: Date of transfer from distributer to retailer
 

     2. Add a new farm product to the ledger

This function is used to add a new product to the ledger. This function is called by the producer or farmer by using the below parameters.

Input Parameters:

             * @param ctx         the transaction context

             * @param id          the product id of the farm product

             * @param description the description of the farm product

             * @param producerName producer or farmer name

             * @param producerAddress producer or farmer address

             * @param harvestdate harvestdate of the farm product

             * @return the Product details

             */

This function also checks if:

The same asset with the same product ID does not exist already
 

       2. Transfer the asset to the distributer from the producer

This function helps to transfer the farm product from a producer (farmer) to a distributor.

Input Parameters:

       * @param ctx      the transaction context

       * @param id     product Id of the Farm Product

       * @param distributerName distributer name

       * @param distributerAddress distributer address

       * @param transferDate transaction date between distributer and producer

       * @return the product id

       */

 

This function also does the following check:

An asset should be present in the ledger
 

       3. Transfer the asset to the retailer from the distributor

This function helps to transfer the farm product Ownership to the retailer from the distributor.

 Input Parameters:

       * @param ctx      the transaction context

       * @param id     product Id of the Farm Product

       * @param retailerName retailer name

       * @param retailerAddress retailer address

       * @param transferDate transaction date between distributer and retailer

       * @return the product id

       */

This function also does the following check:

.

An asset should be present in the ledger.
 

         4. View asset details from the ledger

This function helps to retrieve asset product details from the ledger.

       Input Parameters

       * @param ctx      the transaction context

       * @param id product Id of the farm Product

       * @return Farm Product supply chain details

             */

 

Recommended technologies:

IDE Tool: Eclipse
Chaincode Language: Java
Build Automation tool: Gradle
Blockchain: Hyperledger Fabric
Server: Test network
 

Project development guidelines:

The project will be delivered within four sprints with every sprint delivering a minimal viable product.
It is mandatory to do proper sprint planning with user stories to develop all the components of the project.
The learner can use any technology from the above-mentioned technologies for different layers of the project.
The learner has to maintain the version of the application over GitHub and every new change should be sent to the repository.
The learner should also deploy and host the application on any blockchain instance.
