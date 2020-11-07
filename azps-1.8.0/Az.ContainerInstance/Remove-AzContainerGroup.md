---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: fb9b2c23618d731f6f107f755ca6ef41dfe439ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701188"
---
# <span data-ttu-id="7c6b1-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="7c6b1-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="7c6b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c6b1-102">SYNOPSIS</span></span>
<span data-ttu-id="7c6b1-103">컨테이너 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-103">Removes a container group.</span></span>

## <span data-ttu-id="7c6b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c6b1-104">SYNTAX</span></span>

### <span data-ttu-id="7c6b1-105">RemoveContainerGroupByResourceGroupAndNameParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7c6b1-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c6b1-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="7c6b1-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c6b1-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="7c6b1-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c6b1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7c6b1-108">DESCRIPTION</span></span>
<span data-ttu-id="7c6b1-109">**제거-AzContainerGroup** cmdlet은 컨테이너 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="7c6b1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7c6b1-110">EXAMPLES</span></span>

### <span data-ttu-id="7c6b1-111">예제 1: 컨테이너 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="7c6b1-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="7c6b1-112">이 명령은 지정 된 컨테이너 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="7c6b1-113">예제 2: 파이프를 기준으로 컨테이너 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="7c6b1-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="7c6b1-114">이 명령은 파이프를 기준으로 컨테이너 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="7c6b1-115">예제 3: 리소스 Id를 기준으로 컨테이너 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="7c6b1-116">이 명령은 리소스 Id를 기준으로 컨테이너 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="7c6b1-117">변수</span><span class="sxs-lookup"><span data-stu-id="7c6b1-117">PARAMETERS</span></span>

### <span data-ttu-id="7c6b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c6b1-118">-DefaultProfile</span></span>
<span data-ttu-id="7c6b1-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c6b1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c6b1-120">-InputObject</span></span>
<span data-ttu-id="7c6b1-121">제거할 컨테이너 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-121">The container group to remove.</span></span>

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

### <span data-ttu-id="7c6b1-122">-이름</span><span class="sxs-lookup"><span data-stu-id="7c6b1-122">-Name</span></span>
<span data-ttu-id="7c6b1-123">컨테이너 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-123">The container group name.</span></span>

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

### <span data-ttu-id="7c6b1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c6b1-124">-PassThru</span></span>
<span data-ttu-id="7c6b1-125">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="7c6b1-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7c6b1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c6b1-126">-ResourceGroupName</span></span>
<span data-ttu-id="7c6b1-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-127">The resource group name.</span></span>

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

### <span data-ttu-id="7c6b1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c6b1-128">-ResourceId</span></span>
<span data-ttu-id="7c6b1-129">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-129">The resource id.</span></span>

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

### <span data-ttu-id="7c6b1-130">-확인</span><span class="sxs-lookup"><span data-stu-id="7c6b1-130">-Confirm</span></span>
<span data-ttu-id="7c6b1-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c6b1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c6b1-132">-WhatIf</span></span>
<span data-ttu-id="7c6b1-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c6b1-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c6b1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c6b1-135">CommonParameters</span></span>
<span data-ttu-id="7c6b1-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c6b1-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c6b1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c6b1-138">입력</span><span class="sxs-lookup"><span data-stu-id="7c6b1-138">INPUTS</span></span>

### <span data-ttu-id="7c6b1-139">ContainerInstance. PSContainerGroup/.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="7c6b1-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c6b1-140">System.String</span></span>

## <span data-ttu-id="7c6b1-141">출력</span><span class="sxs-lookup"><span data-stu-id="7c6b1-141">OUTPUTS</span></span>

### <span data-ttu-id="7c6b1-142">ContainerInstance. PSContainerGroup/.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="7c6b1-143">상속자</span><span class="sxs-lookup"><span data-stu-id="7c6b1-143">NOTES</span></span>

## <span data-ttu-id="7c6b1-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c6b1-144">RELATED LINKS</span></span>