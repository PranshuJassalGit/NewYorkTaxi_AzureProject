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













