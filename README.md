# ADF Raw → Bronze Mini Pipeline

## Connect  
Create a linked service to your storage and test it successfully.

## Datasets  
- **[ds_source](ca://s?q=Explain_ds_source_dataset)** → `raw/hotels.csv`  
- **[ds_sink](ca://s?q=Explain_ds_sink_dataset)** → `bronze/`  
CSV, first row as header.

## Move  
Copy activity: source = ds_source, sink = ds_sink.  
After Debug, `hotels.csv` should appear in bronze.

## Inspect  
Create **[ds_raw_folder](ca://s?q=Explain_ds_raw_folder_dataset)** → points to `raw/` (no file).  
Get Metadata → enable Child Items → Debug → view file list.



# Eng_Azure_Data_Factory_Studio_StayNest [Output of - List a folder with Get Metadata]:
{
  "childItems": [
    {
      "name": "bookings.csv",
      "type": "File"
    },
    {
      "name": "customers.csv",
      "type": "File"
    },
    {
      "name": "hotels.csv",
      "type": "File"
    }
  ],
  "effectiveIntegrationRuntime": "AutoResolveIntegrationRuntime (East US)",
  "executionDuration": 1,
  "durationInQueue": {
    "integrationRuntimeQueue": 1
  },
  "billingReference": {
    "activityType": "PipelineActivity",
    "billableDuration": [
      {
        "meterType": "AzureIR",
        "duration": 0.016666666666666666,
        "unit": "Hours"
      }
    ]
  }
}
