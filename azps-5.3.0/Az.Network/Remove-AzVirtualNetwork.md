---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
ms.openlocfilehash: 777e03a570f3915d6e0ebe4cbb5c84f9c1824120
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385253"
---
# <span data-ttu-id="e1127-101">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e1127-101">Remove-AzVirtualNetwork</span></span>

## <span data-ttu-id="e1127-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1127-102">SYNOPSIS</span></span>
<span data-ttu-id="e1127-103">가상 네트워크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e1127-103">Removes a virtual network.</span></span>

## <span data-ttu-id="e1127-104">구문</span><span class="sxs-lookup"><span data-stu-id="e1127-104">SYNTAX</span></span>

```
Remove-AzVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1127-105">설명</span><span class="sxs-lookup"><span data-stu-id="e1127-105">DESCRIPTION</span></span>
<span data-ttu-id="e1127-106">**Remove-AzVirtualNetwork** cmdlet은 Azure 가상 네트워크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e1127-106">The **Remove-AzVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="e1127-107">예제</span><span class="sxs-lookup"><span data-stu-id="e1127-107">EXAMPLES</span></span>

### <span data-ttu-id="e1127-108">1: 가상 네트워크 만들기 및 삭제</span><span class="sxs-lookup"><span data-stu-id="e1127-108">1: Create and delete a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="e1127-109">이 예제에서는 리소스 그룹에 가상 네트워크를 만든 다음 즉시 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e1127-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="e1127-110">가상 네트워크를 삭제하는 경우 프롬프트를 표시하지 않습니다. -Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1127-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="e1127-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1127-111">PARAMETERS</span></span>

### <span data-ttu-id="e1127-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1127-112">-AsJob</span></span>
<span data-ttu-id="e1127-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e1127-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1127-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1127-114">-DefaultProfile</span></span>
<span data-ttu-id="e1127-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e1127-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1127-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e1127-116">-Force</span></span>
<span data-ttu-id="e1127-117">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e1127-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e1127-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e1127-118">-Name</span></span>
<span data-ttu-id="e1127-119">이 cmdlet이 제거하는 가상 네트워크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1127-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1127-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1127-120">-PassThru</span></span>
<span data-ttu-id="e1127-121">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e1127-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e1127-122">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1127-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e1127-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1127-123">-ResourceGroupName</span></span>
<span data-ttu-id="e1127-124">이 cmdlet에서 제거하는 가상 네트워크를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1127-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1127-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1127-125">-Confirm</span></span>
<span data-ttu-id="e1127-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1127-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1127-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1127-127">-WhatIf</span></span>
<span data-ttu-id="e1127-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e1127-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1127-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1127-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1127-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1127-130">CommonParameters</span></span>
<span data-ttu-id="e1127-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e1127-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1127-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e1127-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1127-133">입력</span><span class="sxs-lookup"><span data-stu-id="e1127-133">INPUTS</span></span>

### <span data-ttu-id="e1127-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e1127-134">System.String</span></span>

## <span data-ttu-id="e1127-135">출력</span><span class="sxs-lookup"><span data-stu-id="e1127-135">OUTPUTS</span></span>

### <span data-ttu-id="e1127-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e1127-136">System.Boolean</span></span>

## <span data-ttu-id="e1127-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e1127-137">NOTES</span></span>

## <span data-ttu-id="e1127-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1127-138">RELATED LINKS</span></span>

[<span data-ttu-id="e1127-139">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e1127-139">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="e1127-140">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e1127-140">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="e1127-141">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e1127-141">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


