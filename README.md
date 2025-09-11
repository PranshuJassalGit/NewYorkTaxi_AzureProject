# NewYorkTaxi_AzureProject

Creating a Resource Group
<img width="1918" height="876" alt="image" src="https://github.com/user-attachments/assets/ab2c4567-2c8c-4c5f-9a55-74ce0a285387" />

Resource Group
<img width="1919" height="818" alt="image" src="https://github.com/user-attachments/assets/d3bea357-16aa-46a2-9448-b054d2c2175c" />

Creating a storage account 
<img width="1898" height="741" alt="image" src="https://github.com/user-attachments/assets/dc388ce6-9a3d-4e4f-a348-d91d1a83c77f" />

Enabling hirarchial namespace to convert from blob storage to Data lake
<img width="1033" height="166" alt="image" src="https://github.com/user-attachments/assets/5e6f0936-7c4a-4650-bcf8-786cb647de31" />

Sucessfully created data-lake
<img width="1070" height="484" alt="image" src="https://github.com/user-attachments/assets/dea7b2df-6b80-436d-8d5e-f82a3d1d5564" />

Creating bronze, silver and gold containers
<img width="1919" height="828" alt="image" src="https://github.com/user-attachments/assets/2723d220-b990-493a-9e50-66e8c9ad965d" />

Adding directories
<img width="1919" height="736" alt="image" src="https://github.com/user-attachments/assets/98593c5a-2cf8-45fd-a8b0-90ba97fdf1ff" />

Creating another resoruce adf 
<img width="1919" height="821" alt="image" src="https://github.com/user-attachments/assets/a2acdcb9-dc21-499e-9573-728679bbdf00" />

Creating a linked service bcs i will be making https request from the website to store data into my bronze layer
<img width="1919" height="823" alt="image" src="https://github.com/user-attachments/assets/7afb797f-1495-431c-bae3-9dab6a954313" />

Create a http connection using the base url of the nyc-taxi data
<img width="811" height="816" alt="image" src="https://github.com/user-attachments/assets/19b80166-7dac-48cc-9849-28aa083f71e7" />

Lets create one more linked service for destination which is gen 2
<img width="1919" height="871" alt="image" src="https://github.com/user-attachments/assets/0be19edc-0304-4bea-a1e9-81eb48f74d1e" />

Creating pipeline for data from source i.e nyc taxi data web to sync i.e datalake
<img width="1919" height="800" alt="image" src="https://github.com/user-attachments/assets/fdd3efce-82dd-4c14-a009-61681ae7e0ea" />

Creating a copy activity 
<img width="897" height="699" alt="image" src="https://github.com/user-attachments/assets/c9da03d0-a7d7-485c-bb84-d80196ad0120" />

Setting up the source by selecting https first and the selecting the file format followed by relative URL
trip-data/green_tripdata_2024-01.parquet

<img width="1918" height="821" alt="image" src="https://github.com/user-attachments/assets/58d20c99-93c6-4373-b601-1f215c3fdf98" />
<img width="1919" height="867" alt="image" src="https://github.com/user-attachments/assets/254842f5-ab66-4077-806d-5c3e66ffed61" />

Now create for sink


<img width="1917" height="863" alt="image" src="https://github.com/user-attachments/assets/5cf8ae9d-a095-44fb-9318-76708aae0d30" />

Now pipeline is complete, just debug . till here we are only testing the static piplines we have not used varialbles yet, this one is just fir testing

<img width="1848" height="748" alt="image" src="https://github.com/user-attachments/assets/f4f0e894-64d2-4410-8161-c65a3882785f" />

and here we Goooooooooooooooooo............


<img width="1902" height="608" alt="image" src="https://github.com/user-attachments/assets/477334c9-1079-46cc-a9bc-1ba7a98e452b" />

Now lets make for each activity bcs we have just fetched jan data now i want to parameterized the 01- of the file name so that i can just set the 01 part as variable and iterate

Creating parameters
<img width="963" height="359" alt="image" src="https://github.com/user-attachments/assets/2675bb21-2b08-474d-ae79-4fa889e3ec0c" />

