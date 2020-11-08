---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azhubrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
ms.openlocfilehash: 039d37f9d9dd7b5af026b7ce2a87113513949b67
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218818"
---
# <span data-ttu-id="e3240-101">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="e3240-101">Reset-AzHubRouter</span></span>

## <span data-ttu-id="e3240-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3240-102">SYNOPSIS</span></span>
<span data-ttu-id="e3240-103">VirtualHub 리소스의 RoutingState를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3240-103">Resets the RoutingState of a VirtualHub resource.</span></span>

## <span data-ttu-id="e3240-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e3240-104">SYNTAX</span></span>

### <span data-ttu-id="e3240-105">ByVirtualHubName (기본값)</span><span class="sxs-lookup"><span data-stu-id="e3240-105">ByVirtualHubName (Default)</span></span>
```
Reset-AzHubRouter -ResourceGroupName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3240-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="e3240-106">ByVirtualHubResourceId</span></span>
```
Reset-AzHubRouter -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3240-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="e3240-107">ByVirtualHubObject</span></span>
```
Reset-AzHubRouter -InputObject <PSVirtualHub> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3240-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e3240-108">DESCRIPTION</span></span>
<span data-ttu-id="e3240-109">가상 허브의 라우팅 상태가 프로 비전 되지 않은 경우에만 기존 VirtualHub 리소스의 라우팅 상태를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3240-109">Resets the Routing State of an existing VirtualHub resource only if the Routing State of the virtual hub is not Provisioned.</span></span>

## <span data-ttu-id="e3240-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e3240-110">EXAMPLES</span></span>

### <span data-ttu-id="e3240-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e3240-111">Example 1</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="e3240-112">ResourceGroupName 및 Context.resourcename을 사용 하 여 가상 허브의 라우팅 상태를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3240-112">Reset the routing state of the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="e3240-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e3240-113">Example 2</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceId "/subscriptions/testSub/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub"
```

<span data-ttu-id="e3240-114">ResourceId를 사용 하 여 가상 허브의 라우팅 상태를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3240-114">Reset the routing state of the virtual hub using its ResourceId.</span></span>

### <span data-ttu-id="e3240-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="e3240-115">Example 3</span></span>

```powershell
PS C:\> Reset-AzHubRouter -InputObject $virtualHub
```

<span data-ttu-id="e3240-116">입력 개체를 사용 하 여 가상 허브의 라우팅 상태를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3240-116">Reset the routing state of the virtual hub using an input object.</span></span> <span data-ttu-id="e3240-117">입력 개체는 PSVirtualHub 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e3240-117">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="e3240-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="e3240-118">Example 4</span></span>

```powershell
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Reset-AzHubRouter
```

<span data-ttu-id="e3240-119">기존 가상 허브 개체를 검색 한 다음 입력 개체로 전달 하 여 AzHubRouter를 다시 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3240-119">An existing virtual hub object can be retrieved and then passed as input object to Reset-AzHubRouter.</span></span>

## <span data-ttu-id="e3240-120">변수</span><span class="sxs-lookup"><span data-stu-id="e3240-120">PARAMETERS</span></span>

### <span data-ttu-id="e3240-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3240-121">-AsJob</span></span>
<span data-ttu-id="e3240-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e3240-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3240-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3240-123">-DefaultProfile</span></span>
<span data-ttu-id="e3240-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3240-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3240-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e3240-125">-Force</span></span>
<span data-ttu-id="e3240-126">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="e3240-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e3240-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3240-127">-InputObject</span></span>
<span data-ttu-id="e3240-128">수정할 가상 허브 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e3240-128">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="e3240-129">-이름</span><span class="sxs-lookup"><span data-stu-id="e3240-129">-Name</span></span>
<span data-ttu-id="e3240-130">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3240-130">The resource name.</span></span>

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

### <span data-ttu-id="e3240-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3240-131">-ResourceGroupName</span></span>
<span data-ttu-id="e3240-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3240-132">The resource group name.</span></span>

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

### <span data-ttu-id="e3240-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3240-133">-ResourceId</span></span>
<span data-ttu-id="e3240-134">수정할 가상 허브의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e3240-134">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="e3240-135">-확인</span><span class="sxs-lookup"><span data-stu-id="e3240-135">-Confirm</span></span>
<span data-ttu-id="e3240-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3240-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3240-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3240-137">-WhatIf</span></span>
<span data-ttu-id="e3240-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e3240-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3240-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3240-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3240-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3240-140">CommonParameters</span></span>
<span data-ttu-id="e3240-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3240-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3240-142">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3240-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3240-143">입력</span><span class="sxs-lookup"><span data-stu-id="e3240-143">INPUTS</span></span>

### <span data-ttu-id="e3240-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e3240-144">System.String</span></span>

### <span data-ttu-id="e3240-145">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e3240-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="e3240-146">출력</span><span class="sxs-lookup"><span data-stu-id="e3240-146">OUTPUTS</span></span>

### <span data-ttu-id="e3240-147">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e3240-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="e3240-148">상속자</span><span class="sxs-lookup"><span data-stu-id="e3240-148">NOTES</span></span>

## <span data-ttu-id="e3240-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3240-149">RELATED LINKS</span></span>

[<span data-ttu-id="e3240-150">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e3240-150">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)
