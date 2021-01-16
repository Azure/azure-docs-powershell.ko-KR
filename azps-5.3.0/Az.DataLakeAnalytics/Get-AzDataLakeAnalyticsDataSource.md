---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: e14e4c1b58b24cb8065681ae806789cd1252a0db
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493483"
---
# <span data-ttu-id="fc467-101">Get-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="fc467-101">Get-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="fc467-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc467-102">SYNOPSIS</span></span>
<span data-ttu-id="fc467-103">Data Lake Analytics 데이터 원본을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fc467-103">Gets a Data Lake Analytics data source.</span></span>

## <span data-ttu-id="fc467-104">구문</span><span class="sxs-lookup"><span data-stu-id="fc467-104">SYNTAX</span></span>

### <span data-ttu-id="fc467-105">GetAllDataSources(기본값)</span><span class="sxs-lookup"><span data-stu-id="fc467-105">GetAllDataSources (Default)</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc467-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="fc467-106">GetDataLakeStoreAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc467-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fc467-107">GetBlobStorageAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc467-108">설명</span><span class="sxs-lookup"><span data-stu-id="fc467-108">DESCRIPTION</span></span>
<span data-ttu-id="fc467-109">**Get-AzDataLakeAnalyticsDataSource** cmdlet은 Azure Data Lake Analytics 데이터 원본을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fc467-109">The **Get-AzDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="fc467-110">예제</span><span class="sxs-lookup"><span data-stu-id="fc467-110">EXAMPLES</span></span>

### <span data-ttu-id="fc467-111">예제 1: 계정에서 데이터 원본을 얻다</span><span class="sxs-lookup"><span data-stu-id="fc467-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="fc467-112">이 명령은 Data Lake Analytics 계정에서 ContosoAdls라는 Data Lake Store 데이터 원본을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fc467-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="fc467-113">예제 2: Data Lake Analytics 계정에서 Data Lake Store 계정 목록 얻기</span><span class="sxs-lookup"><span data-stu-id="fc467-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="fc467-114">이 명령은 Data Lake Analytics 계정에서 모든 Data Lake Store 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fc467-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="fc467-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc467-115">PARAMETERS</span></span>

### <span data-ttu-id="fc467-116">-Account</span><span class="sxs-lookup"><span data-stu-id="fc467-116">-Account</span></span>
<span data-ttu-id="fc467-117">이 cmdlet이 데이터 원본을 얻을 Data Lake Analytics 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc467-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="fc467-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="fc467-118">-Blob</span></span>
<span data-ttu-id="fc467-119">Azure Blob Storage 데이터 원본의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc467-119">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="fc467-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fc467-120">-DataLakeStore</span></span>
<span data-ttu-id="fc467-121">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc467-121">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="fc467-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc467-122">-DefaultProfile</span></span>
<span data-ttu-id="fc467-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fc467-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc467-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc467-124">-ResourceGroupName</span></span>
<span data-ttu-id="fc467-125">데이터 원본을 포함하는 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc467-125">Specifies the resource group name that contains the data source.</span></span>

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

### <span data-ttu-id="fc467-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc467-126">CommonParameters</span></span>
<span data-ttu-id="fc467-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fc467-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc467-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fc467-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc467-129">입력</span><span class="sxs-lookup"><span data-stu-id="fc467-129">INPUTS</span></span>

### <span data-ttu-id="fc467-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fc467-130">System.String</span></span>

## <span data-ttu-id="fc467-131">출력</span><span class="sxs-lookup"><span data-stu-id="fc467-131">OUTPUTS</span></span>

### <span data-ttu-id="fc467-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="fc467-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span></span>

### <span data-ttu-id="fc467-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="fc467-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span></span>

### <span data-ttu-id="fc467-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span><span class="sxs-lookup"><span data-stu-id="fc467-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span></span>

## <span data-ttu-id="fc467-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fc467-135">NOTES</span></span>

## <span data-ttu-id="fc467-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc467-136">RELATED LINKS</span></span>

[<span data-ttu-id="fc467-137">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="fc467-137">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="fc467-138">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="fc467-138">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="fc467-139">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="fc467-139">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


