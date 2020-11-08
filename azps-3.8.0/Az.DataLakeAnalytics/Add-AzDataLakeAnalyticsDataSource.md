---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: ddb291a72d3c35c79321ddefa0832d46c489998f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042803"
---
# <span data-ttu-id="c30f0-101">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="c30f0-101">Add-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="c30f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c30f0-102">SYNOPSIS</span></span>
<span data-ttu-id="c30f0-103">데이터 호수 분석 계정에 데이터 원본을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c30f0-103">Adds a data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="c30f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c30f0-104">SYNTAX</span></span>

### <span data-ttu-id="c30f0-105">AddDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c30f0-105">AddDataLakeStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c30f0-106">AddBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c30f0-106">AddBlobStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c30f0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c30f0-107">DESCRIPTION</span></span>
<span data-ttu-id="c30f0-108">**Add-AzDataLakeAnalyticsDataSource** Cmdlet은 Azure Data Lake Analytics 계정에 데이터 원본을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c30f0-108">The **Add-AzDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="c30f0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c30f0-109">EXAMPLES</span></span>

### <span data-ttu-id="c30f0-110">예제 1: 계정에 데이터 원본 추가</span><span class="sxs-lookup"><span data-stu-id="c30f0-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="c30f0-111">이 명령은 data lake Store 데이터 원본을 데이터 호수 분석 계정에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c30f0-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="c30f0-112">변수</span><span class="sxs-lookup"><span data-stu-id="c30f0-112">PARAMETERS</span></span>

### <span data-ttu-id="c30f0-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="c30f0-113">-AccessKey</span></span>
<span data-ttu-id="c30f0-114">추가할 Azure Blob 저장소 계정의 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c30f0-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddBlobStorageAccount
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c30f0-115">-계정</span><span class="sxs-lookup"><span data-stu-id="c30f0-115">-Account</span></span>
<span data-ttu-id="c30f0-116">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c30f0-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c30f0-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="c30f0-117">-Blob</span></span>
<span data-ttu-id="c30f0-118">추가할 Azure Blob 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c30f0-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c30f0-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c30f0-119">-DataLakeStore</span></span>
<span data-ttu-id="c30f0-120">추가할 Azure Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c30f0-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddDataLakeStorageAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c30f0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c30f0-121">-DefaultProfile</span></span>
<span data-ttu-id="c30f0-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c30f0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c30f0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c30f0-123">-ResourceGroupName</span></span>
<span data-ttu-id="c30f0-124">Data Lake Analytics 계정의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c30f0-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c30f0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c30f0-125">CommonParameters</span></span>
<span data-ttu-id="c30f0-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c30f0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c30f0-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c30f0-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c30f0-128">입력</span><span class="sxs-lookup"><span data-stu-id="c30f0-128">INPUTS</span></span>

### <span data-ttu-id="c30f0-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c30f0-129">System.String</span></span>

## <span data-ttu-id="c30f0-130">출력</span><span class="sxs-lookup"><span data-stu-id="c30f0-130">OUTPUTS</span></span>

### <span data-ttu-id="c30f0-131">System. 개체</span><span class="sxs-lookup"><span data-stu-id="c30f0-131">System.Object</span></span>
## <span data-ttu-id="c30f0-132">상속자</span><span class="sxs-lookup"><span data-stu-id="c30f0-132">NOTES</span></span>

## <span data-ttu-id="c30f0-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c30f0-133">RELATED LINKS</span></span>

[<span data-ttu-id="c30f0-134">제거-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="c30f0-134">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="c30f0-135">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="c30f0-135">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


