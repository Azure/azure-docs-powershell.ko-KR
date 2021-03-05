---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
ms.openlocfilehash: 6def67720ee11a2057267845ef458d0759aec589
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005936"
---
# <span data-ttu-id="e1378-101">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e1378-101">Remove-AzVirtualRouter</span></span>

## <span data-ttu-id="e1378-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1378-102">SYNOPSIS</span></span>
<span data-ttu-id="e1378-103">Azure VirtualRouter를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e1378-103">Deletes an Azure VirtualRouter.</span></span>

## <span data-ttu-id="e1378-104">구문</span><span class="sxs-lookup"><span data-stu-id="e1378-104">SYNTAX</span></span>

### <span data-ttu-id="e1378-105">VirtualRouterNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e1378-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1378-106">VirtualRouterInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1378-106">VirtualRouterInputObjectParameterSet</span></span>
```
Remove-AzVirtualRouter -InputObject <PSVirtualRouter> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1378-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1378-107">VirtualRouterResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouter -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1378-108">설명</span><span class="sxs-lookup"><span data-stu-id="e1378-108">DESCRIPTION</span></span>
<span data-ttu-id="e1378-109">**Remove-AzVirtualRouter** cmdlet은 Azure VirtualRouter를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e1378-109">The **Remove-AzVirtualRouter** cmdlet deletes an Azure VirtualRouter</span></span>

## <span data-ttu-id="e1378-110">예제</span><span class="sxs-lookup"><span data-stu-id="e1378-110">EXAMPLES</span></span>

### <span data-ttu-id="e1378-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e1378-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="e1378-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="e1378-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Remove-AzVirtualRouter -ResourceId $virtualRouterId
```

### <span data-ttu-id="e1378-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="e1378-113">Example 3</span></span>
```powershell
$virtualRouter = Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
Remove-AzVirtualRouter -InputObject $virtualRouter
```

## <span data-ttu-id="e1378-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e1378-114">PARAMETERS</span></span>

### <span data-ttu-id="e1378-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1378-115">-AsJob</span></span>
<span data-ttu-id="e1378-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e1378-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1378-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1378-117">-DefaultProfile</span></span>
<span data-ttu-id="e1378-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e1378-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1378-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e1378-119">-Force</span></span>
<span data-ttu-id="e1378-120">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1378-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e1378-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1378-121">-InputObject</span></span>
<span data-ttu-id="e1378-122">가상 라우터 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e1378-122">The virtual router input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouter
Parameter Sets: VirtualRouterInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1378-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1378-123">-PassThru</span></span>
<span data-ttu-id="e1378-124">이 작업이 수행되는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e1378-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="e1378-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1378-125">-ResourceGroupName</span></span>
<span data-ttu-id="e1378-126">가상 라우터의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1378-126">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1378-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1378-127">-ResourceId</span></span>
<span data-ttu-id="e1378-128">가상 라우터 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e1378-128">The virtual router resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1378-129">-라우터 이름</span><span class="sxs-lookup"><span data-stu-id="e1378-129">-RouterName</span></span>
<span data-ttu-id="e1378-130">가상 라우터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1378-130">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1378-131">-확인</span><span class="sxs-lookup"><span data-stu-id="e1378-131">-Confirm</span></span>
<span data-ttu-id="e1378-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1378-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1378-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1378-133">-WhatIf</span></span>
<span data-ttu-id="e1378-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e1378-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1378-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1378-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1378-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1378-136">CommonParameters</span></span>
<span data-ttu-id="e1378-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e1378-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1378-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1378-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1378-139">입력</span><span class="sxs-lookup"><span data-stu-id="e1378-139">INPUTS</span></span>

### <span data-ttu-id="e1378-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e1378-140">System.String</span></span>

### <span data-ttu-id="e1378-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e1378-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="e1378-142">출력</span><span class="sxs-lookup"><span data-stu-id="e1378-142">OUTPUTS</span></span>

### <span data-ttu-id="e1378-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e1378-143">System.Boolean</span></span>

## <span data-ttu-id="e1378-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e1378-144">NOTES</span></span>

## <span data-ttu-id="e1378-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1378-145">RELATED LINKS</span></span>
