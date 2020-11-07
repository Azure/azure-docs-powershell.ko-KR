---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 249ef7ae66436d4bf82b3b038aa8b1201f68110e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703123"
---
# <span data-ttu-id="9927e-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="9927e-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="9927e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9927e-102">SYNOPSIS</span></span>
<span data-ttu-id="9927e-103">카탈로그 항목이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9927e-103">Checks for the existence of a catalog item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9927e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9927e-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9927e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9927e-105">DESCRIPTION</span></span>
<span data-ttu-id="9927e-106">**AzureRmDataLakeAnalyticsCatalogItem** Cmdlet은 Azure Data Lake Analytics 카탈로그 항목이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="9927e-106">The **Test-AzureRmDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="9927e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9927e-107">EXAMPLES</span></span>

### <span data-ttu-id="9927e-108">예제 1: 카탈로그 항목이 있는지 테스트</span><span class="sxs-lookup"><span data-stu-id="9927e-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="9927e-109">이 명령은 지정 된 스키마 항목이 있는지 여부를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9927e-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="9927e-110">변수</span><span class="sxs-lookup"><span data-stu-id="9927e-110">PARAMETERS</span></span>

### <span data-ttu-id="9927e-111">-계정</span><span class="sxs-lookup"><span data-stu-id="9927e-111">-Account</span></span>
<span data-ttu-id="9927e-112">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9927e-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="9927e-113">-ItemType</span><span class="sxs-lookup"><span data-stu-id="9927e-113">-ItemType</span></span>
<span data-ttu-id="9927e-114">확인할 항목의 카탈로그 항목 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9927e-114">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="9927e-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9927e-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9927e-116">데이터</span><span class="sxs-lookup"><span data-stu-id="9927e-116">Database</span></span>
- <span data-ttu-id="9927e-117">스키마</span><span class="sxs-lookup"><span data-stu-id="9927e-117">Schema</span></span>
- <span data-ttu-id="9927e-118">어셈블리가</span><span class="sxs-lookup"><span data-stu-id="9927e-118">Assembly</span></span>
- <span data-ttu-id="9927e-119">테이블로</span><span class="sxs-lookup"><span data-stu-id="9927e-119">Table</span></span>
- <span data-ttu-id="9927e-120">TablePartition</span><span class="sxs-lookup"><span data-stu-id="9927e-120">TablePartition</span></span>
- <span data-ttu-id="9927e-121">Table의 Edfunction</span><span class="sxs-lookup"><span data-stu-id="9927e-121">TableValuedFunction</span></span>
- <span data-ttu-id="9927e-122">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="9927e-122">TableStatistics</span></span>
- <span data-ttu-id="9927e-123">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="9927e-123">ExternalDataSource</span></span>
- <span data-ttu-id="9927e-124">보려고</span><span class="sxs-lookup"><span data-stu-id="9927e-124">View</span></span>
- <span data-ttu-id="9927e-125">절차</span><span class="sxs-lookup"><span data-stu-id="9927e-125">Procedure</span></span>
- <span data-ttu-id="9927e-126">기밀</span><span class="sxs-lookup"><span data-stu-id="9927e-126">Secret</span></span>
- <span data-ttu-id="9927e-127">자격 증명</span><span class="sxs-lookup"><span data-stu-id="9927e-127">Credential</span></span>
- <span data-ttu-id="9927e-128">형식</span><span class="sxs-lookup"><span data-stu-id="9927e-128">Types</span></span>

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

### <span data-ttu-id="9927e-129">-Path</span><span class="sxs-lookup"><span data-stu-id="9927e-129">-Path</span></span>
<span data-ttu-id="9927e-130">가져올 항목의 경로 또는 나열할 항목의 상위 항목에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9927e-130">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

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

### <span data-ttu-id="9927e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9927e-131">-DefaultProfile</span></span>
<span data-ttu-id="9927e-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9927e-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9927e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9927e-133">CommonParameters</span></span>
<span data-ttu-id="9927e-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9927e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9927e-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9927e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9927e-136">입력</span><span class="sxs-lookup"><span data-stu-id="9927e-136">INPUTS</span></span>

## <span data-ttu-id="9927e-137">출력</span><span class="sxs-lookup"><span data-stu-id="9927e-137">OUTPUTS</span></span>

### <span data-ttu-id="9927e-138">부울</span><span class="sxs-lookup"><span data-stu-id="9927e-138">bool</span></span>
<span data-ttu-id="9927e-139">지정 된 카탈로그 항목이 있는지 여부를 나타내는 True 또는 false입니다.</span><span class="sxs-lookup"><span data-stu-id="9927e-139">True or false indicating if the specified catalog item exists or not.</span></span>

## <span data-ttu-id="9927e-140">상속자</span><span class="sxs-lookup"><span data-stu-id="9927e-140">NOTES</span></span>

## <span data-ttu-id="9927e-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9927e-141">RELATED LINKS</span></span>

[<span data-ttu-id="9927e-142">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="9927e-142">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Get-AzureRmDataLakeAnalyticsCatalogItem.md)


