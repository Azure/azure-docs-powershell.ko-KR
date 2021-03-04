---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: f4774ea7dec4ddd8df29c0a131fbaf080cbbba94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004491"
---
# <span data-ttu-id="e1125-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="e1125-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="e1125-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1125-102">SYNOPSIS</span></span>
<span data-ttu-id="e1125-103">컨테이너 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e1125-103">Removes a container group.</span></span>

## <span data-ttu-id="e1125-104">구문</span><span class="sxs-lookup"><span data-stu-id="e1125-104">SYNTAX</span></span>

### <span data-ttu-id="e1125-105">RemoveContainerGroupByResourceGroupAndNameParamSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e1125-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1125-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="e1125-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1125-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="e1125-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1125-108">설명</span><span class="sxs-lookup"><span data-stu-id="e1125-108">DESCRIPTION</span></span>
<span data-ttu-id="e1125-109">**Remove-AzContainerGroup** cmdlet은 컨테이너 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e1125-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="e1125-110">예제</span><span class="sxs-lookup"><span data-stu-id="e1125-110">EXAMPLES</span></span>

### <span data-ttu-id="e1125-111">예제 1: 컨테이너 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="e1125-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="e1125-112">이 명령은 지정된 컨테이너 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e1125-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="e1125-113">예제 2: 배관을 사용하여 컨테이너 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e1125-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="e1125-114">이 명령은 배관을 사용하여 컨테이너 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e1125-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="e1125-115">예제 3: 리소스 ID로 컨테이너 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e1125-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="e1125-116">이 명령은 리소스 ID로 컨테이너 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e1125-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="e1125-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e1125-117">PARAMETERS</span></span>

### <span data-ttu-id="e1125-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1125-118">-DefaultProfile</span></span>
<span data-ttu-id="e1125-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e1125-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1125-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1125-120">-InputObject</span></span>
<span data-ttu-id="e1125-121">제거할 컨테이너 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="e1125-121">The container group to remove.</span></span>

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

### <span data-ttu-id="e1125-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e1125-122">-Name</span></span>
<span data-ttu-id="e1125-123">컨테이너 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1125-123">The container group name.</span></span>

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

### <span data-ttu-id="e1125-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1125-124">-PassThru</span></span>
<span data-ttu-id="e1125-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e1125-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e1125-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1125-126">-ResourceGroupName</span></span>
<span data-ttu-id="e1125-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1125-127">The resource group name.</span></span>

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

### <span data-ttu-id="e1125-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1125-128">-ResourceId</span></span>
<span data-ttu-id="e1125-129">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e1125-129">The resource id.</span></span>

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

### <span data-ttu-id="e1125-130">-확인</span><span class="sxs-lookup"><span data-stu-id="e1125-130">-Confirm</span></span>
<span data-ttu-id="e1125-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1125-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1125-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1125-132">-WhatIf</span></span>
<span data-ttu-id="e1125-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e1125-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1125-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1125-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1125-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1125-135">CommonParameters</span></span>
<span data-ttu-id="e1125-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e1125-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1125-137">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e1125-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1125-138">입력</span><span class="sxs-lookup"><span data-stu-id="e1125-138">INPUTS</span></span>

### <span data-ttu-id="e1125-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="e1125-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="e1125-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e1125-140">System.String</span></span>

## <span data-ttu-id="e1125-141">출력</span><span class="sxs-lookup"><span data-stu-id="e1125-141">OUTPUTS</span></span>

### <span data-ttu-id="e1125-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="e1125-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="e1125-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e1125-143">NOTES</span></span>

## <span data-ttu-id="e1125-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1125-144">RELATED LINKS</span></span>
