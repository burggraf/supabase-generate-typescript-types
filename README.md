# supabase-generate-typescript-types
Generate typescript types for your Supabase project

## Step 0: npm install
Run `npm install`

## Step 1: modify the `config.json` file
Change the following tokens in the [`config.json`](./config.json) file:

- `DATABASE_DOMAIN_HERE`
  - go to your Supabase project dashboard at https://app.supabase.io
  - go to Settings / Database / scroll down to Host
  - copy the Host name and paste it over `DATABASE_DOMAIN_HERE`
  - example Host name:  `db.xyzxyzxyzxyzxyzxyzxy.supabase.co`
- `DATABASE_PASSWORD_HERE`
  - this is the password you entered when you created your project
  
 ## Step 2: (OPTIONAL) edit the `template.handlebars` file
 If you'd like to customize the output, the [`template.handlebars`](./template.handlebars) file is just a standard [Handlebars](https://handlebarsjs.com/) template that you can modify.
 
 ## Step 3: Generate your models
 From the command line run:
 [`./generateModels.sh`](./generateModels.sh)

NOTE:  this script simply runs the following command line: `npx @rmp135/sql-ts -c ./config.json`
 
 ## Step 4: Use your generated types
 The output file `Database.ts` can be copied to your project and imported into your Typescript project.  Optionally, you can edit the `folder` entry in your [`config.json`](./config.json) file to have the file automatically generated in a specific folder of your project.
 
