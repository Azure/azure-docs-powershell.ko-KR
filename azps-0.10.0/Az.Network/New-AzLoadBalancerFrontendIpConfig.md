---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: ba29cef7afe862f8aeb33f66488e0970b5ac6e9c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875430"
---
# <span data-ttu-id="756b1-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="756b1-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="756b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="756b1-102">SYNOPSIS</span></span>
<span data-ttu-id="756b1-103">부하 분산 장치에 대 한 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="756b1-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="756b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="756b1-104">SYNTAX</span></span>

### <span data-ttu-id="756b1-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="756b1-105">SetByResourceSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -Subnet <PSSubnet>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="756b1-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="756b1-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -SubnetId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="756b1-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="756b1-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddressId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="756b1-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="756b1-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddress <PSPublicIpAddress>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="756b1-109">설명은</span><span class="sxs-lookup"><span data-stu-id="756b1-109">DESCRIPTION</span></span>
<span data-ttu-id="756b1-110">**AzLoadBalancerFrontendIpConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="756b1-110">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="756b1-111">예제의</span><span class="sxs-lookup"><span data-stu-id="756b1-111">EXAMPLES</span></span>

### <span data-ttu-id="756b1-112">예제 1: 부하 분산 장치에 대 한 프런트 엔드 IP 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="756b1-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="756b1-113">첫 번째 명령은 MyResourceGroup 이라는 리소스 그룹에 MyPublicIP 라는 동적 공용 IP 주소를 만든 다음이를 $publicip 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b1-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="756b1-114">두 번째 명령은 $publicip에서 공용 IP 주소를 사용 하 여 FrontendIpConfig01 라는 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="756b1-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="756b1-115">변수</span><span class="sxs-lookup"><span data-stu-id="756b1-115">PARAMETERS</span></span>

### <span data-ttu-id="756b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="756b1-116">-DefaultProfile</span></span>
<span data-ttu-id="756b1-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="756b1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="756b1-118">-이름</span><span class="sxs-lookup"><span data-stu-id="756b1-118">-Name</span></span>
<span data-ttu-id="756b1-119">이 cmdlet이 만드는 프런트 엔드 IP 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b1-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="756b1-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="756b1-120">-PrivateIpAddress</span></span>
<span data-ttu-id="756b1-121">부하 분산 장치의 개인 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b1-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="756b1-122">*서브넷* 매개 변수도 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b1-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="756b1-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="756b1-123">-PublicIpAddress</span></span>
<span data-ttu-id="756b1-124">프런트 엔드 IP 구성과 연결 되는 **PublicIpAddress** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b1-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="756b1-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="756b1-125">-PublicIpAddressId</span></span>
<span data-ttu-id="756b1-126">프런트 엔드 IP 구성과 연결할 **PublicIpAddress** 개체의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b1-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="756b1-127">-서브넷</span><span class="sxs-lookup"><span data-stu-id="756b1-127">-Subnet</span></span>
<span data-ttu-id="756b1-128">프런트 엔드 IP 구성을 만들 **서브넷** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b1-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="756b1-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="756b1-129">-SubnetId</span></span>
<span data-ttu-id="756b1-130">프런트 엔드 IP 구성을 만들 서브넷의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b1-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="756b1-131">-Zone</span><span class="sxs-lookup"><span data-stu-id="756b1-131">-Zone</span></span>
<span data-ttu-id="756b1-132">리소스에 대해 할당 된 IP를 나타내는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="756b1-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="756b1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="756b1-133">CommonParameters</span></span>
<span data-ttu-id="756b1-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="756b1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="756b1-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="756b1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="756b1-136">입력</span><span class="sxs-lookup"><span data-stu-id="756b1-136">INPUTS</span></span>

## <span data-ttu-id="756b1-137">출력</span><span class="sxs-lookup"><span data-stu-id="756b1-137">OUTPUTS</span></span>

### <span data-ttu-id="756b1-138">PSFrontendIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="756b1-138">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="756b1-139">상속자</span><span class="sxs-lookup"><span data-stu-id="756b1-139">NOTES</span></span>

## <span data-ttu-id="756b1-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="756b1-140">RELATED LINKS</span></span>

[<span data-ttu-id="756b1-141">추가-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="756b1-141">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="756b1-142">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="756b1-142">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="756b1-143">새로운 AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="756b1-143">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="756b1-144">제거-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="756b1-144">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="756b1-145">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="756b1-145">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


