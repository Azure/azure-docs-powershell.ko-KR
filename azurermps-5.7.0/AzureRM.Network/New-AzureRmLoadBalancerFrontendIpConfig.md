---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: b05804bb5af2513e6a54026c7b989662212ba350
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703012"
---
# <span data-ttu-id="d45c6-101">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d45c6-101">New-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="d45c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d45c6-102">SYNOPSIS</span></span>
<span data-ttu-id="d45c6-103">부하 분산 장치에 대 한 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d45c6-103">Creates a front-end IP configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d45c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d45c6-104">SYNTAX</span></span>

### <span data-ttu-id="d45c6-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="d45c6-105">SetByResourceSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -Subnet <PSSubnet>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d45c6-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="d45c6-106">SetByResourceIdSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -SubnetId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d45c6-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d45c6-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddressId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d45c6-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d45c6-108">SetByResourcePublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddress <PSPublicIpAddress>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d45c6-109">설명은</span><span class="sxs-lookup"><span data-stu-id="d45c6-109">DESCRIPTION</span></span>
<span data-ttu-id="d45c6-110">**AzureRmLoadBalancerFrontendIpConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d45c6-110">The **New-AzureRmLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="d45c6-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d45c6-111">EXAMPLES</span></span>

### <span data-ttu-id="d45c6-112">예제 1: 부하 분산 장치에 대 한 프런트 엔드 IP 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="d45c6-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="d45c6-113">첫 번째 명령은 MyResourceGroup 이라는 리소스 그룹에 MyPublicIP 라는 동적 공용 IP 주소를 만든 다음이를 $publicip 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d45c6-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="d45c6-114">두 번째 명령은 $publicip에서 공용 IP 주소를 사용 하 여 FrontendIpConfig01 라는 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d45c6-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="d45c6-115">변수</span><span class="sxs-lookup"><span data-stu-id="d45c6-115">PARAMETERS</span></span>

### <span data-ttu-id="d45c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d45c6-116">-DefaultProfile</span></span>
<span data-ttu-id="d45c6-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d45c6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45c6-118">-이름</span><span class="sxs-lookup"><span data-stu-id="d45c6-118">-Name</span></span>
<span data-ttu-id="d45c6-119">이 cmdlet이 만드는 프런트 엔드 IP 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d45c6-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45c6-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="d45c6-120">-PrivateIpAddress</span></span>
<span data-ttu-id="d45c6-121">부하 분산 장치의 개인 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d45c6-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="d45c6-122">*서브넷* 매개 변수도 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d45c6-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45c6-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d45c6-123">-PublicIpAddress</span></span>
<span data-ttu-id="d45c6-124">프런트 엔드 IP 구성과 연결 되는 **PublicIpAddress** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d45c6-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45c6-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="d45c6-125">-PublicIpAddressId</span></span>
<span data-ttu-id="d45c6-126">프런트 엔드 IP 구성과 연결할 **PublicIpAddress** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d45c6-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45c6-127">-서브넷</span><span class="sxs-lookup"><span data-stu-id="d45c6-127">-Subnet</span></span>
<span data-ttu-id="d45c6-128">프런트 엔드 IP 구성을 만들 **서브넷** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d45c6-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45c6-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d45c6-129">-SubnetId</span></span>
<span data-ttu-id="d45c6-130">프런트 엔드 IP 구성을 만들 서브넷의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d45c6-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d45c6-131">-Zone</span><span class="sxs-lookup"><span data-stu-id="d45c6-131">-Zone</span></span>
<span data-ttu-id="d45c6-132">리소스에 대해 할당 된 IP를 나타내는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d45c6-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="d45c6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d45c6-133">CommonParameters</span></span>
<span data-ttu-id="d45c6-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d45c6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d45c6-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d45c6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d45c6-136">입력</span><span class="sxs-lookup"><span data-stu-id="d45c6-136">INPUTS</span></span>

### <span data-ttu-id="d45c6-137">않아야</span><span class="sxs-lookup"><span data-stu-id="d45c6-137">None</span></span>
<span data-ttu-id="d45c6-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d45c6-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d45c6-139">출력</span><span class="sxs-lookup"><span data-stu-id="d45c6-139">OUTPUTS</span></span>

### <span data-ttu-id="d45c6-140">PSFrontendIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d45c6-140">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="d45c6-141">상속자</span><span class="sxs-lookup"><span data-stu-id="d45c6-141">NOTES</span></span>

## <span data-ttu-id="d45c6-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d45c6-142">RELATED LINKS</span></span>

[<span data-ttu-id="d45c6-143">추가-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d45c6-143">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d45c6-144">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d45c6-144">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d45c6-145">새로운 AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d45c6-145">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="d45c6-146">제거-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d45c6-146">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d45c6-147">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d45c6-147">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