Creating expression
<img width="906" height="859" alt="image" src="https://github.com/user-attachments/assets/ca846d7e-3f70-4d1c-bd11-4bafe17927ee" />

Creating a For Each activity
<img width="1919" height="776" alt="image" src="https://github.com/user-attachments/assets/2154dd22-fdc4-43d4-b425-f22c19d832a3" />

Set sequencial and add the range for the loop
<img width="1913" height="823" alt="image" src="https://github.com/user-attachments/assets/d43c5677-9d83-4067-b51d-1223ff597762" />

Paste the copy activity inside the for each activity
<img width="1919" height="791" alt="image" src="https://github.com/user-attachments/assets/1a99d856-a688-4b39-83ac-a6f156974346" />

Connect and set the output of the for each to the source of the copy activity
<img width="1919" height="875" alt="image" src="https://github.com/user-attachments/assets/5df3ee79-495a-4aeb-b624-99f74b376b48" />

Here we go.....
<img width="1919" height="822" alt="image" src="https://github.com/user-attachments/assets/4ebd5df6-601a-44b1-bf33-e7d9e7469ef8" />

Let's make the service principle that will act as intermidiate between databricks and azure gen

Go to microsoft entra ID
<img width="1894" height="691" alt="image" src="https://github.com/user-attachments/assets/688df175-221b-4105-98c2-530fb12373ab" />

Make a new app registeration, we are doing this to connect our databricks
<img width="1593" height="814" alt="image" src="https://github.com/user-attachments/assets/e58f9b70-bd14-40a8-b1af-740d1c8ecd19" />

Create service principle
<img width="1832" height="756" alt="image" src="https://github.com/user-attachments/assets/62e4bcff-f358-48ab-a535-e6580ceafc88" />

add permission, storage blob containers
<img width="1919" height="862" alt="image" src="https://github.com/user-attachments/assets/941efd0b-2243-4a51-9c17-db72c261dbe7" />

Select pranshu service principle
<img width="1903" height="860" alt="image" src="https://github.com/user-attachments/assets/98018241-9668-4162-9f3d-b7a585b7d4d1" />

Setting up databricks workspace
<img width="1149" height="864" alt="image" src="https://github.com/user-attachments/assets/fa22b987-a4d3-405f-93ab-2d9752f5e634" />
<img width="1509" height="852" alt="image" src="https://github.com/user-attachments/assets/d24e8758-dc2e-48fe-868b-b38ae0009d7a" />

Lets create compute , for creating the cluster
<img width="1673" height="842" alt="image" src="https://github.com/user-attachments/assets/bd8e442b-4934-40a9-932f-eb307b80df16" />

Create a notebook
<img width="1912" height="855" alt="image" src="https://github.com/user-attachments/assets/cd1e0680-14f1-4ed7-a59e-216185f1c72e" />

Connecting databricks to delta lake
<img width="1668" height="810" alt="image" src="https://github.com/user-attachments/assets/74cffee4-b99b-4861-89b5-824f928c220e" />

Run the connection code
<img width="1492" height="616" alt="image" src="https://github.com/user-attachments/assets/03d4fcb3-dbae-44e9-ad88-af52d2a6359d" />

Reading the trip data using recursive loookup
<img width="1514" height="665" alt="image" src="https://github.com/user-attachments/assets/8b5275f6-5418-4b2d-8d9f-7ececb8f8bfb" />

Transforming trip type data and loading it to silver layer
<img width="1402" height="408" alt="image" src="https://github.com/user-attachments/assets/bb36fbce-3d65-467e-b2d7-639df4142119" />

Loading 
<img width="1481" height="254" alt="image" src="https://github.com/user-attachments/assets/332747e5-692f-4166-a5fc-06c421fb44d8" />

Creating a silver Notebook and making connection 
<img width="1490" height="454" alt="image" src="https://github.com/user-attachments/assets/61bcb2c7-3b28-4464-90af-c6a1f3efba82" />

Reading Trip type data from bronze layer
<img width="1544" height="702" alt="image" src="https://github.com/user-attachments/assets/c3410307-289d-46f4-854f-f2938b8df1ba" />

Reading trip zone data from bromze
<img width="1543" height="711" alt="image" src="https://github.com/user-attachments/assets/7c6ae906-bb5c-4020-9793-2e60243a0e1a" />

