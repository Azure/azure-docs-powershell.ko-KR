---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: c4841678a1e1f318da36b506cc56e586244c233f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006032"
---
# <span data-ttu-id="92fdd-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="92fdd-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="92fdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92fdd-102">SYNOPSIS</span></span>
<span data-ttu-id="92fdd-103">Virtual Network Gateway 삭제</span><span class="sxs-lookup"><span data-stu-id="92fdd-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="92fdd-104">구문</span><span class="sxs-lookup"><span data-stu-id="92fdd-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92fdd-105">설명</span><span class="sxs-lookup"><span data-stu-id="92fdd-105">DESCRIPTION</span></span>
<span data-ttu-id="92fdd-106">Virtual Network Gateway는 Azure에서 게이트웨이를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="92fdd-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="92fdd-107">**Get-AzVirtualNetworkGateway** cmdlet은 이름 및 리소스 그룹 이름을 기반으로 Azure에서 게이트웨이의 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="92fdd-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="92fdd-108">예제</span><span class="sxs-lookup"><span data-stu-id="92fdd-108">EXAMPLES</span></span>

### <span data-ttu-id="92fdd-109">예제 1: 가상 네트워크 게이트웨이 삭제</span><span class="sxs-lookup"><span data-stu-id="92fdd-109">Example 1: Delete a Virtual Network Gateway</span></span>
```powershell
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="92fdd-110">리소스 그룹 "myRG" 참고 내에서 "myGateway"라는 이름으로 Virtual Network Gateway의 개체를 삭제합니다. 먼저 **Remove-AzVirtualNetworkGatewayConnection** cmdlet을 사용하여 Virtual Network Gateway에 대한 모든 연결을 삭제해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="92fdd-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="92fdd-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="92fdd-111">PARAMETERS</span></span>

### <span data-ttu-id="92fdd-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92fdd-112">-AsJob</span></span>
<span data-ttu-id="92fdd-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="92fdd-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92fdd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92fdd-114">-DefaultProfile</span></span>
<span data-ttu-id="92fdd-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92fdd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92fdd-116">-Force</span><span class="sxs-lookup"><span data-stu-id="92fdd-116">-Force</span></span>
<span data-ttu-id="92fdd-117">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="92fdd-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="92fdd-118">-Name</span><span class="sxs-lookup"><span data-stu-id="92fdd-118">-Name</span></span>
<span data-ttu-id="92fdd-119">이 cmdlet이 제거하는 가상 네트워크 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="92fdd-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="92fdd-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92fdd-120">-PassThru</span></span>
<span data-ttu-id="92fdd-121">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="92fdd-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="92fdd-122">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92fdd-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="92fdd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92fdd-123">-ResourceGroupName</span></span>
<span data-ttu-id="92fdd-124">가상 네트워크 게이트웨이를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="92fdd-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="92fdd-125">-확인</span><span class="sxs-lookup"><span data-stu-id="92fdd-125">-Confirm</span></span>
<span data-ttu-id="92fdd-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="92fdd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92fdd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92fdd-127">-WhatIf</span></span>
<span data-ttu-id="92fdd-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="92fdd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92fdd-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92fdd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92fdd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92fdd-130">CommonParameters</span></span>
<span data-ttu-id="92fdd-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="92fdd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92fdd-132">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="92fdd-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92fdd-133">입력</span><span class="sxs-lookup"><span data-stu-id="92fdd-133">INPUTS</span></span>

### <span data-ttu-id="92fdd-134">System.String</span><span class="sxs-lookup"><span data-stu-id="92fdd-134">System.String</span></span>

## <span data-ttu-id="92fdd-135">출력</span><span class="sxs-lookup"><span data-stu-id="92fdd-135">OUTPUTS</span></span>

### <span data-ttu-id="92fdd-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="92fdd-136">System.Boolean</span></span>

## <span data-ttu-id="92fdd-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="92fdd-137">NOTES</span></span>

## <span data-ttu-id="92fdd-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92fdd-138">RELATED LINKS</span></span>

[<span data-ttu-id="92fdd-139">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="92fdd-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="92fdd-140">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="92fdd-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="92fdd-141">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="92fdd-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="92fdd-142">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="92fdd-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="92fdd-143">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="92fdd-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
