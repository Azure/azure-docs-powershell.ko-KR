---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: e14e4c1b58b24cb8065681ae806789cd1252a0db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305861"
---
# <span data-ttu-id="6131a-101">Get-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="6131a-101">Get-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="6131a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6131a-102">SYNOPSIS</span></span>
<span data-ttu-id="6131a-103">Data Lake Analytics 데이터 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6131a-103">Gets a Data Lake Analytics data source.</span></span>

## <span data-ttu-id="6131a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6131a-104">SYNTAX</span></span>

### <span data-ttu-id="6131a-105">GetAllDataSources 원본 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6131a-105">GetAllDataSources (Default)</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6131a-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="6131a-106">GetDataLakeStoreAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6131a-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6131a-107">GetBlobStorageAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6131a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6131a-108">DESCRIPTION</span></span>
<span data-ttu-id="6131a-109">**AzDataLakeAnalyticsDataSource** Cmdlet은 Azure Data Lake Analytics 데이터 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6131a-109">The **Get-AzDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="6131a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6131a-110">EXAMPLES</span></span>

### <span data-ttu-id="6131a-111">예제 1: 계정에서 데이터 원본 가져오기</span><span class="sxs-lookup"><span data-stu-id="6131a-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="6131a-112">이 명령은 Data Lake Analytics 계정에서 ContosoAdls 이라는 Data Lake Store 데이터 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6131a-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="6131a-113">예제 2: Data Lake Analytics 계정에서 Data Lake Store 계정 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="6131a-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="6131a-114">이 명령은 Data Lake Analytics 계정에서 모든 Data Lake Store 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6131a-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="6131a-115">변수</span><span class="sxs-lookup"><span data-stu-id="6131a-115">PARAMETERS</span></span>

### <span data-ttu-id="6131a-116">-계정</span><span class="sxs-lookup"><span data-stu-id="6131a-116">-Account</span></span>
<span data-ttu-id="6131a-117">이 cmdlet이 데이터 원본을 가져오는 데이터 호수 분석 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6131a-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="6131a-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="6131a-118">-Blob</span></span>
<span data-ttu-id="6131a-119">Azure Blob 저장소 데이터 원본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6131a-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6131a-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6131a-120">-DataLakeStore</span></span>
<span data-ttu-id="6131a-121">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6131a-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDataLakeStoreAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6131a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6131a-122">-DefaultProfile</span></span>
<span data-ttu-id="6131a-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6131a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6131a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6131a-124">-ResourceGroupName</span></span>
<span data-ttu-id="6131a-125">데이터 원본을 포함 하는 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6131a-125">Specifies the resource group name that contains the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6131a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6131a-126">CommonParameters</span></span>
<span data-ttu-id="6131a-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6131a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6131a-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6131a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6131a-129">입력</span><span class="sxs-lookup"><span data-stu-id="6131a-129">INPUTS</span></span>

### <span data-ttu-id="6131a-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6131a-130">System.String</span></span>

## <span data-ttu-id="6131a-131">출력</span><span class="sxs-lookup"><span data-stu-id="6131a-131">OUTPUTS</span></span>

### <span data-ttu-id="6131a-132">DataLakeAnalytics. a n i. PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="6131a-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span></span>

### <span data-ttu-id="6131a-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="6131a-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span></span>

### <span data-ttu-id="6131a-134">DataLakeAnalytics. \* AdlDataSource</span><span class="sxs-lookup"><span data-stu-id="6131a-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span></span>

## <span data-ttu-id="6131a-135">상속자</span><span class="sxs-lookup"><span data-stu-id="6131a-135">NOTES</span></span>

## <span data-ttu-id="6131a-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6131a-136">RELATED LINKS</span></span>

[<span data-ttu-id="6131a-137">추가-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="6131a-137">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="6131a-138">제거-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="6131a-138">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="6131a-139">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="6131a-139">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


