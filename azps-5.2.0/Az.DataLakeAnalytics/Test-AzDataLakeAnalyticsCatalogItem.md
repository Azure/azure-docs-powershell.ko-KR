---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2879923b38b6813213fe6819f84fa55a593f6930
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336597"
---
# <span data-ttu-id="27dca-101">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="27dca-101">Test-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="27dca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27dca-102">SYNOPSIS</span></span>
<span data-ttu-id="27dca-103">카탈로그 항목의 존재를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="27dca-103">Checks for the existence of a catalog item.</span></span>

## <span data-ttu-id="27dca-104">구문</span><span class="sxs-lookup"><span data-stu-id="27dca-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27dca-105">설명</span><span class="sxs-lookup"><span data-stu-id="27dca-105">DESCRIPTION</span></span>
<span data-ttu-id="27dca-106">**Test-AzDataLakeAnalyticsCatalogItem** cmdlet은 Azure Data Lake Analytics 카탈로그 항목의 존재를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="27dca-106">The **Test-AzDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="27dca-107">예제</span><span class="sxs-lookup"><span data-stu-id="27dca-107">EXAMPLES</span></span>

### <span data-ttu-id="27dca-108">예제 1: 카탈로그 항목이 있는지 여부 테스트</span><span class="sxs-lookup"><span data-stu-id="27dca-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="27dca-109">이 명령은 지정된 Schema 항목이 있는지 여부를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="27dca-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="27dca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27dca-110">PARAMETERS</span></span>

### <span data-ttu-id="27dca-111">-Account</span><span class="sxs-lookup"><span data-stu-id="27dca-111">-Account</span></span>
<span data-ttu-id="27dca-112">Data Lake Analytics 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27dca-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="27dca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27dca-113">-DefaultProfile</span></span>
<span data-ttu-id="27dca-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="27dca-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27dca-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="27dca-115">-ItemType</span></span>
<span data-ttu-id="27dca-116">확인할 항목의 카탈로그 항목 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27dca-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="27dca-117">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="27dca-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="27dca-118">데이터베이스</span><span class="sxs-lookup"><span data-stu-id="27dca-118">Database</span></span>
- <span data-ttu-id="27dca-119">Schema</span><span class="sxs-lookup"><span data-stu-id="27dca-119">Schema</span></span>
- <span data-ttu-id="27dca-120">어셈블리</span><span class="sxs-lookup"><span data-stu-id="27dca-120">Assembly</span></span>
- <span data-ttu-id="27dca-121">표</span><span class="sxs-lookup"><span data-stu-id="27dca-121">Table</span></span>
- <span data-ttu-id="27dca-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="27dca-122">TablePartition</span></span>
- <span data-ttu-id="27dca-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="27dca-123">TableValuedFunction</span></span>
- <span data-ttu-id="27dca-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="27dca-124">TableStatistics</span></span>
- <span data-ttu-id="27dca-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="27dca-125">ExternalDataSource</span></span>
- <span data-ttu-id="27dca-126">보기</span><span class="sxs-lookup"><span data-stu-id="27dca-126">View</span></span>
- <span data-ttu-id="27dca-127">프로시저</span><span class="sxs-lookup"><span data-stu-id="27dca-127">Procedure</span></span>
- <span data-ttu-id="27dca-128">비밀</span><span class="sxs-lookup"><span data-stu-id="27dca-128">Secret</span></span>
- <span data-ttu-id="27dca-129">자격 증명</span><span class="sxs-lookup"><span data-stu-id="27dca-129">Credential</span></span>
- <span data-ttu-id="27dca-130">형식</span><span class="sxs-lookup"><span data-stu-id="27dca-130">Types</span></span>

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

### <span data-ttu-id="27dca-131">-Path</span><span class="sxs-lookup"><span data-stu-id="27dca-131">-Path</span></span>
<span data-ttu-id="27dca-132">인계할 항목의 경로 또는 나열할 항목의 부모 항목에 대한 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="27dca-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

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

### <span data-ttu-id="27dca-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27dca-133">CommonParameters</span></span>
<span data-ttu-id="27dca-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="27dca-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27dca-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="27dca-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27dca-136">입력</span><span class="sxs-lookup"><span data-stu-id="27dca-136">INPUTS</span></span>

### <span data-ttu-id="27dca-137">System.String</span><span class="sxs-lookup"><span data-stu-id="27dca-137">System.String</span></span>

### <span data-ttu-id="27dca-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="27dca-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="27dca-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="27dca-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="27dca-140">출력</span><span class="sxs-lookup"><span data-stu-id="27dca-140">OUTPUTS</span></span>

### <span data-ttu-id="27dca-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="27dca-141">System.Boolean</span></span>

## <span data-ttu-id="27dca-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="27dca-142">NOTES</span></span>

## <span data-ttu-id="27dca-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27dca-143">RELATED LINKS</span></span>

[<span data-ttu-id="27dca-144">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="27dca-144">Get-AzDataLakeAnalyticsCatalogItem</span></span>](./Get-AzDataLakeAnalyticsCatalogItem.md)


