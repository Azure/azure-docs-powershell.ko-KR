---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 19b8b5a00e5bcb75b90a91097316dc065afa025b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701104"
---
# <span data-ttu-id="9bc97-101">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="9bc97-101">Add-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="9bc97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bc97-102">SYNOPSIS</span></span>
<span data-ttu-id="9bc97-103">데이터 호수 분석 계정에 데이터 원본을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc97-103">Adds a data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="9bc97-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9bc97-104">SYNTAX</span></span>

### <span data-ttu-id="9bc97-105">AddDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9bc97-105">AddDataLakeStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bc97-106">AddBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9bc97-106">AddBlobStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bc97-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9bc97-107">DESCRIPTION</span></span>
<span data-ttu-id="9bc97-108">**Add-AzDataLakeAnalyticsDataSource** Cmdlet은 Azure Data Lake Analytics 계정에 데이터 원본을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc97-108">The **Add-AzDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="9bc97-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9bc97-109">EXAMPLES</span></span>

### <span data-ttu-id="9bc97-110">예제 1: 계정에 데이터 원본 추가</span><span class="sxs-lookup"><span data-stu-id="9bc97-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="9bc97-111">이 명령은 data lake Store 데이터 원본을 데이터 호수 분석 계정에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc97-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="9bc97-112">변수</span><span class="sxs-lookup"><span data-stu-id="9bc97-112">PARAMETERS</span></span>

### <span data-ttu-id="9bc97-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="9bc97-113">-AccessKey</span></span>
<span data-ttu-id="9bc97-114">추가할 Azure Blob 저장소 계정의 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc97-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

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

### <span data-ttu-id="9bc97-115">-계정</span><span class="sxs-lookup"><span data-stu-id="9bc97-115">-Account</span></span>
<span data-ttu-id="9bc97-116">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc97-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="9bc97-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="9bc97-117">-Blob</span></span>
<span data-ttu-id="9bc97-118">추가할 Azure Blob 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc97-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

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

### <span data-ttu-id="9bc97-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9bc97-119">-DataLakeStore</span></span>
<span data-ttu-id="9bc97-120">추가할 Azure Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc97-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

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

### <span data-ttu-id="9bc97-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bc97-121">-DefaultProfile</span></span>
<span data-ttu-id="9bc97-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9bc97-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9bc97-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bc97-123">-ResourceGroupName</span></span>
<span data-ttu-id="9bc97-124">Data Lake Analytics 계정의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc97-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="9bc97-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bc97-125">CommonParameters</span></span>
<span data-ttu-id="9bc97-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9bc97-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bc97-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bc97-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bc97-128">입력</span><span class="sxs-lookup"><span data-stu-id="9bc97-128">INPUTS</span></span>

### <span data-ttu-id="9bc97-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9bc97-129">System.String</span></span>

## <span data-ttu-id="9bc97-130">출력</span><span class="sxs-lookup"><span data-stu-id="9bc97-130">OUTPUTS</span></span>

### <span data-ttu-id="9bc97-131">System. 개체</span><span class="sxs-lookup"><span data-stu-id="9bc97-131">System.Object</span></span>
## <span data-ttu-id="9bc97-132">상속자</span><span class="sxs-lookup"><span data-stu-id="9bc97-132">NOTES</span></span>

## <span data-ttu-id="9bc97-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9bc97-133">RELATED LINKS</span></span>

[<span data-ttu-id="9bc97-134">제거-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="9bc97-134">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="9bc97-135">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="9bc97-135">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


