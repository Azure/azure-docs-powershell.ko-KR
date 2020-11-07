---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2a69517a3b8a7624098a01e621e51b81dfaba835
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701103"
---
# <span data-ttu-id="f900f-101">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="f900f-101">Get-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="f900f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f900f-102">SYNOPSIS</span></span>
<span data-ttu-id="f900f-103">Data Lake Analytics 카탈로그 항목 또는 항목 유형을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f900f-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

## <span data-ttu-id="f900f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f900f-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f900f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f900f-105">DESCRIPTION</span></span>
<span data-ttu-id="f900f-106">**AzDataLakeAnalyticsCatalogItem** 에서 지정 된 Azure Data Lake Analytics 카탈로그 항목을 가져오거나 지정 된 형식의 카탈로그 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f900f-106">The **Get-AzDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="f900f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f900f-107">EXAMPLES</span></span>

### <span data-ttu-id="f900f-108">예제 1: 지정 된 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="f900f-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="f900f-109">이 명령은 지정 된 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f900f-109">This command gets the specified database.</span></span>

### <span data-ttu-id="f900f-110">예제 2: 지정 된 데이터베이스 및 스키마의 테이블 가져오기</span><span class="sxs-lookup"><span data-stu-id="f900f-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="f900f-111">이 명령은 지정 된 데이터베이스의 테이블 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f900f-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="f900f-112">변수</span><span class="sxs-lookup"><span data-stu-id="f900f-112">PARAMETERS</span></span>

### <span data-ttu-id="f900f-113">-계정</span><span class="sxs-lookup"><span data-stu-id="f900f-113">-Account</span></span>
<span data-ttu-id="f900f-114">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f900f-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="f900f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f900f-115">-DefaultProfile</span></span>
<span data-ttu-id="f900f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f900f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f900f-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="f900f-117">-ItemType</span></span>
<span data-ttu-id="f900f-118">가져오고 나열 되는 항목의 카탈로그 항목 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f900f-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="f900f-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f900f-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f900f-120">데이터</span><span class="sxs-lookup"><span data-stu-id="f900f-120">Database</span></span>
- <span data-ttu-id="f900f-121">스키마</span><span class="sxs-lookup"><span data-stu-id="f900f-121">Schema</span></span>
- <span data-ttu-id="f900f-122">어셈블리가</span><span class="sxs-lookup"><span data-stu-id="f900f-122">Assembly</span></span>
- <span data-ttu-id="f900f-123">테이블로</span><span class="sxs-lookup"><span data-stu-id="f900f-123">Table</span></span>
- <span data-ttu-id="f900f-124">Table의 Edfunction</span><span class="sxs-lookup"><span data-stu-id="f900f-124">TableValuedFunction</span></span>
- <span data-ttu-id="f900f-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="f900f-125">TableStatistics</span></span>
- <span data-ttu-id="f900f-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="f900f-126">ExternalDataSource</span></span>
- <span data-ttu-id="f900f-127">보려고</span><span class="sxs-lookup"><span data-stu-id="f900f-127">View</span></span>
- <span data-ttu-id="f900f-128">절차</span><span class="sxs-lookup"><span data-stu-id="f900f-128">Procedure</span></span>
- <span data-ttu-id="f900f-129">기밀</span><span class="sxs-lookup"><span data-stu-id="f900f-129">Secret</span></span>
- <span data-ttu-id="f900f-130">자격 증명</span><span class="sxs-lookup"><span data-stu-id="f900f-130">Credential</span></span>
- <span data-ttu-id="f900f-131">형식</span><span class="sxs-lookup"><span data-stu-id="f900f-131">Types</span></span>
- <span data-ttu-id="f900f-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="f900f-132">TablePartition</span></span>

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

### <span data-ttu-id="f900f-133">-Path</span><span class="sxs-lookup"><span data-stu-id="f900f-133">-Path</span></span>
<span data-ttu-id="f900f-134">검색할 항목에 대 한 다중 파트 경로를 지정 하거나 나열할 항목의 상위 항목에 대 한 여러 부분으로 구성 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f900f-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="f900f-135">경로의 각 부분은 마침표 (.)로 구분 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f900f-135">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="f900f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f900f-136">CommonParameters</span></span>
<span data-ttu-id="f900f-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f900f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f900f-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f900f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f900f-139">입력</span><span class="sxs-lookup"><span data-stu-id="f900f-139">INPUTS</span></span>

### <span data-ttu-id="f900f-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f900f-140">System.String</span></span>

### <span data-ttu-id="f900f-141">DataLakeAnalytics. DataLakeAnalyticsEnums + CatalogItemType.</span><span class="sxs-lookup"><span data-stu-id="f900f-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="f900f-142">DataLakeAnalytics. CatalogPathInstance/.</span><span class="sxs-lookup"><span data-stu-id="f900f-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="f900f-143">출력</span><span class="sxs-lookup"><span data-stu-id="f900f-143">OUTPUTS</span></span>

### <span data-ttu-id="f900f-144">DataLake. CatalogItem-. \*</span><span class="sxs-lookup"><span data-stu-id="f900f-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="f900f-145">상속자</span><span class="sxs-lookup"><span data-stu-id="f900f-145">NOTES</span></span>

## <span data-ttu-id="f900f-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f900f-146">RELATED LINKS</span></span>

[<span data-ttu-id="f900f-147">테스트-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="f900f-147">Test-AzDataLakeAnalyticsCatalogItem</span></span>](./Test-AzDataLakeAnalyticsCatalogItem.md)

