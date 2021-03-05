---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 513fbe1d973a75dbc1c967610d95882202bab147
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960272"
---
# <span data-ttu-id="054aa-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="054aa-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="054aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="054aa-102">SYNOPSIS</span></span>
<span data-ttu-id="054aa-103">Virtual Network Gateway 리소스에서 Vpn 사용자 지정 ipsec 정책 집합을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="054aa-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="054aa-104">구문</span><span class="sxs-lookup"><span data-stu-id="054aa-104">SYNTAX</span></span>

### <span data-ttu-id="054aa-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="054aa-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="054aa-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="054aa-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="054aa-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="054aa-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="054aa-108">설명</span><span class="sxs-lookup"><span data-stu-id="054aa-108">DESCRIPTION</span></span>
<span data-ttu-id="054aa-109">Virtual Network Gateway는 Azure에서 게이트웨이를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="054aa-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="054aa-110">**Remove-AzVpnClientIpsecParameter** cmdlet은 Virtual Network Gateway에 설정된 VPN 사용자 지정 ipsec 매개 변수를 제거하며, 이 매개 변수는 전달된 VirtualNetworkGateway 이름 및 리소스 그룹 이름을 기반으로 VPN 게이트웨이에서 기본 VPN ipsec 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="054aa-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="054aa-111">예제</span><span class="sxs-lookup"><span data-stu-id="054aa-111">EXAMPLES</span></span>

### <span data-ttu-id="054aa-112">예제 1: Virtual Network Gateway에 설정된 VPN ipsec 매개 변수 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="054aa-112">Example 1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```powershell
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="054aa-113">리소스 그룹 "myRG"에서 "myGateway"라는 이름으로 Virtual Network Gateway에 설정된 VPN 사용자 지정 ipsec 매개 변수를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="054aa-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="054aa-114">이 명령은 제거가 성공했거나 실패한 경우를 보여 주며 부적 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="054aa-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="054aa-115">참고: 가상 네트워크 게이트웨이에서 기본 vpn ipsec 정책을 설정하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="054aa-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="054aa-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="054aa-116">PARAMETERS</span></span>

### <span data-ttu-id="054aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="054aa-117">-DefaultProfile</span></span>
<span data-ttu-id="054aa-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="054aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="054aa-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="054aa-119">-InputObject</span></span>
<span data-ttu-id="054aa-120">가상 네트워크 게이트웨이 개체</span><span class="sxs-lookup"><span data-stu-id="054aa-120">The virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="054aa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="054aa-121">-ResourceGroupName</span></span>
<span data-ttu-id="054aa-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="054aa-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054aa-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="054aa-123">-ResourceId</span></span>
<span data-ttu-id="054aa-124">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="054aa-124">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="054aa-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="054aa-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="054aa-126">가상 네트워크 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="054aa-126">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="054aa-127">-확인</span><span class="sxs-lookup"><span data-stu-id="054aa-127">-Confirm</span></span>
<span data-ttu-id="054aa-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="054aa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="054aa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="054aa-129">-WhatIf</span></span>
<span data-ttu-id="054aa-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="054aa-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="054aa-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="054aa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="054aa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="054aa-132">CommonParameters</span></span>
<span data-ttu-id="054aa-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="054aa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="054aa-134">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="054aa-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="054aa-135">입력</span><span class="sxs-lookup"><span data-stu-id="054aa-135">INPUTS</span></span>

### <span data-ttu-id="054aa-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="054aa-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="054aa-137">System.String</span><span class="sxs-lookup"><span data-stu-id="054aa-137">System.String</span></span>

## <span data-ttu-id="054aa-138">출력</span><span class="sxs-lookup"><span data-stu-id="054aa-138">OUTPUTS</span></span>

### <span data-ttu-id="054aa-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="054aa-139">System.Boolean</span></span>

## <span data-ttu-id="054aa-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="054aa-140">NOTES</span></span>

## <span data-ttu-id="054aa-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="054aa-141">RELATED LINKS</span></span>

[<span data-ttu-id="054aa-142">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="054aa-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="054aa-143">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="054aa-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="054aa-144">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="054aa-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
