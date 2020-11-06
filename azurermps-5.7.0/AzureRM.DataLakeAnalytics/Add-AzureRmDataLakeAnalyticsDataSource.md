---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/add-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 1f2fe13567bd17170fd73854ce5554a693210c7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528997"
---
# <span data-ttu-id="669b1-101">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="669b1-101">Add-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="669b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="669b1-102">SYNOPSIS</span></span>
<span data-ttu-id="669b1-103">데이터 호수 분석 계정에 데이터 원본을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="669b1-103">Adds a data source to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="669b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="669b1-104">SYNTAX</span></span>

### <span data-ttu-id="669b1-105">AddDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="669b1-105">AddDataLakeStorageAccount</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="669b1-106">AddBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="669b1-106">AddBlobStorageAccount</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="669b1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="669b1-107">DESCRIPTION</span></span>
<span data-ttu-id="669b1-108">**Add-AzureRmDataLakeAnalyticsDataSource** Cmdlet은 Azure Data Lake Analytics 계정에 데이터 원본을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="669b1-108">The **Add-AzureRmDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="669b1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="669b1-109">EXAMPLES</span></span>

### <span data-ttu-id="669b1-110">예제 1: 계정에 데이터 원본 추가</span><span class="sxs-lookup"><span data-stu-id="669b1-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="669b1-111">이 명령은 data lake Store 데이터 원본을 데이터 호수 분석 계정에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="669b1-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="669b1-112">변수</span><span class="sxs-lookup"><span data-stu-id="669b1-112">PARAMETERS</span></span>

### <span data-ttu-id="669b1-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="669b1-113">-AccessKey</span></span>
<span data-ttu-id="669b1-114">추가할 Azure Blob 저장소 계정의 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="669b1-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: String
Parameter Sets: AddBlobStorageAccount
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="669b1-115">-계정</span><span class="sxs-lookup"><span data-stu-id="669b1-115">-Account</span></span>
<span data-ttu-id="669b1-116">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="669b1-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="669b1-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="669b1-117">-Blob</span></span>
<span data-ttu-id="669b1-118">추가할 Azure Blob 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="669b1-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: String
Parameter Sets: AddBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="669b1-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="669b1-119">-DataLakeStore</span></span>
<span data-ttu-id="669b1-120">추가할 Azure Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="669b1-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: String
Parameter Sets: AddDataLakeStorageAccount
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="669b1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="669b1-121">-DefaultProfile</span></span>
<span data-ttu-id="669b1-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="669b1-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="669b1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="669b1-123">-ResourceGroupName</span></span>
<span data-ttu-id="669b1-124">Data Lake Analytics 계정의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="669b1-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="669b1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="669b1-125">CommonParameters</span></span>
<span data-ttu-id="669b1-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="669b1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="669b1-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="669b1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="669b1-128">입력</span><span class="sxs-lookup"><span data-stu-id="669b1-128">INPUTS</span></span>

### <span data-ttu-id="669b1-129">않아야</span><span class="sxs-lookup"><span data-stu-id="669b1-129">None</span></span>
<span data-ttu-id="669b1-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="669b1-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="669b1-131">출력</span><span class="sxs-lookup"><span data-stu-id="669b1-131">OUTPUTS</span></span>

### <span data-ttu-id="669b1-132">않아야</span><span class="sxs-lookup"><span data-stu-id="669b1-132">None</span></span>

## <span data-ttu-id="669b1-133">상속자</span><span class="sxs-lookup"><span data-stu-id="669b1-133">NOTES</span></span>

## <span data-ttu-id="669b1-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="669b1-134">RELATED LINKS</span></span>

[<span data-ttu-id="669b1-135">제거-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="669b1-135">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="669b1-136">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="669b1-136">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


