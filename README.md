# AzureAISearchresource_projeto_dio
Readme.md descrevendo o passo a passo para se configurar uma pesquisa


Create an Azure AI Search resource
Sign into the Azure portal.

Click the + Create a resource button, search for Azure AI Search, and create a Azure AI Search resource with the following settings:

Subscription: Your Azure subscription.
Resource group: Select or create a resource group with a unique name.
Service name: A unique name.
Location: Choose any available region.
Pricing tier: Basic
Select Review + create, and after you see the response Validation Success, select Create.

After deployment completes, select Go to resource. On the Azure AI Search overview page, you can add indexes, import data, and search created indexes.

Create an Azure AI services resource
You’ll need to provision an Azure AI services resource that’s in the same location as your Azure AI Search resource. Your search solution will use this resource to enrich the data in the datastore with AI-generated insights.

Return to the home page of the Azure portal. Click the ＋Create a resource button and search for Azure AI services. Select create an Azure AI services plan. You will be taken to a page to create an Azure AI services resource. Configure it with the following settings:
Subscription: Your Azure subscription.
Resource group: The same resource group as your Azure AI Search resource.
Region: The same location as your Azure AI Search resource.
Name: A unique name.
Pricing tier: Standard S0
By checking this box I acknowledge that I have read and understood all the terms below: Selected
Select Review + create. After you see the response Validation Passed, select Create.

Wait for deployment to complete, then view the deployment details.

Create a storage account
Return to the home page of the Azure portal, and then select the + Create a resource button.

Search for storage account, and create a Storage account resource with the following settings:
Subscription: Your Azure subscription.
Resource group: The same resource group as your Azure AI Search and Azure AI services resources.
Storage account name: A unique name.
Location: Choose any available location.
Performance: Standard
Redundancy: Locally redundant storage (LRS)
Click Review and then click Create. Wait for deployment to complete, and then go to the deployed resource.

In the Azure Storage account you created, in the left-hand menu pane, select Configuration (under Settings).
Change the setting for Allow Blob anonymous access to Enabled and then select Save.











