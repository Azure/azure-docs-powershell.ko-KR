---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: ba1f9372ffcf4a756debc02258a10b935581f377
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192697"
---
# <span data-ttu-id="9185f-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="9185f-101">New-AzSearchService</span></span>

## <span data-ttu-id="9185f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9185f-102">SYNOPSIS</span></span>
<span data-ttu-id="9185f-103">Azure Cognitive Search 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9185f-103">Creates an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="9185f-104">구문</span><span class="sxs-lookup"><span data-stu-id="9185f-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9185f-105">설명</span><span class="sxs-lookup"><span data-stu-id="9185f-105">DESCRIPTION</span></span>
<span data-ttu-id="9185f-106">**New-AzSearchService** cmdlet은 지정된 매개 변수를 사용하여 Azure Cognitive Search 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9185f-106">The **New-AzSearchService** cmdlet creates an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="9185f-107">예제</span><span class="sxs-lookup"><span data-stu-id="9185f-107">EXAMPLES</span></span>

### <span data-ttu-id="9185f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9185f-108">Example 1</span></span>
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

<span data-ttu-id="9185f-109">이 명령은 Azure Cognitive Search 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9185f-109">The command creates an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="9185f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9185f-110">PARAMETERS</span></span>

### <span data-ttu-id="9185f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9185f-111">-DefaultProfile</span></span>
<span data-ttu-id="9185f-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9185f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9185f-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="9185f-113">-HostingMode</span></span>
<span data-ttu-id="9185f-114">Azure Cognitive Search 서비스 호스팅 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="9185f-114">Azure Cognitive Search Service hosting mode.</span></span>

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

### <span data-ttu-id="9185f-115">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="9185f-115">-IdentityType</span></span>
<span data-ttu-id="9185f-116">(선택 사항) Azure Cognitive Search 서비스 ID(None/SystemAssigned)</span><span class="sxs-lookup"><span data-stu-id="9185f-116">(Optional) Azure Cognitive Search Service Identity (None/SystemAssigned)</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSIdentityType]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9185f-117">-IPRuleList</span><span class="sxs-lookup"><span data-stu-id="9185f-117">-IPRuleList</span></span>
<span data-ttu-id="9185f-118">(선택 사항) Azure Cognitive Search 서비스 IP 규칙</span><span class="sxs-lookup"><span data-stu-id="9185f-118">(Optional) Azure Cognitive Search Service IP rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9185f-119">-Location</span><span class="sxs-lookup"><span data-stu-id="9185f-119">-Location</span></span>
<span data-ttu-id="9185f-120">Azure Cognitive Search 서비스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9185f-120">Azure Cognitive Search Service location.</span></span>

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

### <span data-ttu-id="9185f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9185f-121">-Name</span></span>
<span data-ttu-id="9185f-122">Azure Cognitive Search 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9185f-122">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="9185f-123">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="9185f-123">-PartitionCount</span></span>
<span data-ttu-id="9185f-124">Azure Cognitive Search 서비스 파티션 수입니다.</span><span class="sxs-lookup"><span data-stu-id="9185f-124">Azure Cognitive Search Service partition count.</span></span>

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

### <span data-ttu-id="9185f-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="9185f-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="9185f-126">(선택 사항) Azure Cognitive Search Service 공용 네트워크 액세스(사용/비활성화)</span><span class="sxs-lookup"><span data-stu-id="9185f-126">(Optional) Azure Cognitive Search Service public network access (Enabled/Disabled)</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSPublicNetworkAccess]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9185f-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="9185f-127">-ReplicaCount</span></span>
<span data-ttu-id="9185f-128">Azure Cognitive Search 서비스 복제본 수입니다.</span><span class="sxs-lookup"><span data-stu-id="9185f-128">Azure Cognitive Search Service replica count.</span></span>

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

### <span data-ttu-id="9185f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9185f-129">-ResourceGroupName</span></span>
<span data-ttu-id="9185f-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9185f-130">Resource Group name.</span></span>

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

### <span data-ttu-id="9185f-131">-Sku</span><span class="sxs-lookup"><span data-stu-id="9185f-131">-Sku</span></span>
<span data-ttu-id="9185f-132">Azure Cognitive Search 서비스 SKU입니다.</span><span class="sxs-lookup"><span data-stu-id="9185f-132">Azure Cognitive Search Service Sku.</span></span>

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

### <span data-ttu-id="9185f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9185f-133">-Confirm</span></span>
<span data-ttu-id="9185f-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9185f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9185f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9185f-135">-WhatIf</span></span>
<span data-ttu-id="9185f-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9185f-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9185f-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9185f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9185f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9185f-138">CommonParameters</span></span>
<span data-ttu-id="9185f-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9185f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9185f-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9185f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9185f-141">입력</span><span class="sxs-lookup"><span data-stu-id="9185f-141">INPUTS</span></span>

### <span data-ttu-id="9185f-142">없음</span><span class="sxs-lookup"><span data-stu-id="9185f-142">None</span></span>

## <span data-ttu-id="9185f-143">출력</span><span class="sxs-lookup"><span data-stu-id="9185f-143">OUTPUTS</span></span>

### <span data-ttu-id="9185f-144">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="9185f-144">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="9185f-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9185f-145">NOTES</span></span>

## <span data-ttu-id="9185f-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9185f-146">RELATED LINKS</span></span>

[<span data-ttu-id="9185f-147">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="9185f-147">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="9185f-148">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="9185f-148">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="9185f-149">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="9185f-149">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)