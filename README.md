According to the American Society for the Prevention of Cruelty to Animals (“ASPCA”), approximately 6.3 mn companion animals (“pets”, dogs and cats) enter a pet shelter anually as of 2019; of which, 920,000 were euthanized in 2019<sup>[1]</sup>. However, there are an estimated 70 mn strays on US streets at any given time<sup>[2]</sup>. There are 3,500 municipal, publicly-funded, shelters, and a total of 10,500 “animal rescue organizations” and privately- and mixed-funded shelters in the United States<sup>[2]</sup>. In total, it is claimed that taxpayers directly fund animal shelters about $1-2 bn/year (at most 0.01% USA 2020 GDP, 0.03% USA FY2020 Budget)<sup>[2]</sup>. **The purpose of this website is to be a central platform for pet adoptions that assists pet shelters with pet adoptions through**:
- Developing a website that allows pet adoption centers to list pets available for adoption so that they do not need to spend money a Software Engineer to setup their website. This allows pet adoption centers to focus on their mission of keeping their pets alive and maybe even increase their budget to take in more pets. Furthermore, a central platform allows pet adopters to quickly look through many pet adoption centers at once rather than visit each site independently and increases the chance a prospective pet owner will choose to adopt a pet.
- Developing a database system that allows pet adoption centers to list pets available for applicable reasons above.
- Developing an API to efficiently connect the website and database system.
- User Sign-Up and Log-In features to authenticate pet adoption centers and prospective pet adopters (***to assist pet adoption centers find prospective pet adopters so that pet adoption centers can also search pet adopters?***).
- **Future Ideas**: Chat Feature to allow pet adoption centers and prospective adopters to ask questions (WSS Connection?). Even better is a video chat feature so that prospective adopters may see the pet before visiting. **There are more ideas that are difficult to timely implement within 2 weeks time, even this course for that matter and purposefully left out**.

## Target Demographics
The current types of users that will be supported and considered are:
- **Pet Rescue Groups / Pet Adoption Centers**: To list pets available for adoption.
- **Prospective Pet Adopters**: To find a pet that is in the database and potentially to be searched by Pet Rescue Groups for outreach.

The current regional location targeted is:
- **San Francisco Bay Area**: eventually probably expand outwards to cover the United States.

## Data Usage
For the scope of this project, I intend only to input a limited amount of data; seed the database with a sample list of pets for adoption. It depends whether or not the web application will be ready for use.

## Project Creation Outline
1. **Database Schema**
  - See the following three files in the same directory:
    - **Paste the contents of this in [https://app.quickdatabasediagrams.com/#/](https://app.quickdatabasediagrams.com/#/)**: `24.09.01_-_01.database_schema_src.md`
    - **Database Schema, Image**: `24.09.01_-_01.database_schema_img.png`
    - **Database Schema, Documentation**: `24.09.01_-_01.database_schema_documentation.pdf`
  - Questions:
    - **On the use of "UUID"**: Is it suggested to use UUID as a way to index information (see "Pets" model, "internal_uuid" attribute)?
    - **Implementing Address Validation**: I am thinking of using [USPS's (**U**nited **S**tates **P**ostal **S**ervice) Address Validation API](https://www.usps.com/business/web-tools-apis/address-information-api.htm#_Toc39492052). This way I skip the relations related to location for the user.
2. **Possible API Issues**
  - Not sure.
3. **Sensitive Information to Secure**
  - Login Credentials
  - Pet Shelter: Account Registration Information
  - Pet Adopter: Profile Information
  - Chat Logs
4. **API Functionality**
  - Mostly just retrieve search results.
  - Chat: Consider retrieving chat logs for persistence.
  - Forums?: To improve site usefulness (i.e. tips on pet care, etc.)
5. **User Flow**
  - Public: Register > Search > View Pets > Share
  - Pet Shelter: Register / Sign-In > Add Pet Listings > Modify/Manage Pet Listings > Close Account?; Search Pet Adopters > Contact (Pet Adopters)
  - Pet Adopter: Register / Sign-In > Search Pet Listings > Contact (Pet Shelters)
6. **Goals in addition to basic CRUD Features**
  - Nice UI. Initially, I only intend Craigslist-like UI
  - Flask File. Allow pet shelters to upload a CSV to be parsed into the database. (Sanitize text to prevent injection).
  - Basic Chat Feature

## Sources
[1] Unknown. *Pet Statistics*. **American Society for the Prevention of Cruelty to Animals**. https://www.aspca.org/helping-people-pets/shelter-intake-and-surrender/pet-statistics (retrieved 2022-06-29)

[2] Cvetkovska, L. *44 Shocking Animal Shelter Statistics (2022 Update)*. **petpedia.co**.
https://petpedia.co/animal-shelter-statistics/#14,000%20shelters%20and%20rescue%20groups (updated 2022-02-18, retrieved 2022-06-29)
