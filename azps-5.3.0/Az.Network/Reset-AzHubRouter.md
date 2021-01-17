---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azhubrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
ms.openlocfilehash: 039d37f9d9dd7b5af026b7ce2a87113513949b67
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385134"
---
# <span data-ttu-id="c7a80-101">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="c7a80-101">Reset-AzHubRouter</span></span>

## <span data-ttu-id="c7a80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7a80-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a80-103">VirtualHub 리소스의 RoutingState를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c7a80-103">Resets the RoutingState of a VirtualHub resource.</span></span>

## <span data-ttu-id="c7a80-104">구문</span><span class="sxs-lookup"><span data-stu-id="c7a80-104">SYNTAX</span></span>

### <span data-ttu-id="c7a80-105">ByVirtualHubName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c7a80-105">ByVirtualHubName (Default)</span></span>
```
Reset-AzHubRouter -ResourceGroupName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7a80-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="c7a80-106">ByVirtualHubResourceId</span></span>
```
Reset-AzHubRouter -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7a80-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="c7a80-107">ByVirtualHubObject</span></span>
```
Reset-AzHubRouter -InputObject <PSVirtualHub> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7a80-108">설명</span><span class="sxs-lookup"><span data-stu-id="c7a80-108">DESCRIPTION</span></span>
<span data-ttu-id="c7a80-109">가상 허브의 라우팅 상태가 프로비전되지 않은 경우 기존 VirtualHub 리소스의 라우팅 상태를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c7a80-109">Resets the Routing State of an existing VirtualHub resource only if the Routing State of the virtual hub is not Provisioned.</span></span>

## <span data-ttu-id="c7a80-110">예제</span><span class="sxs-lookup"><span data-stu-id="c7a80-110">EXAMPLES</span></span>

### <span data-ttu-id="c7a80-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c7a80-111">Example 1</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="c7a80-112">ResourceGroupName 및 ResourceName을 사용하여 가상 허브의 라우팅 상태를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c7a80-112">Reset the routing state of the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="c7a80-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="c7a80-113">Example 2</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceId "/subscriptions/testSub/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub"
```

<span data-ttu-id="c7a80-114">ResourceId를 사용하여 가상 허브의 라우팅 상태를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c7a80-114">Reset the routing state of the virtual hub using its ResourceId.</span></span>

### <span data-ttu-id="c7a80-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="c7a80-115">Example 3</span></span>

```powershell
PS C:\> Reset-AzHubRouter -InputObject $virtualHub
```

<span data-ttu-id="c7a80-116">입력 개체를 사용하여 가상 허브의 라우팅 상태를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c7a80-116">Reset the routing state of the virtual hub using an input object.</span></span> <span data-ttu-id="c7a80-117">입력 개체는 PSVirtualHub 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="c7a80-117">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="c7a80-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="c7a80-118">Example 4</span></span>

```powershell
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Reset-AzHubRouter
```

<span data-ttu-id="c7a80-119">기존 가상 허브 개체를 검색한 다음, Reset-AzHubRouter에 입력 개체로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7a80-119">An existing virtual hub object can be retrieved and then passed as input object to Reset-AzHubRouter.</span></span>

## <span data-ttu-id="c7a80-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7a80-120">PARAMETERS</span></span>

### <span data-ttu-id="c7a80-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7a80-121">-AsJob</span></span>
<span data-ttu-id="c7a80-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c7a80-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7a80-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a80-123">-DefaultProfile</span></span>
<span data-ttu-id="c7a80-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7a80-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7a80-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c7a80-125">-Force</span></span>
<span data-ttu-id="c7a80-126">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7a80-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c7a80-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7a80-127">-InputObject</span></span>
<span data-ttu-id="c7a80-128">수정할 가상 허브 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c7a80-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a80-129">-Name</span><span class="sxs-lookup"><span data-stu-id="c7a80-129">-Name</span></span>
<span data-ttu-id="c7a80-130">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7a80-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a80-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7a80-131">-ResourceGroupName</span></span>
<span data-ttu-id="c7a80-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7a80-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a80-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7a80-133">-ResourceId</span></span>
<span data-ttu-id="c7a80-134">수정할 가상 허브의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c7a80-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a80-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7a80-135">-Confirm</span></span>
<span data-ttu-id="c7a80-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7a80-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7a80-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7a80-137">-WhatIf</span></span>
<span data-ttu-id="c7a80-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c7a80-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7a80-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7a80-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7a80-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a80-140">CommonParameters</span></span>
<span data-ttu-id="c7a80-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c7a80-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a80-142">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c7a80-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a80-143">입력</span><span class="sxs-lookup"><span data-stu-id="c7a80-143">INPUTS</span></span>

### <span data-ttu-id="c7a80-144">System.String</span><span class="sxs-lookup"><span data-stu-id="c7a80-144">System.String</span></span>

### <span data-ttu-id="c7a80-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c7a80-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="c7a80-146">출력</span><span class="sxs-lookup"><span data-stu-id="c7a80-146">OUTPUTS</span></span>

### <span data-ttu-id="c7a80-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c7a80-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="c7a80-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c7a80-148">NOTES</span></span>

## <span data-ttu-id="c7a80-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7a80-149">RELATED LINKS</span></span>

[<span data-ttu-id="c7a80-150">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c7a80-150">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)
