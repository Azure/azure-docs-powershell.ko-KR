---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 77dbd80f03cb26adbb68e320d761200cd9ee7bc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530195"
---
# <span data-ttu-id="3f307-101">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f307-101">New-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="3f307-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f307-102">SYNOPSIS</span></span>
<span data-ttu-id="3f307-103">부하 분산 장치에 대 한 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f307-103">Creates a front-end IP configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f307-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3f307-104">SYNTAX</span></span>

### <span data-ttu-id="3f307-105">SetByResourceSubnet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3f307-105">SetByResourceSubnet (Default)</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f307-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="3f307-106">SetByResourceIdSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f307-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3f307-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f307-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3f307-108">SetByResourcePublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f307-109">설명은</span><span class="sxs-lookup"><span data-stu-id="3f307-109">DESCRIPTION</span></span>
<span data-ttu-id="3f307-110">**AzureRmLoadBalancerFrontendIpConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f307-110">The **New-AzureRmLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="3f307-111">예제의</span><span class="sxs-lookup"><span data-stu-id="3f307-111">EXAMPLES</span></span>

### <span data-ttu-id="3f307-112">예제 1: 부하 분산 장치에 대 한 프런트 엔드 IP 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="3f307-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="3f307-113">첫 번째 명령은 MyResourceGroup 이라는 리소스 그룹에 MyPublicIP 라는 동적 공용 IP 주소를 만든 다음이를 $publicip 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f307-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="3f307-114">두 번째 명령은 $publicip에서 공용 IP 주소를 사용 하 여 FrontendIpConfig01 라는 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f307-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="3f307-115">변수</span><span class="sxs-lookup"><span data-stu-id="3f307-115">PARAMETERS</span></span>

### <span data-ttu-id="3f307-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f307-116">-DefaultProfile</span></span>
<span data-ttu-id="3f307-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f307-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f307-118">-이름</span><span class="sxs-lookup"><span data-stu-id="3f307-118">-Name</span></span>
<span data-ttu-id="3f307-119">이 cmdlet이 만드는 프런트 엔드 IP 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f307-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f307-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="3f307-120">-PrivateIpAddress</span></span>
<span data-ttu-id="3f307-121">부하 분산 장치의 개인 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f307-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="3f307-122">*서브넷* 매개 변수도 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f307-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f307-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3f307-123">-PublicIpAddress</span></span>
<span data-ttu-id="3f307-124">프런트 엔드 IP 구성과 연결 되는 **PublicIpAddress** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f307-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f307-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="3f307-125">-PublicIpAddressId</span></span>
<span data-ttu-id="3f307-126">프런트 엔드 IP 구성과 연결할 **PublicIpAddress** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f307-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f307-127">-서브넷</span><span class="sxs-lookup"><span data-stu-id="3f307-127">-Subnet</span></span>
<span data-ttu-id="3f307-128">프런트 엔드 IP 구성을 만들 **서브넷** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f307-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f307-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3f307-129">-SubnetId</span></span>
<span data-ttu-id="3f307-130">프런트 엔드 IP 구성을 만들 서브넷의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f307-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f307-131">-Zone</span><span class="sxs-lookup"><span data-stu-id="3f307-131">-Zone</span></span>
<span data-ttu-id="3f307-132">리소스에 대해 할당 된 IP를 나타내는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3f307-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f307-133">-확인</span><span class="sxs-lookup"><span data-stu-id="3f307-133">-Confirm</span></span>
<span data-ttu-id="3f307-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f307-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f307-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f307-135">-WhatIf</span></span>
<span data-ttu-id="3f307-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3f307-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f307-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f307-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f307-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f307-138">CommonParameters</span></span>
<span data-ttu-id="3f307-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f307-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f307-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f307-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f307-141">입력</span><span class="sxs-lookup"><span data-stu-id="3f307-141">INPUTS</span></span>

### <span data-ttu-id="3f307-142">System.webserver. 목록 \` 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="3f307-142">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="3f307-143">출력</span><span class="sxs-lookup"><span data-stu-id="3f307-143">OUTPUTS</span></span>

### <span data-ttu-id="3f307-144">PSFrontendIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="3f307-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="3f307-145">상속자</span><span class="sxs-lookup"><span data-stu-id="3f307-145">NOTES</span></span>

## <span data-ttu-id="3f307-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f307-146">RELATED LINKS</span></span>

[<span data-ttu-id="3f307-147">추가-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f307-147">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="3f307-148">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f307-148">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="3f307-149">새로운 AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="3f307-149">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="3f307-150">제거-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f307-150">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="3f307-151">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f307-151">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


