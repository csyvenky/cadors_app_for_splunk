# CADORS App for Splunk
A Splunk app to process Transport Canada Aviation Safety Data

# Install app on Splunk Enterprise (standalone)
1.

# Add the CADORS Data
1.

# Access the main Dashboard
1.

# Data Download and Cleanse Workflow
To use this app, the raw data file from Transport Canada needs to be downloaded.

# Credit for External Lookup Data
The airport details data has been downloaded from **OurAirports.com**. More information on the project and the Public Domain license can be found [here](http://ourairports.com/data/).

# Build details (for OS X)
1. Clone github repo `git clone https://github.com/csyvenky/cadors_app_for_splunk.git`.
2. Make your enhancements and increase the Build and Version numbers in the ./default/app.conf file.
3. Make a tarball of the app folder `tar --exclude='cadors_app_for_splunk/.git' -czvf cadors_app_for_splunk.tar.gz cadors_app_for_splunk/`  .
4. Run AppInspect validation via Postman `http://dev.splunk.com/view/appinspect/SP-CAAAFDU`.
5. Test the app installation on clean instance of Splunk.
