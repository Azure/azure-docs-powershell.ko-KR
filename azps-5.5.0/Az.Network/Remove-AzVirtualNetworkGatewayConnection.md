---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: f5ea9c291d23c6378170946ee6b605ec02742ed8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191700"
---
# <span data-ttu-id="29b1d-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="29b1d-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="29b1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29b1d-102">SYNOPSIS</span></span>
<span data-ttu-id="29b1d-103">Virtual Network 게이트웨이 연결을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="29b1d-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="29b1d-104">구문</span><span class="sxs-lookup"><span data-stu-id="29b1d-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29b1d-105">설명</span><span class="sxs-lookup"><span data-stu-id="29b1d-105">DESCRIPTION</span></span>
<span data-ttu-id="29b1d-106">Virtual Network 게이트웨이 연결은 Azure의 Virtual Network Gateway에 연결된 IPsec 터널(사이트-사이트 또는 Vnet-Vnet)을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="29b1d-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="29b1d-107">**Remove-AzVirtualNetworkGatewayConnection** cmdlet은 이름 및 리소스 그룹 이름을 기반으로 연결의 개체를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="29b1d-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="29b1d-108">예제</span><span class="sxs-lookup"><span data-stu-id="29b1d-108">EXAMPLES</span></span>

### <span data-ttu-id="29b1d-109">예제 1: Virtual Network 게이트웨이 연결 삭제</span><span class="sxs-lookup"><span data-stu-id="29b1d-109">Example 1: Delete a Virtual Network Gateway Connection</span></span>
```powershell
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="29b1d-110">리소스 그룹 "myRG"에서 "myTunnel"으로 Virtual Network 게이트웨이 연결의 개체를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="29b1d-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="29b1d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29b1d-111">PARAMETERS</span></span>

### <span data-ttu-id="29b1d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29b1d-112">-DefaultProfile</span></span>
<span data-ttu-id="29b1d-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29b1d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29b1d-114">-Force</span><span class="sxs-lookup"><span data-stu-id="29b1d-114">-Force</span></span>
<span data-ttu-id="29b1d-115">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="29b1d-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="29b1d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="29b1d-116">-Name</span></span>
<span data-ttu-id="29b1d-117">이 cmdlet에서 제거하는 가상 네트워크 게이트웨이 연결의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29b1d-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="29b1d-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29b1d-118">-PassThru</span></span>
<span data-ttu-id="29b1d-119">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="29b1d-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="29b1d-120">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29b1d-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="29b1d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29b1d-121">-ResourceGroupName</span></span>
<span data-ttu-id="29b1d-122">가상 네트워크 게이트웨이 연결을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29b1d-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="29b1d-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29b1d-123">-Confirm</span></span>
<span data-ttu-id="29b1d-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="29b1d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29b1d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29b1d-125">-WhatIf</span></span>
<span data-ttu-id="29b1d-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="29b1d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29b1d-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29b1d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29b1d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29b1d-128">CommonParameters</span></span>
<span data-ttu-id="29b1d-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="29b1d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29b1d-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="29b1d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29b1d-131">입력</span><span class="sxs-lookup"><span data-stu-id="29b1d-131">INPUTS</span></span>

### <span data-ttu-id="29b1d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="29b1d-132">System.String</span></span>

## <span data-ttu-id="29b1d-133">출력</span><span class="sxs-lookup"><span data-stu-id="29b1d-133">OUTPUTS</span></span>

### <span data-ttu-id="29b1d-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="29b1d-134">System.Boolean</span></span>

## <span data-ttu-id="29b1d-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="29b1d-135">NOTES</span></span>

## <span data-ttu-id="29b1d-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29b1d-136">RELATED LINKS</span></span>

[<span data-ttu-id="29b1d-137">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="29b1d-137">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="29b1d-138">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="29b1d-138">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="29b1d-139">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="29b1d-139">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
