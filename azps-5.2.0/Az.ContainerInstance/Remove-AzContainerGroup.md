---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: 6f3b3006bfb51a90d5919c4cba2e2bc4295d4a76
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335529"
---
# <span data-ttu-id="8dc4e-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="8dc4e-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="8dc4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dc4e-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc4e-103">컨테이너 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-103">Removes a container group.</span></span>

## <span data-ttu-id="8dc4e-104">구문</span><span class="sxs-lookup"><span data-stu-id="8dc4e-104">SYNTAX</span></span>

### <span data-ttu-id="8dc4e-105">RemoveContainerGroupByResourceGroupAndNameParamSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8dc4e-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dc4e-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="8dc4e-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dc4e-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="8dc4e-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dc4e-108">설명</span><span class="sxs-lookup"><span data-stu-id="8dc4e-108">DESCRIPTION</span></span>
<span data-ttu-id="8dc4e-109">**Remove-AzContainerGroup** cmdlet은 컨테이너 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="8dc4e-110">예제</span><span class="sxs-lookup"><span data-stu-id="8dc4e-110">EXAMPLES</span></span>

### <span data-ttu-id="8dc4e-111">예제 1: 컨테이너 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="8dc4e-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="8dc4e-112">이 명령은 지정된 컨테이너 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="8dc4e-113">예제 2: 파이핑하여 컨테이너 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="8dc4e-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="8dc4e-114">이 명령은 파이핑하여 컨테이너 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="8dc4e-115">예제 3: 리소스 ID로 컨테이너 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="8dc4e-116">이 명령은 리소스 ID로 컨테이너 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="8dc4e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dc4e-117">PARAMETERS</span></span>

### <span data-ttu-id="8dc4e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc4e-118">-DefaultProfile</span></span>
<span data-ttu-id="8dc4e-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dc4e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dc4e-120">-InputObject</span></span>
<span data-ttu-id="8dc4e-121">제거할 컨테이너 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-121">The container group to remove.</span></span>

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

### <span data-ttu-id="8dc4e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8dc4e-122">-Name</span></span>
<span data-ttu-id="8dc4e-123">컨테이너 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-123">The container group name.</span></span>

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

### <span data-ttu-id="8dc4e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8dc4e-124">-PassThru</span></span>
<span data-ttu-id="8dc4e-125">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="8dc4e-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8dc4e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dc4e-126">-ResourceGroupName</span></span>
<span data-ttu-id="8dc4e-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-127">The resource group name.</span></span>

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

### <span data-ttu-id="8dc4e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dc4e-128">-ResourceId</span></span>
<span data-ttu-id="8dc4e-129">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-129">The resource id.</span></span>

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

### <span data-ttu-id="8dc4e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dc4e-130">-Confirm</span></span>
<span data-ttu-id="8dc4e-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dc4e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dc4e-132">-WhatIf</span></span>
<span data-ttu-id="8dc4e-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8dc4e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dc4e-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dc4e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc4e-135">CommonParameters</span></span>
<span data-ttu-id="8dc4e-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc4e-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8dc4e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc4e-138">입력</span><span class="sxs-lookup"><span data-stu-id="8dc4e-138">INPUTS</span></span>

### <span data-ttu-id="8dc4e-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="8dc4e-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="8dc4e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8dc4e-140">System.String</span></span>

## <span data-ttu-id="8dc4e-141">출력</span><span class="sxs-lookup"><span data-stu-id="8dc4e-141">OUTPUTS</span></span>

### <span data-ttu-id="8dc4e-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="8dc4e-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="8dc4e-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8dc4e-143">NOTES</span></span>

## <span data-ttu-id="8dc4e-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8dc4e-144">RELATED LINKS</span></span>
