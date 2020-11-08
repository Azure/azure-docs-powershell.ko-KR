---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2879923b38b6813213fe6819f84fa55a593f6930
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033993"
---
# <span data-ttu-id="d8458-101">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="d8458-101">Test-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="d8458-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8458-102">SYNOPSIS</span></span>
<span data-ttu-id="d8458-103">카탈로그 항목이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8458-103">Checks for the existence of a catalog item.</span></span>

## <span data-ttu-id="d8458-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d8458-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8458-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d8458-105">DESCRIPTION</span></span>
<span data-ttu-id="d8458-106">**AzDataLakeAnalyticsCatalogItem** Cmdlet은 Azure Data Lake Analytics 카탈로그 항목이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8458-106">The **Test-AzDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="d8458-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d8458-107">EXAMPLES</span></span>

### <span data-ttu-id="d8458-108">예제 1: 카탈로그 항목이 있는지 테스트</span><span class="sxs-lookup"><span data-stu-id="d8458-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="d8458-109">이 명령은 지정 된 스키마 항목이 있는지 여부를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8458-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="d8458-110">변수</span><span class="sxs-lookup"><span data-stu-id="d8458-110">PARAMETERS</span></span>

### <span data-ttu-id="d8458-111">-계정</span><span class="sxs-lookup"><span data-stu-id="d8458-111">-Account</span></span>
<span data-ttu-id="d8458-112">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8458-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d8458-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8458-113">-DefaultProfile</span></span>
<span data-ttu-id="d8458-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d8458-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8458-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="d8458-115">-ItemType</span></span>
<span data-ttu-id="d8458-116">확인할 항목의 카탈로그 항목 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8458-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="d8458-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d8458-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d8458-118">데이터</span><span class="sxs-lookup"><span data-stu-id="d8458-118">Database</span></span>
- <span data-ttu-id="d8458-119">스키마</span><span class="sxs-lookup"><span data-stu-id="d8458-119">Schema</span></span>
- <span data-ttu-id="d8458-120">어셈블리가</span><span class="sxs-lookup"><span data-stu-id="d8458-120">Assembly</span></span>
- <span data-ttu-id="d8458-121">테이블로</span><span class="sxs-lookup"><span data-stu-id="d8458-121">Table</span></span>
- <span data-ttu-id="d8458-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="d8458-122">TablePartition</span></span>
- <span data-ttu-id="d8458-123">Table의 Edfunction</span><span class="sxs-lookup"><span data-stu-id="d8458-123">TableValuedFunction</span></span>
- <span data-ttu-id="d8458-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="d8458-124">TableStatistics</span></span>
- <span data-ttu-id="d8458-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="d8458-125">ExternalDataSource</span></span>
- <span data-ttu-id="d8458-126">보려고</span><span class="sxs-lookup"><span data-stu-id="d8458-126">View</span></span>
- <span data-ttu-id="d8458-127">절차</span><span class="sxs-lookup"><span data-stu-id="d8458-127">Procedure</span></span>
- <span data-ttu-id="d8458-128">기밀</span><span class="sxs-lookup"><span data-stu-id="d8458-128">Secret</span></span>
- <span data-ttu-id="d8458-129">자격 증명</span><span class="sxs-lookup"><span data-stu-id="d8458-129">Credential</span></span>
- <span data-ttu-id="d8458-130">형식</span><span class="sxs-lookup"><span data-stu-id="d8458-130">Types</span></span>

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

### <span data-ttu-id="d8458-131">-Path</span><span class="sxs-lookup"><span data-stu-id="d8458-131">-Path</span></span>
<span data-ttu-id="d8458-132">가져올 항목의 경로 또는 나열할 항목의 상위 항목에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8458-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8458-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8458-133">CommonParameters</span></span>
<span data-ttu-id="d8458-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8458-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8458-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8458-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8458-136">입력</span><span class="sxs-lookup"><span data-stu-id="d8458-136">INPUTS</span></span>

### <span data-ttu-id="d8458-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d8458-137">System.String</span></span>

### <span data-ttu-id="d8458-138">DataLakeAnalytics. DataLakeAnalyticsEnums + CatalogItemType.</span><span class="sxs-lookup"><span data-stu-id="d8458-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="d8458-139">DataLakeAnalytics. CatalogPathInstance/.</span><span class="sxs-lookup"><span data-stu-id="d8458-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="d8458-140">출력</span><span class="sxs-lookup"><span data-stu-id="d8458-140">OUTPUTS</span></span>

### <span data-ttu-id="d8458-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d8458-141">System.Boolean</span></span>

## <span data-ttu-id="d8458-142">상속자</span><span class="sxs-lookup"><span data-stu-id="d8458-142">NOTES</span></span>

## <span data-ttu-id="d8458-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8458-143">RELATED LINKS</span></span>

[<span data-ttu-id="d8458-144">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="d8458-144">Get-AzDataLakeAnalyticsCatalogItem</span></span>](./Get-AzDataLakeAnalyticsCatalogItem.md)


