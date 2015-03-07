#OpInsights MP Samples
This repo contains sample management packs for System Center Operations Manager. These management pack samples illustrate collection rules that allow sending various data to Azure Operational Insights.

Below a list and description of the XML samples:

####OpInsights.Custom.Log.Test.Rules.xml 
This contains collection rules for text log files to be sent as Type=Event. Sample for this blog post http://blogs.technet.com/b/momteam/archive/2015/03/06/collecting-text-log-files-to-azure-operational-insights-using-system-center-operations-manager.aspx

Note - the data source module used to read the logs in this example is a pre-existing module in SCOM, not specific to Operational Insights – details on the module are on MSDN documentation https://msdn.microsoft.com/en-us/library/ee809315.aspx and caveats when using the module are described in this KB article http://support.microsoft.com/kb/2691973

####Microsoft.IntelligencePacks.LogManagement.Sample.Syslog.xml
This example contains a collection rule that receives syslog sent to a Management server, maps it a little better in the Event shape, and sends it to OpInsights. This is similar to the example by Michale here http://blogs.technet.com/b/omx/archive/2013/01/07/how-to-store-syslog-in-the-scom-data-warehouse.aspx
For better mapping you need to use something like the script-based mapper example here http://blogs.technet.com/b/momteam/archive/2014/07/29/how-to-collect-syslog-events-thru-operations-manager-scom-to-advisor-preview.aspx (will move/reconcile the two examples)