Search explorer json


 
{
 "search": "locations:'Chicago'",
 "count": true
}

    
{
  "@odata.context": "https://labexam900.search.windows.net/indexes('coffee-index')/$metadata#docs(*)",
  "@odata.count": 3,
  "value": [
    {
      "@search.score": 2.6786075,
      "content": "\nReview: I often make Fourth Coffee my meeting spot for my client meetings weekday mornings. I own a small business and the folks who work at Fourth Coffee are always very friendly. It leaves a good impression on my clients. There are also plenty of drink selections, good wi-fi, and seating. Some of my favorite coffees are the lavender honey latte and, in the winter, the apple-chai latte. There are delicious baked goods offered as well. \nDate: October 21, 2018\nLocation: Chicago, Illinois \n\nimage1.png\n\n\n\n",
      "metadata_storage_path": "aHR0cHM6Ly9zdG9yYWdlYmFzaWNsZWFybmluZy5ibG9iLmNvcmUud2luZG93cy5uZXQvY29mZmVlLXJldmlld3MvcmV2aWV3LTUuZG9jeA2",
      "locations": [
        "meeting spot",
        "Chicago",
        "Illinois"
      ],
      "keyphrases": [
        "delicious baked goods",
        "lavender honey latte",
        "apple-chai latte",
        "Fourth Coffee",
        "meeting spot",
        "client meetings",
        "small business",
        "good impression",
        "drink selections",
        "good wi",
        "favorite coffees",
        "Review",
        "mornings",
        "folks",
        "clients",
        "plenty",
        "fi",
        "seating",
        "winter",
        "Date",
        "October",
        "Location",
        "Chicago",
        "Illinois"
      ],
      "sentiment": "[\"positive\"]",
      "merged_content": "\nReview: I often make Fourth Coffee my meeting spot for my client meetings weekday mornings. I own a small business and the folks who work at Fourth Coffee are always very friendly. It leaves a good impression on my clients. There are also plenty of drink selections, good wi-fi, and seating. Some of my favorite coffees are the lavender honey latte and, in the winter, the apple-chai latte. There are delicious baked goods offered as well. \nDate: October 21, 2018\nLocation: Chicago, Illinois \n\nimage1.png\n  \n\n\n",
      "text": [
        ""
      ],
      "layoutText": [
        "{\"language\":\"en\",\"text\":\"\",\"lines\":[],\"words\":[]}"
      ],
      "imageTags": [
        "clothing",
        "person",
        "furniture",
        "human face",
        "chair",
        "table",
        "woman",
        "indoor",
        "window",
        "desk",
        "sitting",
        "people",
        "restaurant"
      ],
      "imageCaption": [
        "{\"tags\":[\"person\",\"woman\",\"laptop\",\"dish\"],\"captions\":[{\"text\":\"a woman showing a woman something on a tablet\",\"confidence\":0.513512134552002}]}"
      ]
    },
    {
      "@search.score": 1.0858147,
      "content": "\n\nReview: The coffee tastings every Wednesday afternoon are so fun. Each month there is a new drink theme. You do need to book a spot in advance to attend. It is very worth it! I also love their local music. Fourth Coffee brings in rising artists every weekend. I like to head over there mid-afternoon on weekdays when it’s not too busy and get a slice of pie or their seasonal baked goods.  \nDate: August 13, 2018\nLocation: Chicago, Illinois  \n\nimage1.png\n\n\n\nimage2.png\n\n\n\n",
      "metadata_storage_path": "aHR0cHM6Ly9zdG9yYWdlYmFzaWNsZWFybmluZy5ibG9iLmNvcmUud2luZG93cy5uZXQvY29mZmVlLXJldmlld3MvcmV2aWV3LTQuZG9jeA2",
      "locations": [
        "Fourth Coffee",
        "Chicago",
        "Illinois"
      ],
      "keyphrases": [
        "new drink theme",
        "seasonal baked goods",
        "coffee tastings",
        "local music",
        "Fourth Coffee",
        "rising artists",
        "ierican Coffee",
        "Review",
        "afternoon",
        "spot",
        "advance",
        "weekdays",
        "slice",
        "pie",
        "Date",
        "August",
        "Location",
        "Chicago",
        "Illinois"
      ],
      "sentiment": "[\"positive\"]",
      "merged_content": "\n\nReview: The coffee tastings every Wednesday afternoon are so fun. Each month there is a new drink theme. You do need to book a spot in advance to attend. It is very worth it! I also love their local music. Fourth Coffee brings in rising artists every weekend. I like to head over there mid-afternoon on weekdays when it’s not too busy and get a slice of pie or their seasonal baked goods.  \nDate: August 13, 2018\nLocation: Chicago, Illinois  \n\nimage1.png\n ierican Coffee 114 10148/0034 \n\n\nimage2.png\n  \n\n\n",
      "text": [
        "ierican Coffee 114 10148/0034",
        ""
      ],
      "layoutText": [
        "{\"language\":\"en\",\"text\":\"ierican Coffee 114 10148/0034\",\"lines\":[{\"boundingBox\":[{\"x\":701,\"y\":284},{\"x\":649,\"y\":303},{\"x\":647,\"y\":297},{\"x\":699,\"y\":279}],\"text\":\"ierican Coffee\"},{\"boundingBox\":[{\"x\":682,\"y\":241},{\"x\":614,\"y\":263},{\"x\":611,\"y\":251},{\"x\":678,\"y\":228}],\"text\":\"114 10148/0034\"}],\"words\":[{\"boundingBox\":[{\"x\":701,\"y\":285},{\"x\":679,\"y\":293},{\"x\":676,\"y\":287},{\"x\":699,\"y\":279}],\"text\":\"ierican\"},{\"boundingBox\":[{\"x\":676,\"y\":294},{\"x\":652,\"y\":303},{\"x\":650,\"y\":297},{\"x\":674,\"y\":288}],\"text\":\"Coffee\"},{\"boundingBox\":[{\"x\":682,\"y\":242},{\"x\":672,\"y\":245},{\"x\":668,\"y\":232},{\"x\":678,\"y\":229}],\"text\":\"114\"},{\"boundingBox\":[{\"x\":669,\"y\":245},{\"x\":618,\"y\":262},{\"x\":615,\"y\":251},{\"x\":666,\"y\":233}],\"text\":\"10148/0034\"}]}",
        "{\"language\":\"en\",\"text\":\"\",\"lines\":[],\"words\":[]}"
      ],
      "imageTags": [
        "food",
        "chocolate",
        "table",
        "cup",
        "serveware",
        "indoor",
        "cocoa solids",
        "caffeine",
        "tableware",
        "sitting",
        "coffee",
        "dessert",
        "musical instrument",
        "music",
        "concert",
        "clothing",
        "person",
        "string instrument",
        "human face",
        "microphone",
        "plucked string instruments",
        "acoustic guitar",
        "guitar",
        "indoor",
        "woman"
      ],
      "imageCaption": [
        "{\"tags\":[\"cup\",\"coffee\",\"table\",\"indoor\",\"pastry\",\"beverage\",\"breakfast\",\"close\"],\"captions\":[{\"text\":\"a group of small cups with brown liquid in them\",\"confidence\":0.39556038379669189}]}",
        "{\"tags\":[\"person\",\"music\",\"guitar\",\"bowed instrument\",\"bass\"],\"captions\":[{\"text\":\"a person playing a guitar\",\"confidence\":0.54444891214370728}]}"
      ]
    },
    {
      "@search.score": 0.96866095,
      "content": "Review: Today I was truly disappointed with how long I had to wait for the pastries I ordered ahead of time. When I got my box, some of the pastries seemed stale. Terrible experience!  \nDate: October 23, 2018\nLocation: Chicago, Illinois \n\n",
      "metadata_storage_path": "aHR0cHM6Ly9zdG9yYWdlYmFzaWNsZWFybmluZy5ibG9iLmNvcmUud2luZG93cy5uZXQvY29mZmVlLXJldmlld3MvcmV2aWV3LTguZG9jeA2",
      "locations": [
        "Chicago",
        "Illinois"
      ],
      "keyphrases": [
        "Terrible experience",
        "Review",
        "pastries",
        "time",
        "box",
        "Date",
        "October",
        "Location",
        "Chicago",
        "Illinois"
      ],
      "sentiment": "[\"negative\"]",
      "merged_content": "Review: Today I was truly disappointed with how long I had to wait for the pastries I ordered ahead of time. When I got my box, some of the pastries seemed stale. Terrible experience!  \nDate: October 23, 2018\nLocation: Chicago, Illinois \n\n",
      "text": [],
      "layoutText": [],
      "imageTags": [],
      "imageCaption": []
    }
  ]
}