Creating trip type schema 
<img width="1506" height="664" alt="image" src="https://github.com/user-attachments/assets/746da7b5-65fc-4b83-bad7-4e682d68e9c9" />

Reading Trip Data
<img width="1549" height="709" alt="image" src="https://github.com/user-attachments/assets/c4426651-88c3-4849-a455-227d0191d2ad" />

Transforming Trip type data
<img width="1514" height="529" alt="image" src="https://github.com/user-attachments/assets/cfd39a3e-ddd8-4178-939d-815d38b5e883" />

Writing Trip type data on silver layer
<img width="1516" height="250" alt="image" src="https://github.com/user-attachments/assets/5206830a-d77a-4e68-9cf0-ce28df1d6d1e" />

Transforming Trip Zone
<img width="1484" height="703" alt="image" src="https://github.com/user-attachments/assets/dc053e0e-aeac-4e0e-bc89-493e10ce7822" />

Writing Trip zone to silver layer
<img width="1536" height="265" alt="image" src="https://github.com/user-attachments/assets/e8013d7a-2188-4b28-9f21-8df5f5301208" />

Transforming Trip data
<img width="1490" height="697" alt="image" src="https://github.com/user-attachments/assets/aa69d905-d1df-401f-97fb-72900079b7ac" />

Writing trip type into the silver layer
<img width="1526" height="244" alt="image" src="https://github.com/user-attachments/assets/7bef10f8-9cf7-4eaf-a411-fe7a313e57a6" />


###Creating Gold Layer

Creating connection string
<img width="1481" height="343" alt="image" src="https://github.com/user-attachments/assets/ba7a9b4d-9362-4ab3-b0e6-f14592691a5f" />

Creating a database
<img width="1458" height="420" alt="image" src="https://github.com/user-attachments/assets/386e336a-d2b7-4ab2-ad72-fb30374c8451" />

Reading from silver layer trip zone and writing to gold
<img width="1476" height="668" alt="image" src="https://github.com/user-attachments/assets/9220da45-83da-4729-8db9-2d0b3e9a4f95" />

Running Gold table
<img width="1508" height="554" alt="image" src="https://github.com/user-attachments/assets/5c974d79-37a9-4d8d-bfc0-d3bc2b95c607" />

Reading Trip type data and writing to gold
<img width="1479" height="628" alt="image" src="https://github.com/user-attachments/assets/06daade5-d40e-4bed-af3c-e0d42723df9f" />

Reading trip zone and writing to gold
<img width="1481" height="629" alt="image" src="https://github.com/user-attachments/assets/14f2332e-5e83-4678-b022-21072bc3f165" />

Reading the trip data and writing to gold
<img width="1485" height="660" alt="image" src="https://github.com/user-attachments/assets/d3933392-f6f0-4fda-a898-2df466492e35" />

Now , lets connect to Power BI
<img width="1116" height="662" alt="image" src="https://github.com/user-attachments/assets/30c5bfbe-f843-4a38-977b-10f4900b0f3f" />

CLick on connection
<img width="1919" height="868" alt="image" src="https://github.com/user-attachments/assets/c54dcff1-6d4b-4a61-9305-0b21200354ab" />

Now open the file and go to the access token 
<img width="1157" height="532" alt="image" src="https://github.com/user-attachments/assets/733a709a-2c97-4c3d-b748-0aaa5871926b" />

Now create a access token , go to profile, setting developer and access token
<img width="1558" height="789" alt="image" src="https://github.com/user-attachments/assets/9df0c267-59a1-41c1-94a9-a4e93871c867" />

Paste token to the power BI
<img width="995" height="422" alt="image" src="https://github.com/user-attachments/assets/b4e178d2-184d-4aba-91d3-50f2e4f5841e" />

Booooom here we goooooooooo,

<img width="1082" height="672" alt="image" src="https://github.com/user-attachments/assets/d41f8554-e68c-4289-9735-377b492fd290" />

Loaded
<img width="1204" height="706" alt="image" src="https://github.com/user-attachments/assets/e6005cf2-e282-45b8-a9da-b5afab3396e8" />































