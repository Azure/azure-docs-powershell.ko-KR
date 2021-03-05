---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: 8fadba097b602bd84c8eb36d75f5b7a331e2280b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972544"
---
# <span data-ttu-id="0e37f-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0e37f-101">Set-AzSearchService</span></span>

## <span data-ttu-id="0e37f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e37f-102">SYNOPSIS</span></span>
<span data-ttu-id="0e37f-103">Azure Cognitive Search 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0e37f-103">Update an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="0e37f-104">구문</span><span class="sxs-lookup"><span data-stu-id="0e37f-104">SYNTAX</span></span>

### <span data-ttu-id="0e37f-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0e37f-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>]
 [-IPRuleList <PSIpRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e37f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e37f-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e37f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e37f-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e37f-108">설명</span><span class="sxs-lookup"><span data-stu-id="0e37f-108">DESCRIPTION</span></span>
<span data-ttu-id="0e37f-109">**Set-AzSearchService** cmdlet은 Azure Cognitive Search 서비스를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e37f-109">The **Set-AzSearchService** cmdlet modifies an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="0e37f-110">예제</span><span class="sxs-lookup"><span data-stu-id="0e37f-110">EXAMPLES</span></span>

### <span data-ttu-id="0e37f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0e37f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 2
PartitionCount    : 2
HostingMode       : Default
Tags              :
```

<span data-ttu-id="0e37f-112">이 예제에서는 Azure Cognitive Search 서비스의 파티션 수 및 복제본 수를 2로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="0e37f-112">The example changes partition count and replica count of the Azure Cognitive Search service to 2.</span></span>

## <span data-ttu-id="0e37f-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0e37f-113">PARAMETERS</span></span>

### <span data-ttu-id="0e37f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e37f-114">-DefaultProfile</span></span>
<span data-ttu-id="0e37f-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e37f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e37f-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="0e37f-116">-IdentityType</span></span>
<span data-ttu-id="0e37f-117">(선택 사항) Azure Cognitive Search 서비스 ID(없음/SystemAssigned)</span><span class="sxs-lookup"><span data-stu-id="0e37f-117">(Optional) Azure Cognitive Search Service Identity (None/SystemAssigned)</span></span>

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

### <span data-ttu-id="0e37f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e37f-118">-InputObject</span></span>
<span data-ttu-id="0e37f-119">서비스 입력 개체를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="0e37f-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e37f-120">-IPRuleList</span><span class="sxs-lookup"><span data-stu-id="0e37f-120">-IPRuleList</span></span>
<span data-ttu-id="0e37f-121">(선택 사항) Azure Cognitive Search Service IP 규칙</span><span class="sxs-lookup"><span data-stu-id="0e37f-121">(Optional) Azure Cognitive Search Service IP rules</span></span>

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

### <span data-ttu-id="0e37f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0e37f-122">-Name</span></span>
<span data-ttu-id="0e37f-123">서비스 이름을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="0e37f-123">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e37f-124">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="0e37f-124">-PartitionCount</span></span>
<span data-ttu-id="0e37f-125">서비스 파티션 수를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="0e37f-125">Search Service partition count.</span></span>

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

### <span data-ttu-id="0e37f-126">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="0e37f-126">-PublicNetworkAccess</span></span>
<span data-ttu-id="0e37f-127">(선택 사항) Azure Cognitive Search Service 공용 네트워크 액세스(사용 가능/비활성화)</span><span class="sxs-lookup"><span data-stu-id="0e37f-127">(Optional) Azure Cognitive Search Service public network access (Enabled/Disabled)</span></span>

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

### <span data-ttu-id="0e37f-128">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="0e37f-128">-ReplicaCount</span></span>
<span data-ttu-id="0e37f-129">Service 복제본 수를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="0e37f-129">Search Service replica count.</span></span>

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

### <span data-ttu-id="0e37f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e37f-130">-ResourceGroupName</span></span>
<span data-ttu-id="0e37f-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e37f-131">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e37f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e37f-132">-ResourceId</span></span>
<span data-ttu-id="0e37f-133">서비스 리소스 ID를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="0e37f-133">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e37f-134">-확인</span><span class="sxs-lookup"><span data-stu-id="0e37f-134">-Confirm</span></span>
<span data-ttu-id="0e37f-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e37f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e37f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e37f-136">-WhatIf</span></span>
<span data-ttu-id="0e37f-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0e37f-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e37f-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e37f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e37f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e37f-139">CommonParameters</span></span>
<span data-ttu-id="0e37f-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0e37f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e37f-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e37f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e37f-142">입력</span><span class="sxs-lookup"><span data-stu-id="0e37f-142">INPUTS</span></span>

### <span data-ttu-id="0e37f-143">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="0e37f-143">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="0e37f-144">System.String</span><span class="sxs-lookup"><span data-stu-id="0e37f-144">System.String</span></span>

## <span data-ttu-id="0e37f-145">출력</span><span class="sxs-lookup"><span data-stu-id="0e37f-145">OUTPUTS</span></span>

### <span data-ttu-id="0e37f-146">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="0e37f-146">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="0e37f-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0e37f-147">NOTES</span></span>

## <span data-ttu-id="0e37f-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e37f-148">RELATED LINKS</span></span>

[<span data-ttu-id="0e37f-149">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0e37f-149">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="0e37f-150">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0e37f-150">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="0e37f-151">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="0e37f-151">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)