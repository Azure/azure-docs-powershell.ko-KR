---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azhubrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
ms.openlocfilehash: 2261e3e0f9237985459dc69e06ba4f055dd86427
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962667"
---
# <span data-ttu-id="7a08d-101">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="7a08d-101">Reset-AzHubRouter</span></span>

## <span data-ttu-id="7a08d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a08d-102">SYNOPSIS</span></span>
<span data-ttu-id="7a08d-103">VirtualHub 리소스의 RoutingState를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a08d-103">Resets the RoutingState of a VirtualHub resource.</span></span>

## <span data-ttu-id="7a08d-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a08d-104">SYNTAX</span></span>

### <span data-ttu-id="7a08d-105">ByVirtualHubName(기본값)</span><span class="sxs-lookup"><span data-stu-id="7a08d-105">ByVirtualHubName (Default)</span></span>
```
Reset-AzHubRouter -ResourceGroupName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a08d-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="7a08d-106">ByVirtualHubResourceId</span></span>
```
Reset-AzHubRouter -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a08d-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="7a08d-107">ByVirtualHubObject</span></span>
```
Reset-AzHubRouter -InputObject <PSVirtualHub> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a08d-108">설명</span><span class="sxs-lookup"><span data-stu-id="7a08d-108">DESCRIPTION</span></span>
<span data-ttu-id="7a08d-109">가상 허브의 라우팅 상태가 프로비전되지 않은 경우만 기존 VirtualHub 리소스의 라우팅 상태를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a08d-109">Resets the Routing State of an existing VirtualHub resource only if the Routing State of the virtual hub is not Provisioned.</span></span>

## <span data-ttu-id="7a08d-110">예제</span><span class="sxs-lookup"><span data-stu-id="7a08d-110">EXAMPLES</span></span>

### <span data-ttu-id="7a08d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a08d-111">Example 1</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="7a08d-112">ResourceGroupName 및 ResourceName을 사용하여 가상 허브의 라우팅 상태를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a08d-112">Reset the routing state of the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="7a08d-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="7a08d-113">Example 2</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceId "/subscriptions/testSub/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub"
```

<span data-ttu-id="7a08d-114">ResourceId를 사용하여 가상 허브의 라우팅 상태를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a08d-114">Reset the routing state of the virtual hub using its ResourceId.</span></span>

### <span data-ttu-id="7a08d-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="7a08d-115">Example 3</span></span>

```powershell
PS C:\> Reset-AzHubRouter -InputObject $virtualHub
```

<span data-ttu-id="7a08d-116">입력 개체를 사용하여 가상 허브의 라우팅 상태를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a08d-116">Reset the routing state of the virtual hub using an input object.</span></span> <span data-ttu-id="7a08d-117">입력 개체는 PSVirtualHub 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7a08d-117">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="7a08d-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="7a08d-118">Example 4</span></span>

```powershell
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Reset-AzHubRouter
```

<span data-ttu-id="7a08d-119">기존 가상 허브 개체를 검색한 다음, Reset-AzHubRouter에 입력 개체로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a08d-119">An existing virtual hub object can be retrieved and then passed as input object to Reset-AzHubRouter.</span></span>

## <span data-ttu-id="7a08d-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7a08d-120">PARAMETERS</span></span>

### <span data-ttu-id="7a08d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a08d-121">-AsJob</span></span>
<span data-ttu-id="7a08d-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7a08d-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a08d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a08d-123">-DefaultProfile</span></span>
<span data-ttu-id="7a08d-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a08d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a08d-125">-Force</span><span class="sxs-lookup"><span data-stu-id="7a08d-125">-Force</span></span>
<span data-ttu-id="7a08d-126">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a08d-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7a08d-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a08d-127">-InputObject</span></span>
<span data-ttu-id="7a08d-128">수정할 가상 허브 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7a08d-128">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="7a08d-129">-Name</span><span class="sxs-lookup"><span data-stu-id="7a08d-129">-Name</span></span>
<span data-ttu-id="7a08d-130">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a08d-130">The resource name.</span></span>

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

### <span data-ttu-id="7a08d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a08d-131">-ResourceGroupName</span></span>
<span data-ttu-id="7a08d-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a08d-132">The resource group name.</span></span>

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

### <span data-ttu-id="7a08d-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a08d-133">-ResourceId</span></span>
<span data-ttu-id="7a08d-134">수정할 가상 허브의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7a08d-134">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="7a08d-135">-확인</span><span class="sxs-lookup"><span data-stu-id="7a08d-135">-Confirm</span></span>
<span data-ttu-id="7a08d-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a08d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a08d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a08d-137">-WhatIf</span></span>
<span data-ttu-id="7a08d-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7a08d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a08d-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a08d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a08d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a08d-140">CommonParameters</span></span>
<span data-ttu-id="7a08d-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a08d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a08d-142">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7a08d-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a08d-143">입력</span><span class="sxs-lookup"><span data-stu-id="7a08d-143">INPUTS</span></span>

### <span data-ttu-id="7a08d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="7a08d-144">System.String</span></span>

### <span data-ttu-id="7a08d-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7a08d-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="7a08d-146">출력</span><span class="sxs-lookup"><span data-stu-id="7a08d-146">OUTPUTS</span></span>

### <span data-ttu-id="7a08d-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7a08d-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="7a08d-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a08d-148">NOTES</span></span>

## <span data-ttu-id="7a08d-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a08d-149">RELATED LINKS</span></span>

[<span data-ttu-id="7a08d-150">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7a08d-150">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)
