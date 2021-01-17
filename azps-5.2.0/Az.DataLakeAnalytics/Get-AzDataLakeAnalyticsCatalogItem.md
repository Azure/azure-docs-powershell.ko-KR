---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: fb0e73d338c54b93626ee3a5ee78bbbe4adca884
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370021"
---
# <span data-ttu-id="32145-101">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="32145-101">Get-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="32145-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32145-102">SYNOPSIS</span></span>
<span data-ttu-id="32145-103">Data Lake Analytics 카탈로그 항목 또는 항목 유형을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32145-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

## <span data-ttu-id="32145-104">구문</span><span class="sxs-lookup"><span data-stu-id="32145-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32145-105">설명</span><span class="sxs-lookup"><span data-stu-id="32145-105">DESCRIPTION</span></span>
<span data-ttu-id="32145-106">**Get-AzDataLakeAnalyticsCatalogItem은** 지정된 Azure Data Lake Analytics 카탈로그 항목을 얻거나 지정된 형식의 카탈로그 항목을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32145-106">The **Get-AzDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="32145-107">예제</span><span class="sxs-lookup"><span data-stu-id="32145-107">EXAMPLES</span></span>

### <span data-ttu-id="32145-108">예제 1: 지정된 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32145-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="32145-109">이 명령은 지정된 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32145-109">This command gets the specified database.</span></span>

### <span data-ttu-id="32145-110">예제 2: 지정된 데이터베이스 및 schema의 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32145-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="32145-111">이 명령은 지정된 데이터베이스의 테이블 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="32145-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="32145-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32145-112">PARAMETERS</span></span>

### <span data-ttu-id="32145-113">-Account</span><span class="sxs-lookup"><span data-stu-id="32145-113">-Account</span></span>
<span data-ttu-id="32145-114">Data Lake Analytics 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32145-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="32145-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32145-115">-DefaultProfile</span></span>
<span data-ttu-id="32145-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="32145-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32145-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="32145-117">-ItemType</span></span>
<span data-ttu-id="32145-118">인입하거나 나열할 항목의 카탈로그 항목 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32145-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="32145-119">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="32145-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="32145-120">데이터베이스</span><span class="sxs-lookup"><span data-stu-id="32145-120">Database</span></span>
- <span data-ttu-id="32145-121">Schema</span><span class="sxs-lookup"><span data-stu-id="32145-121">Schema</span></span>
- <span data-ttu-id="32145-122">어셈블리</span><span class="sxs-lookup"><span data-stu-id="32145-122">Assembly</span></span>
- <span data-ttu-id="32145-123">표</span><span class="sxs-lookup"><span data-stu-id="32145-123">Table</span></span>
- <span data-ttu-id="32145-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="32145-124">TableValuedFunction</span></span>
- <span data-ttu-id="32145-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="32145-125">TableStatistics</span></span>
- <span data-ttu-id="32145-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="32145-126">ExternalDataSource</span></span>
- <span data-ttu-id="32145-127">보기</span><span class="sxs-lookup"><span data-stu-id="32145-127">View</span></span>
- <span data-ttu-id="32145-128">프로시저</span><span class="sxs-lookup"><span data-stu-id="32145-128">Procedure</span></span>
- <span data-ttu-id="32145-129">비밀</span><span class="sxs-lookup"><span data-stu-id="32145-129">Secret</span></span>
- <span data-ttu-id="32145-130">자격 증명</span><span class="sxs-lookup"><span data-stu-id="32145-130">Credential</span></span>
- <span data-ttu-id="32145-131">형식</span><span class="sxs-lookup"><span data-stu-id="32145-131">Types</span></span>
- <span data-ttu-id="32145-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="32145-132">TablePartition</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType
Parameter Sets: (All)
Aliases:
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32145-133">-Path</span><span class="sxs-lookup"><span data-stu-id="32145-133">-Path</span></span>
<span data-ttu-id="32145-134">검색할 항목 또는 나열할 항목의 부모 항목에 대한 다중 파트 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32145-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="32145-135">경로의 부분은 기간(.)으로 구분해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32145-135">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32145-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32145-136">CommonParameters</span></span>
<span data-ttu-id="32145-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="32145-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32145-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="32145-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32145-139">입력</span><span class="sxs-lookup"><span data-stu-id="32145-139">INPUTS</span></span>

### <span data-ttu-id="32145-140">System.String</span><span class="sxs-lookup"><span data-stu-id="32145-140">System.String</span></span>

### <span data-ttu-id="32145-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="32145-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="32145-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="32145-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="32145-143">출력</span><span class="sxs-lookup"><span data-stu-id="32145-143">OUTPUTS</span></span>

### <span data-ttu-id="32145-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span><span class="sxs-lookup"><span data-stu-id="32145-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="32145-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="32145-145">NOTES</span></span>

## <span data-ttu-id="32145-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32145-146">RELATED LINKS</span></span>

[<span data-ttu-id="32145-147">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="32145-147">Test-AzDataLakeAnalyticsCatalogItem</span></span>](./Test-AzDataLakeAnalyticsCatalogItem.md)


