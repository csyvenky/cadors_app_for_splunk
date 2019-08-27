# CADORS App for Splunk
A Splunk app to process Transport Canada Aviation Safety Data

# Install app on Splunk Enterprise (standalone)
1. Click the Settings gear icon next to **Apps** on the Launcher homepage.
2. Click **Install app from file**.
3. Navigate to **cadors_app_for_splunk.tar.gz**.
4. Click **Upload**.
5. Restart Splunk.

# Add the CADORS Data (XML)
1. Click **Add Data** on the Launcher homepage.
2. Click **Upload files from my computer**.
3. Click **Select File**.
4. Navigate to the location of the **CADORS_NATIONAL_{yyyymmdd}_E.xml** data files. You can have Transport Canada send you daily emails - simply subscribe to the CADORS reports.
5. Click **Next**.
6. For **Source type**, click **Custom**, then select **cadors_xml**.
7. Click **Next**.
8. For **Index**, click **Create a new index**, set **Index Name** to **cadors_xml**, set **Max Size of Entire Index** to **100MB**, set **App** to **CADORS App for Splunk**.
9. Click **Save**.
10. Click **Review**.
11. Click **Submit**.

# Access the main Dashboard
1. Select **Apps** | **CADORS App for Splunk**.

# Data Download and Cleanse Workflow
To use this app, the raw data file from Transport Canada needs to be downloaded.

# Credit for External Lookup Data
The airport details data has been downloaded from **OurAirports.com**. More information on the project and the Public Domain license can be found [here](http://ourairports.com/data/).

# Build details (for OS X)
1. Clone github repo `git clone https://github.com/csyvenky/cadors_app_for_splunk.git`.
2. Make your enhancements and increase the Build and Version numbers in the ./default/app.conf file.
3. Make a tarball of the app folder `tar --exclude='cadors_app_for_splunk/.git*' --exclude='cadors_app_for_splunk/.DS_Store' -czvf cadors_app_for_splunk.tar.gz cadors_app_for_splunk/`  .
4. Run AppInspect validation via Postman `http://dev.splunk.com/view/appinspect/SP-CAAAFDU`.
5. Test the app installation on clean instance of Splunk.
