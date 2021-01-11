# Lab 1: Meeting the Technical Requirements

### Setup your Azure Account

By now, you should have activated your Azure Pass with a personal Outlook account (NOT your work email). If you haven't done so yet, find the instructions at [https://www.microsoftazurepass.com/howto](https://www.microsoftazurepass.com/howto).

### Environment Setup

These labs are intended to be used with the .NET Framework using Visual Studio 2019. This environment is prepared for you on your Lab VM as described by your instructor. Do not try to do these labs on your local device since you may not have the right requirements. Do all labs on your Lab VM which you can access through [esi.learnondemand.net](https://esi.learnondemand.net/User/Login?ReturnUrl=%2f).

### Urls and Keys Needed

Over the course of this lab, we will collect multiple Cognitive Services keys and storage keys. You should save all of them in a text file so you can easily access them in future labs. Make sure you are working in your Lab VM. Open a notepad and create a file with the following content. We will get the keys in later steps.

>_Keys_
>
>- Cognitive Services API Url:
>- Cognitive Services API key:
>- LUIS API Endpoint:
>- LUIS API Key:
>- LUIS API App ID:
>- Bot App Name:
>- Bot App ID:
>- Bot App Password:
>- Azure Storage Connection String:
>- Cosmos DB Url:
>- Cosmos DB Key:
>- DirectLine Key:

## Azure Setup

In the following steps, you will configure the Azure environment for the labs that follow.

### Cognitive Services

While the first lab focuses on the [Computer Vision](https://www.microsoft.com/cognitive-services/en-us/computer-vision-api) Cognitive Service, Microsoft Azure allows you to create a cognitive service account that spans all services, or you can elect to create a cognitive service account for an individual service.  In the following steps, you will create a single Azure resource that contains all available cognitive services endpoints.

1. Open the [Azure Portal](https://portal.azure.com)

1. Select **+ Create a Resource** and then enter **cognitive services** in the search box

1. Choose **Cognitive Services** from the available options, then select **Create**

    > **Note** Again to reiterate, you can create specific cognitive services resources or you can create a single resource that contains all the endpoints.

1. Select your subscription and resource group, these should be in your Azure Pass subscription.

1. Type a name of your own choosing

1. For the pricing tier, select **S0**

1. Check the two confirmation checkboxes

    >[!Note]
    >Microsoft updates the Azure portal and services on a regular basis.  These steps contained the appropriate items at the time of writing but options and dialogs may 
    differ if changes are made to Azure.  Check with your instructor for any anomalies that you may encounter.

1. Select **Review + create**

1. Once validation passes, select **Create**

1. Navigate to the new resource, under the **Resource Management** section in the left toolbar, select **Keys and Endpoints**

1. Copy the **API Key** and the **url of the endpoint** to your notepad

    ![Quick start and the Key1 and Endpoint values are highlighted](../images/lab01-cogskeys.png 'The service key and endpoint values are highlighted')

### Azure Storage Account

1. In the Azure Portal, select **+ Create a Resource** and then enter **storage** in the search box

1. Choose **Storage account** from the available options, then select **Create**

1. Select your subscription and resource group

1. Type a name for your account, using your initials to make it unbique. **ai100storagego**

1. For the location, select the same as your resource group

1. Performance should be **Standard**

1. Account kind should be **StorageV2 (general purpose v2**)

1. For replication, select **Locally-redundant storage (LRS)**

    ![The values for a storage account are displayed](../images/lab01-storageaccount.png 'Create a storage account')

1. Select **Review + create**

1. Select **Create**

1. Navigate to the new resource, select **Access Keys**

1. Copy the **Connection string** to your notepad

    ![The Access Keys and Connection string value is highlighted](../images/lab01-storageaccountkeys.png 'Copy the connection string')

1. Select **Overview**, then select **Containers**

    ![The overview and containers links are highlighted](../images/lab01-storageaccountcontainers.png 'Open the storage account containers')

1. Select **+ Container**

1. For the name, type **images**

    ![The container button is highlighted and the container name is populated.  The OK button is also highlighted.](../images/new-container.png 'Create a container called images')

1. Select **Create**

### Cosmos DB

1. Open the [Azure Portal](https://portal.azure.com)

1. Select **"+ Create a Resource"** and then enter **cosmos** in the search box

1. Choose **Azure Cosmos DB** from the available options.  

1. Select **Create**

1. Select your subscription and resource group

1. Type a unique account name such as **ai100cosmosdbgo**

1. Select a location that matches your resource group

    ![The cosmosdb creation details are populated.](../images/cosmosdb.png 'Create a cosmosdb resource')

1. Configure the remaining options as depicted in the above image

1. Select **Review + create**

1. Select **Create**

1. Navigate to the new resource, under **Settings**, select **Keys**

1. Copy the **URI** and the **PRIMARY KEY** to your notepad

### Bot Builder SDK

We will use the Bot Builder template for C# to create bots in this course.

### Download the Bot Builder SDK

1. Open a browser window to [Bot Builder SDK v4 Template for C# here](https://marketplace.visualstudio.com/items?itemName=BotBuilder.botbuilderv4)

1. Select **Download**

1. Navigate to the download folder location and double-click on the install

1. Ensure that all versions of Visual Studio are selected and select **Install**.  If prompted, select **End Tasks**.  

1. Select **Close**. You should now have the bot templates added to your Visual Studio templates.

### Bot Emulator

We will be developing a bot using the latest .NET SDK (v4).  In order to do local testing, we'll need to download the Bot Framework Emulator.

### Download the Bot Framework Emulator

You can download the v4 Bot Framework Emulator for testing your bot locally. The instructions for the rest of the labs will assume you've downloaded the v4 Emulator.

1. Download the emulator by going to [this page](https://github.com/Microsoft/BotFramework-Emulator/releases) and downloading the most recent version of the emulator that has the tag "4.6.0" or higher (select the "*-windows-setup.exe" file, if you are using windows).

    > **Note** The emulator installs to
    `"C:\Users\_your-username\AppData\Local\Programs\@bfemulatormain\Bot Framework Emulator.exe"`, but you can gain access to it through the start menu by searching for **bot framework**.

## Credits

Labs in this series were adapted from the [Cognitive Services Tutorial](https://github.com/noodlefrenzy/CognitiveServicesTutorial) and [Learn AI BootCamp](https://github.com/Azure/LearnAI-Bootcamp)

## Resources

To deepen your understanding of the architecture described here, and to involve your broader team in the development of AI solutions, we recommend reviewing the following resources:

- [Cognitive Services](https://www.microsoft.com/cognitive-services) - AI Engineer
- [Cosmos DB](https://docs.microsoft.com/en-us/azure/cosmos-db/) - Data Engineer
- [Azure Cognitive Search](https://azure.microsoft.com/en-us/services/search/) - Search Engineer
- [Bot Developer Portal](http://dev.botframework.com) - AI Engineer

## Next Steps

- [Lab 02-01: Implement Computer Vision](../Lab2-Implement_Computer_Vision/01-Introduction.md)
