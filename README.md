## Get Started

1. Configure backend site setting in Business Manager:

    (1) Go to  Administration > Site Development > Import & Export, upload file `metadata/bolt-meta-import/meta/system-objecttype-extensions.xml` and import it.

    (2) Go to Merchant Tools > Ordering > Payment Processors, create a new Processor with ID `BOLT_PAY`.

    (3) Go to  Merchant Tools > Ordering > Import & Export, upload file `metadata/bolt-meta-import/sites/RefArch/payment-methods.xml` and import it.

    (4) Go to Merchant Tools > Site Preferences > Custom Site Preference Groups, Click into group <Bolt Payment Setting - Managed Checkout> and add/update the bolt related configurations.

2. Configure OCAPI:

    (1) Navigate to Administration > Site Development > Open Commerce API Settings.
    
    (2) Navigate to `metadata/ocapi` folder.
    
    (3) Copy the contents of `OCAPIshop.json` within Shop Type > Open Commerce API Settings.
    
    (4) Replace `<<client_id>>` with your client_id.
    
    (5) Click `Save`.
    
    (6) Copy the content of `OCAPIdata.json` within Data Type > Open Commerce API Settings.
    
    (7) Select "Global (organization-wide)" from the Context Selection dropdown.
    
    (8) Replace `<<client_id>>` with your client_id.
    
    (9) Click `Save`.

3. Add SFRA cartridge to your code base:

    (1) Add cartridge `cartridges/int_bolt_pwa` to your project and upload it to the SFCC instance. 
    
    (2) In SFCC Business Manager, Go to Administration > Sites > Manage Sites, select the site, click on `Setting` Tab, add `int_bolt_pwa` at the beginning of the site path field with separator `:`.