---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 0299494ca775df60c94151f36efe554d0b876d22
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700323"
---
# <span data-ttu-id="a39ec-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a39ec-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="a39ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a39ec-102">SYNOPSIS</span></span>
<span data-ttu-id="a39ec-103">부하 분산 장치에 대 한 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a39ec-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="a39ec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a39ec-104">SYNTAX</span></span>

### <span data-ttu-id="a39ec-105">SetByResourceSubnet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a39ec-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] [-Zone <String[]>]
 -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a39ec-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="a39ec-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] [-Zone <String[]>]
 -SubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a39ec-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a39ec-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a39ec-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a39ec-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a39ec-109">설명은</span><span class="sxs-lookup"><span data-stu-id="a39ec-109">DESCRIPTION</span></span>
<span data-ttu-id="a39ec-110">**AzLoadBalancerFrontendIpConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a39ec-110">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="a39ec-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a39ec-111">EXAMPLES</span></span>

### <span data-ttu-id="a39ec-112">예제 1: 부하 분산 장치에 대 한 프런트 엔드 IP 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="a39ec-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="a39ec-113">첫 번째 명령은 MyResourceGroup 이라는 리소스 그룹에 MyPublicIP 라는 동적 공용 IP 주소를 만든 다음이를 $publicip 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a39ec-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="a39ec-114">두 번째 명령은 $publicip에서 공용 IP 주소를 사용 하 여 FrontendIpConfig01 라는 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a39ec-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="a39ec-115">변수</span><span class="sxs-lookup"><span data-stu-id="a39ec-115">PARAMETERS</span></span>

### <span data-ttu-id="a39ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a39ec-116">-DefaultProfile</span></span>
<span data-ttu-id="a39ec-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a39ec-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a39ec-118">-이름</span><span class="sxs-lookup"><span data-stu-id="a39ec-118">-Name</span></span>
<span data-ttu-id="a39ec-119">이 cmdlet이 만드는 프런트 엔드 IP 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a39ec-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a39ec-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="a39ec-120">-PrivateIpAddress</span></span>
<span data-ttu-id="a39ec-121">부하 분산 장치의 개인 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a39ec-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="a39ec-122">*서브넷* 매개 변수도 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a39ec-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="a39ec-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a39ec-123">-PublicIpAddress</span></span>
<span data-ttu-id="a39ec-124">프런트 엔드 IP 구성과 연결 되는 **PublicIpAddress** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a39ec-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="a39ec-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="a39ec-125">-PublicIpAddressId</span></span>
<span data-ttu-id="a39ec-126">프런트 엔드 IP 구성과 연결할 **PublicIpAddress** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a39ec-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="a39ec-127">-서브넷</span><span class="sxs-lookup"><span data-stu-id="a39ec-127">-Subnet</span></span>
<span data-ttu-id="a39ec-128">프런트 엔드 IP 구성을 만들 **서브넷** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a39ec-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="a39ec-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a39ec-129">-SubnetId</span></span>
<span data-ttu-id="a39ec-130">프런트 엔드 IP 구성을 만들 서브넷의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a39ec-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="a39ec-131">-Zone</span><span class="sxs-lookup"><span data-stu-id="a39ec-131">-Zone</span></span>
<span data-ttu-id="a39ec-132">리소스에 대해 할당 된 IP를 나타내는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a39ec-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a39ec-133">-확인</span><span class="sxs-lookup"><span data-stu-id="a39ec-133">-Confirm</span></span>
<span data-ttu-id="a39ec-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a39ec-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a39ec-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a39ec-135">-WhatIf</span></span>
<span data-ttu-id="a39ec-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a39ec-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a39ec-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a39ec-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a39ec-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a39ec-138">CommonParameters</span></span>
<span data-ttu-id="a39ec-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a39ec-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a39ec-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a39ec-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a39ec-141">입력</span><span class="sxs-lookup"><span data-stu-id="a39ec-141">INPUTS</span></span>

### <span data-ttu-id="a39ec-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a39ec-142">System.String</span></span>

### <span data-ttu-id="a39ec-143">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="a39ec-143">System.String[]</span></span>

### <span data-ttu-id="a39ec-144">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="a39ec-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="a39ec-145">PSPublicIpAddress에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a39ec-145">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="a39ec-146">출력</span><span class="sxs-lookup"><span data-stu-id="a39ec-146">OUTPUTS</span></span>

### <span data-ttu-id="a39ec-147">PSFrontendIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a39ec-147">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="a39ec-148">상속자</span><span class="sxs-lookup"><span data-stu-id="a39ec-148">NOTES</span></span>

## <span data-ttu-id="a39ec-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a39ec-149">RELATED LINKS</span></span>

[<span data-ttu-id="a39ec-150">추가-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a39ec-150">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a39ec-151">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a39ec-151">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a39ec-152">새로운 AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a39ec-152">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="a39ec-153">제거-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a39ec-153">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="a39ec-154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="a39ec-154">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


