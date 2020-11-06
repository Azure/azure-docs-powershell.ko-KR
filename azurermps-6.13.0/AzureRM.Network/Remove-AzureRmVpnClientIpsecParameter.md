---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: b88fff9775665f5b20f403d46f11bba89dc61220
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529465"
---
# <span data-ttu-id="9a50b-101">Remove-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="9a50b-101">Remove-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="9a50b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a50b-102">SYNOPSIS</span></span>
<span data-ttu-id="9a50b-103">가상 네트워크 게이트웨이 리소스에 설정 되어 있는 Vpn 사용자 지정 ipsec 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50b-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a50b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a50b-104">SYNTAX</span></span>

### <span data-ttu-id="9a50b-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="9a50b-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a50b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9a50b-106">ByFactoryObject</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a50b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9a50b-107">ByResourceId</span></span>
```
Remove-AzureRmVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a50b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9a50b-108">DESCRIPTION</span></span>
<span data-ttu-id="9a50b-109">가상 네트워크 게이트웨이는 Azure에서 게이트웨이를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9a50b-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="9a50b-110">**AzureRmVpnClientIpsecParameter** Cmdlet은 가상 네트워크 게이트웨이에서 설정 된 vpn 사용자 지정 ipsec 매개 변수를 제거 하 고,이는 VirtualNetworkGateway 이름 및 리소스 그룹 이름에 기반 하 여 vpn 게이트웨이에서 기본 vpn ipsec 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50b-110">The **Remove-AzureRmVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="9a50b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9a50b-111">EXAMPLES</span></span>

### <span data-ttu-id="9a50b-112">1: 가상 네트워크 게이트웨이에 설정 된 vpn ipsec 매개 변수 집합을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50b-112">1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```
PS C:\> $delete = Remove-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="9a50b-113">리소스 그룹 "Mygateway" 내에서 이름 "myGateway"를 사용 하 여 가상 네트워크 게이트웨이에 설정 된 vpn 사용자 지정 ipsec 매개 변수를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50b-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="9a50b-114">이 명령은 제거의 성공 또는 실패 여부를 표시 하는 bool 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50b-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="9a50b-115">참고:이로 인해 가상 네트워크 게이트웨이에서 기본 vpn ipsec 정책이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a50b-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="9a50b-116">변수</span><span class="sxs-lookup"><span data-stu-id="9a50b-116">PARAMETERS</span></span>

### <span data-ttu-id="9a50b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a50b-117">-DefaultProfile</span></span>
<span data-ttu-id="9a50b-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a50b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a50b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a50b-119">-InputObject</span></span>
<span data-ttu-id="9a50b-120">가상 네트워크 gateaway 개체</span><span class="sxs-lookup"><span data-stu-id="9a50b-120">The virtual network gateaway object</span></span>

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

### <span data-ttu-id="9a50b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a50b-121">-ResourceGroupName</span></span>
<span data-ttu-id="9a50b-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a50b-122">The resource group name.</span></span>

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

### <span data-ttu-id="9a50b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a50b-123">-ResourceId</span></span>
<span data-ttu-id="9a50b-124">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9a50b-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="9a50b-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="9a50b-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="9a50b-126">가상 네트워크 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a50b-126">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="9a50b-127">-확인</span><span class="sxs-lookup"><span data-stu-id="9a50b-127">-Confirm</span></span>
<span data-ttu-id="9a50b-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a50b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a50b-129">-WhatIf</span></span>
<span data-ttu-id="9a50b-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9a50b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a50b-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a50b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a50b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a50b-132">CommonParameters</span></span>
<span data-ttu-id="9a50b-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a50b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a50b-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a50b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a50b-135">입력</span><span class="sxs-lookup"><span data-stu-id="9a50b-135">INPUTS</span></span>

### <span data-ttu-id="9a50b-136">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9a50b-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="9a50b-137">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9a50b-137">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="9a50b-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9a50b-138">System.String</span></span>

## <span data-ttu-id="9a50b-139">출력</span><span class="sxs-lookup"><span data-stu-id="9a50b-139">OUTPUTS</span></span>

### <span data-ttu-id="9a50b-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9a50b-140">System.Boolean</span></span>

## <span data-ttu-id="9a50b-141">상속자</span><span class="sxs-lookup"><span data-stu-id="9a50b-141">NOTES</span></span>

## <span data-ttu-id="9a50b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a50b-142">RELATED LINKS</span></span>
