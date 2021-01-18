---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: e4329c0d3ad4499af1174458ea3e0449672774a5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495059"
---
# <span data-ttu-id="2db61-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="2db61-101">Set-AzSearchService</span></span>

## <span data-ttu-id="2db61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2db61-102">SYNOPSIS</span></span>
<span data-ttu-id="2db61-103">Azure Search 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2db61-103">Update an Azure Search service.</span></span>

## <span data-ttu-id="2db61-104">구문</span><span class="sxs-lookup"><span data-stu-id="2db61-104">SYNTAX</span></span>

### <span data-ttu-id="2db61-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2db61-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2db61-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2db61-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2db61-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2db61-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2db61-108">설명</span><span class="sxs-lookup"><span data-stu-id="2db61-108">DESCRIPTION</span></span>
<span data-ttu-id="2db61-109">**Set-AzSearchService** cmdlet은 Azure Search 서비스를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="2db61-109">The **Set-AzSearchService** cmdlet modifies an Azure Search service.</span></span>

## <span data-ttu-id="2db61-110">예제</span><span class="sxs-lookup"><span data-stu-id="2db61-110">EXAMPLES</span></span>

### <span data-ttu-id="2db61-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2db61-111">Example 1</span></span>
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

<span data-ttu-id="2db61-112">이 예제에서는 Azure Search 서비스의 파티션 수 및 복제본 수를 2로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="2db61-112">The example changes partition count and replica count of the Azure Search service to 2.</span></span>

## <span data-ttu-id="2db61-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2db61-113">PARAMETERS</span></span>

### <span data-ttu-id="2db61-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2db61-114">-DefaultProfile</span></span>
<span data-ttu-id="2db61-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2db61-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2db61-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2db61-116">-InputObject</span></span>
<span data-ttu-id="2db61-117">Search 서비스 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2db61-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="2db61-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2db61-118">-Name</span></span>
<span data-ttu-id="2db61-119">검색 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2db61-119">Search Service name.</span></span>

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

### <span data-ttu-id="2db61-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="2db61-120">-PartitionCount</span></span>
<span data-ttu-id="2db61-121">Search 서비스 파티션 수.</span><span class="sxs-lookup"><span data-stu-id="2db61-121">Search Service partition count.</span></span>

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

### <span data-ttu-id="2db61-122">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="2db61-122">-ReplicaCount</span></span>
<span data-ttu-id="2db61-123">Search 서비스 복제본 수입니다.</span><span class="sxs-lookup"><span data-stu-id="2db61-123">Search Service replica count.</span></span>

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

### <span data-ttu-id="2db61-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2db61-124">-ResourceGroupName</span></span>
<span data-ttu-id="2db61-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2db61-125">Resource Group name.</span></span>

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

### <span data-ttu-id="2db61-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2db61-126">-ResourceId</span></span>
<span data-ttu-id="2db61-127">Search 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2db61-127">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="2db61-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2db61-128">-Confirm</span></span>
<span data-ttu-id="2db61-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2db61-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2db61-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2db61-130">-WhatIf</span></span>
<span data-ttu-id="2db61-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2db61-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2db61-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2db61-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2db61-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db61-133">CommonParameters</span></span>
<span data-ttu-id="2db61-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2db61-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db61-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2db61-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db61-136">입력</span><span class="sxs-lookup"><span data-stu-id="2db61-136">INPUTS</span></span>

### <span data-ttu-id="2db61-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="2db61-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="2db61-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2db61-138">System.String</span></span>

## <span data-ttu-id="2db61-139">출력</span><span class="sxs-lookup"><span data-stu-id="2db61-139">OUTPUTS</span></span>

### <span data-ttu-id="2db61-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="2db61-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="2db61-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2db61-141">NOTES</span></span>

## <span data-ttu-id="2db61-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2db61-142">RELATED LINKS</span></span>

[<span data-ttu-id="2db61-143">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="2db61-143">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="2db61-144">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="2db61-144">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="2db61-145">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="2db61-145">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)