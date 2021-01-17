---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 3fa4a8c1868673b4ce9bc630a70e02bb92a55fda
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491638"
---
# <span data-ttu-id="b2a70-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b2a70-101">New-AzSearchService</span></span>

## <span data-ttu-id="b2a70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2a70-102">SYNOPSIS</span></span>
<span data-ttu-id="b2a70-103">Azure Search 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2a70-103">Creates an Azure Search service.</span></span>

## <span data-ttu-id="b2a70-104">구문</span><span class="sxs-lookup"><span data-stu-id="b2a70-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2a70-105">설명</span><span class="sxs-lookup"><span data-stu-id="b2a70-105">DESCRIPTION</span></span>
<span data-ttu-id="b2a70-106">**New-AzSearchService** cmdlet은 지정된 매개 변수를 사용하여 Azure Search 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2a70-106">The **New-AzSearchService** cmdlet creates an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="b2a70-107">예제</span><span class="sxs-lookup"><span data-stu-id="b2a70-107">EXAMPLES</span></span>

### <span data-ttu-id="b2a70-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b2a70-108">Example 1</span></span>
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

<span data-ttu-id="b2a70-109">이 명령은 Azure Search 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2a70-109">The command creates an Azure Search service.</span></span>

## <span data-ttu-id="b2a70-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2a70-110">PARAMETERS</span></span>

### <span data-ttu-id="b2a70-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2a70-111">-DefaultProfile</span></span>
<span data-ttu-id="b2a70-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2a70-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2a70-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="b2a70-113">-HostingMode</span></span>
<span data-ttu-id="b2a70-114">Search 서비스 호스팅 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="b2a70-114">Search Service hosting mode.</span></span>

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

### <span data-ttu-id="b2a70-115">-Location</span><span class="sxs-lookup"><span data-stu-id="b2a70-115">-Location</span></span>
<span data-ttu-id="b2a70-116">Search 서비스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b2a70-116">Search Service location.</span></span>

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

### <span data-ttu-id="b2a70-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b2a70-117">-Name</span></span>
<span data-ttu-id="b2a70-118">검색 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2a70-118">Search Service name.</span></span>

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

### <span data-ttu-id="b2a70-119">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="b2a70-119">-PartitionCount</span></span>
<span data-ttu-id="b2a70-120">Search 서비스 파티션 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b2a70-120">Search Service partition count.</span></span>

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

### <span data-ttu-id="b2a70-121">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="b2a70-121">-ReplicaCount</span></span>
<span data-ttu-id="b2a70-122">Search 서비스 복제본 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b2a70-122">Search Service replica count.</span></span>

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

### <span data-ttu-id="b2a70-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2a70-123">-ResourceGroupName</span></span>
<span data-ttu-id="b2a70-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2a70-124">Resource Group name.</span></span>

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

### <span data-ttu-id="b2a70-125">-Sku</span><span class="sxs-lookup"><span data-stu-id="b2a70-125">-Sku</span></span>
<span data-ttu-id="b2a70-126">Search 서비스 SKU입니다.</span><span class="sxs-lookup"><span data-stu-id="b2a70-126">Search Service Sku.</span></span>

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

### <span data-ttu-id="b2a70-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2a70-127">-Confirm</span></span>
<span data-ttu-id="b2a70-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2a70-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2a70-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2a70-129">-WhatIf</span></span>
<span data-ttu-id="b2a70-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b2a70-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2a70-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2a70-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2a70-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2a70-132">CommonParameters</span></span>
<span data-ttu-id="b2a70-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b2a70-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2a70-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b2a70-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2a70-135">입력</span><span class="sxs-lookup"><span data-stu-id="b2a70-135">INPUTS</span></span>

### <span data-ttu-id="b2a70-136">없음</span><span class="sxs-lookup"><span data-stu-id="b2a70-136">None</span></span>

## <span data-ttu-id="b2a70-137">출력</span><span class="sxs-lookup"><span data-stu-id="b2a70-137">OUTPUTS</span></span>

### <span data-ttu-id="b2a70-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="b2a70-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="b2a70-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b2a70-139">NOTES</span></span>

## <span data-ttu-id="b2a70-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2a70-140">RELATED LINKS</span></span>

[<span data-ttu-id="b2a70-141">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b2a70-141">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="b2a70-142">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b2a70-142">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="b2a70-143">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="b2a70-143">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)