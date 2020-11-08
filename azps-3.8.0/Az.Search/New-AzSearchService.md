---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 3fa4a8c1868673b4ce9bc630a70e02bb92a55fda
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042321"
---
# <span data-ttu-id="f26d5-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="f26d5-101">New-AzSearchService</span></span>

## <span data-ttu-id="f26d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f26d5-102">SYNOPSIS</span></span>
<span data-ttu-id="f26d5-103">Azure Search 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f26d5-103">Creates an Azure Search service.</span></span>

## <span data-ttu-id="f26d5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f26d5-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f26d5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f26d5-105">DESCRIPTION</span></span>
<span data-ttu-id="f26d5-106">**AzSearchService** cmdlet은 지정 된 매개 변수를 사용 하 여 Azure Search 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f26d5-106">The **New-AzSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="f26d5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f26d5-107">EXAMPLES</span></span>

### <span data-ttu-id="f26d5-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f26d5-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Tags              :
```

<span data-ttu-id="f26d5-109">명령에서 Azure Search 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f26d5-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="f26d5-110">변수</span><span class="sxs-lookup"><span data-stu-id="f26d5-110">PARAMETERS</span></span>

### <span data-ttu-id="f26d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f26d5-111">-DefaultProfile</span></span>
<span data-ttu-id="f26d5-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f26d5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f26d5-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="f26d5-113">-HostingMode</span></span>
<span data-ttu-id="f26d5-114">검색 서비스 호스팅 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="f26d5-114">Search Service hosting mode.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSHostingMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, HighDensity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f26d5-115">-위치</span><span class="sxs-lookup"><span data-stu-id="f26d5-115">-Location</span></span>
<span data-ttu-id="f26d5-116">검색 서비스 위치.</span><span class="sxs-lookup"><span data-stu-id="f26d5-116">Search Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f26d5-117">-이름</span><span class="sxs-lookup"><span data-stu-id="f26d5-117">-Name</span></span>
<span data-ttu-id="f26d5-118">검색 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f26d5-118">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f26d5-119">-파티션 수</span><span class="sxs-lookup"><span data-stu-id="f26d5-119">-PartitionCount</span></span>
<span data-ttu-id="f26d5-120">검색 서비스 파티션 수입니다.</span><span class="sxs-lookup"><span data-stu-id="f26d5-120">Search Service partition count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f26d5-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="f26d5-121">-ReplicaCount</span></span>
<span data-ttu-id="f26d5-122">검색 서비스 복제본 수입니다.</span><span class="sxs-lookup"><span data-stu-id="f26d5-122">Search Service replica count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f26d5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f26d5-123">-ResourceGroupName</span></span>
<span data-ttu-id="f26d5-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f26d5-124">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f26d5-125">-Sku</span><span class="sxs-lookup"><span data-stu-id="f26d5-125">-Sku</span></span>
<span data-ttu-id="f26d5-126">Search Service Sku.</span><span class="sxs-lookup"><span data-stu-id="f26d5-126">Search Service Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard, Standard2, Standard3

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f26d5-127">-확인</span><span class="sxs-lookup"><span data-stu-id="f26d5-127">-Confirm</span></span>
<span data-ttu-id="f26d5-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f26d5-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f26d5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f26d5-129">-WhatIf</span></span>
<span data-ttu-id="f26d5-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f26d5-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f26d5-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f26d5-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f26d5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f26d5-132">CommonParameters</span></span>
<span data-ttu-id="f26d5-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f26d5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f26d5-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f26d5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f26d5-135">입력</span><span class="sxs-lookup"><span data-stu-id="f26d5-135">INPUTS</span></span>

### <span data-ttu-id="f26d5-136">않아야</span><span class="sxs-lookup"><span data-stu-id="f26d5-136">None</span></span>

## <span data-ttu-id="f26d5-137">출력</span><span class="sxs-lookup"><span data-stu-id="f26d5-137">OUTPUTS</span></span>

### <span data-ttu-id="f26d5-138">Microsoft. Azure. PSSearchService를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="f26d5-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="f26d5-139">상속자</span><span class="sxs-lookup"><span data-stu-id="f26d5-139">NOTES</span></span>

## <span data-ttu-id="f26d5-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f26d5-140">RELATED LINKS</span></span>

[<span data-ttu-id="f26d5-141">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="f26d5-141">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="f26d5-142">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="f26d5-142">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="f26d5-143">제거-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="f26d5-143">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)