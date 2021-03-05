---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 3a598001421bf237f93a63fb4f45d069bf9404ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006011"
---
# <span data-ttu-id="c34ed-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c34ed-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="c34ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c34ed-102">SYNOPSIS</span></span>
<span data-ttu-id="c34ed-103">Virtual Network Gateway 연결을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="c34ed-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="c34ed-104">구문</span><span class="sxs-lookup"><span data-stu-id="c34ed-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c34ed-105">설명</span><span class="sxs-lookup"><span data-stu-id="c34ed-105">DESCRIPTION</span></span>
<span data-ttu-id="c34ed-106">Virtual Network Gateway 연결은 Azure의 Virtual Network Gateway에 연결된 IPsec 터널(사이트 대 사이트 또는 Vnet-Vnet)을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c34ed-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="c34ed-107">**Remove-AzVirtualNetworkGatewayConnection** cmdlet은 이름 및 리소스 그룹 이름을 기반으로 연결 개체를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="c34ed-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="c34ed-108">예제</span><span class="sxs-lookup"><span data-stu-id="c34ed-108">EXAMPLES</span></span>

### <span data-ttu-id="c34ed-109">예제 1: 가상 네트워크 게이트웨이 연결 삭제</span><span class="sxs-lookup"><span data-stu-id="c34ed-109">Example 1: Delete a Virtual Network Gateway Connection</span></span>
```powershell
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="c34ed-110">리소스 그룹 "myRG" 내에서 "myTunnel"으로 Virtual Network Gateway 연결의 개체를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="c34ed-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="c34ed-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c34ed-111">PARAMETERS</span></span>

### <span data-ttu-id="c34ed-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c34ed-112">-DefaultProfile</span></span>
<span data-ttu-id="c34ed-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c34ed-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c34ed-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c34ed-114">-Force</span></span>
<span data-ttu-id="c34ed-115">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c34ed-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c34ed-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c34ed-116">-Name</span></span>
<span data-ttu-id="c34ed-117">이 cmdlet이 제거한 가상 네트워크 게이트웨이 연결의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c34ed-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c34ed-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c34ed-118">-PassThru</span></span>
<span data-ttu-id="c34ed-119">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c34ed-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c34ed-120">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c34ed-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c34ed-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c34ed-121">-ResourceGroupName</span></span>
<span data-ttu-id="c34ed-122">가상 네트워크 게이트웨이 연결을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c34ed-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="c34ed-123">-확인</span><span class="sxs-lookup"><span data-stu-id="c34ed-123">-Confirm</span></span>
<span data-ttu-id="c34ed-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c34ed-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c34ed-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c34ed-125">-WhatIf</span></span>
<span data-ttu-id="c34ed-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c34ed-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c34ed-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c34ed-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c34ed-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c34ed-128">CommonParameters</span></span>
<span data-ttu-id="c34ed-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c34ed-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c34ed-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c34ed-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c34ed-131">입력</span><span class="sxs-lookup"><span data-stu-id="c34ed-131">INPUTS</span></span>

### <span data-ttu-id="c34ed-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c34ed-132">System.String</span></span>

## <span data-ttu-id="c34ed-133">출력</span><span class="sxs-lookup"><span data-stu-id="c34ed-133">OUTPUTS</span></span>

### <span data-ttu-id="c34ed-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c34ed-134">System.Boolean</span></span>

## <span data-ttu-id="c34ed-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c34ed-135">NOTES</span></span>

## <span data-ttu-id="c34ed-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c34ed-136">RELATED LINKS</span></span>

[<span data-ttu-id="c34ed-137">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c34ed-137">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="c34ed-138">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c34ed-138">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="c34ed-139">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c34ed-139">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