{
 "search": "sentiment:'negative'",
 "count": true
}

{
  "@odata.context": "https://labexam900.search.windows.net/indexes('coffee-index')/$metadata#docs(*)",
  "@odata.count": 1,
  "value": [
    {
      "@search.score": 0.2876821,
      "content": "Review: Today I was truly disappointed with how long I had to wait for the pastries I ordered ahead of time. When I got my box, some of the pastries seemed stale. Terrible experience!  \nDate: October 23, 2018\nLocation: Chicago, Illinois \n\n",
      "metadata_storage_path": "aHR0cHM6Ly9zdG9yYWdlYmFzaWNsZWFybmluZy5ibG9iLmNvcmUud2luZG93cy5uZXQvY29mZmVlLXJldmlld3MvcmV2aWV3LTguZG9jeA2",
      "locations": [
        "Chicago",
        "Illinois"
      ],
      "keyphrases": [
        "Terrible experience",
        "Review",
        "pastries",
        "time",
        "box",
        "Date",
        "October",
        "Location",
        "Chicago",
        "Illinois"
      ],
      "sentiment": "[\"negative\"]",
      "merged_content": "Review: Today I was truly disappointed with how long I had to wait for the pastries I ordered ahead of time. When I got my box, some of the pastries seemed stale. Terrible experience!  \nDate: October 23, 2018\nLocation: Chicago, Illinois \n\n",
      "text": [],
      "layoutText": [],
      "imageTags": [],
      "imageCaption": []
    }
  ]
}








