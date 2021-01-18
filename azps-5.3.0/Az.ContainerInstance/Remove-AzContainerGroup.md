---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: 6f3b3006bfb51a90d5919c4cba2e2bc4295d4a76
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495860"
---
# <span data-ttu-id="7bf54-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="7bf54-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="7bf54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bf54-102">SYNOPSIS</span></span>
<span data-ttu-id="7bf54-103">컨테이너 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf54-103">Removes a container group.</span></span>

## <span data-ttu-id="7bf54-104">구문</span><span class="sxs-lookup"><span data-stu-id="7bf54-104">SYNTAX</span></span>

### <span data-ttu-id="7bf54-105">RemoveContainerGroupByResourceGroupAndNameParamSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7bf54-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bf54-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="7bf54-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bf54-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="7bf54-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bf54-108">설명</span><span class="sxs-lookup"><span data-stu-id="7bf54-108">DESCRIPTION</span></span>
<span data-ttu-id="7bf54-109">**Remove-AzContainerGroup** cmdlet은 컨테이너 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf54-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="7bf54-110">예제</span><span class="sxs-lookup"><span data-stu-id="7bf54-110">EXAMPLES</span></span>

### <span data-ttu-id="7bf54-111">예제 1: 컨테이너 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="7bf54-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="7bf54-112">이 명령은 지정된 컨테이너 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf54-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="7bf54-113">예제 2: 파이핑하여 컨테이너 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="7bf54-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="7bf54-114">이 명령은 파이핑하여 컨테이너 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf54-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="7bf54-115">예제 3: 리소스 ID로 컨테이너 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf54-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="7bf54-116">이 명령은 리소스 ID로 컨테이너 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf54-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="7bf54-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bf54-117">PARAMETERS</span></span>

### <span data-ttu-id="7bf54-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bf54-118">-DefaultProfile</span></span>
<span data-ttu-id="7bf54-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf54-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bf54-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bf54-120">-InputObject</span></span>
<span data-ttu-id="7bf54-121">제거할 컨테이너 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf54-121">The container group to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bf54-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7bf54-122">-Name</span></span>
<span data-ttu-id="7bf54-123">컨테이너 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf54-123">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bf54-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7bf54-124">-PassThru</span></span>
<span data-ttu-id="7bf54-125">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="7bf54-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bf54-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bf54-126">-ResourceGroupName</span></span>
<span data-ttu-id="7bf54-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf54-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bf54-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bf54-128">-ResourceId</span></span>
<span data-ttu-id="7bf54-129">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf54-129">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bf54-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bf54-130">-Confirm</span></span>
<span data-ttu-id="7bf54-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bf54-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bf54-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bf54-132">-WhatIf</span></span>
<span data-ttu-id="7bf54-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7bf54-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bf54-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf54-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bf54-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bf54-135">CommonParameters</span></span>
<span data-ttu-id="7bf54-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf54-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bf54-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7bf54-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bf54-138">입력</span><span class="sxs-lookup"><span data-stu-id="7bf54-138">INPUTS</span></span>

### <span data-ttu-id="7bf54-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="7bf54-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="7bf54-140">System.String</span><span class="sxs-lookup"><span data-stu-id="7bf54-140">System.String</span></span>

## <span data-ttu-id="7bf54-141">출력</span><span class="sxs-lookup"><span data-stu-id="7bf54-141">OUTPUTS</span></span>

### <span data-ttu-id="7bf54-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="7bf54-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="7bf54-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7bf54-143">NOTES</span></span>

## <span data-ttu-id="7bf54-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7bf54-144">RELATED LINKS</span></span>
