---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
ms.openlocfilehash: 11939edc15d49614d2a1fd1692825cd07cd82b2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869825"
---
# <span data-ttu-id="1bd0c-101">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1bd0c-101">New-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="1bd0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bd0c-102">SYNOPSIS</span></span>
<span data-ttu-id="1bd0c-103">VirtualNetworkTap 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-103">Creates a VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="1bd0c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1bd0c-104">SYNTAX</span></span>

### <span data-ttu-id="1bd0c-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="1bd0c-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bd0c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1bd0c-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bd0c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1bd0c-107">DESCRIPTION</span></span>
<span data-ttu-id="1bd0c-108">**AzVirtualNetworkTap** Cmdlet은 Azure 가상 네트워크를 만드는 리소스를 탭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-108">The **New-AzVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="1bd0c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1bd0c-109">EXAMPLES</span></span>

### <span data-ttu-id="1bd0c-110">예제 1: Azure 가상 네트워크 만들기 탭</span><span class="sxs-lookup"><span data-stu-id="1bd0c-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="1bd0c-111">이 명령은 대상 VM 구성 세부 정보 (DestinationIpConfiguration, Destinationipconfiguration)가 있는 "VirtualNetworkTap1" 라는 가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="1bd0c-112">모든 원본 탭 구성 된 모든 VM의 트래픽이이 대상 IP + 포트로 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="1bd0c-113">예제 2: Azure 가상 네트워크 만들기 LoadBalancer IP를 사용 하 여 탭 하기</span><span class="sxs-lookup"><span data-stu-id="1bd0c-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="1bd0c-114">이 명령은 대상 VM 구성 세부 정보 (FrontEndIpConfiguration)가 있는 "VirtualNetworkTap1" 라는 가상 네트워크를 탭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="1bd0c-115">모든 원본 탭 구성 된 모든 VM의 트래픽이이 부하 분산 장치 IpConfiguration으로 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="1bd0c-116">기본 대상 포트는 4789입니다.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="1bd0c-117">변수</span><span class="sxs-lookup"><span data-stu-id="1bd0c-117">PARAMETERS</span></span>

### <span data-ttu-id="1bd0c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bd0c-118">-AsJob</span></span>
<span data-ttu-id="1bd0c-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1bd0c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1bd0c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bd0c-120">-DefaultProfile</span></span>
<span data-ttu-id="1bd0c-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bd0c-122">-DestinationLoadBalancerFrontEndIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bd0c-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="1bd0c-123">대상 부하 분산 장치 프론트 엔드 IP 구성 리소스의 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd0c-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1bd0c-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="1bd0c-125">대상 부하 분산 장치 프론트 엔드 IP 구성 리소스의 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd0c-126">-DestinationNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bd0c-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="1bd0c-127">대상 네트워크 인터페이스 IP 구성 리소스의 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-127">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd0c-128">-DestinationNetworkInterfaceIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1bd0c-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="1bd0c-129">대상 네트워크 인터페이스 IP 구성 리소스의 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-129">The reference of the destination network interface IP configuration resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd0c-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="1bd0c-130">-DestinationPort</span></span>
<span data-ttu-id="1bd0c-131">패킷 수집기의 대상 포트</span><span class="sxs-lookup"><span data-stu-id="1bd0c-131">The Destination Port of the packet collector</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd0c-132">-Force</span><span class="sxs-lookup"><span data-stu-id="1bd0c-132">-Force</span></span>
<span data-ttu-id="1bd0c-133">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="1bd0c-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1bd0c-134">-위치</span><span class="sxs-lookup"><span data-stu-id="1bd0c-134">-Location</span></span>
<span data-ttu-id="1bd0c-135">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-135">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd0c-136">-이름</span><span class="sxs-lookup"><span data-stu-id="1bd0c-136">-Name</span></span>
<span data-ttu-id="1bd0c-137">탭의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-137">The name of the tap.</span></span>

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

### <span data-ttu-id="1bd0c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bd0c-138">-ResourceGroupName</span></span>
<span data-ttu-id="1bd0c-139">가상 네트워크의 리소스 그룹 이름 탭 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-139">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="1bd0c-140">태그</span><span class="sxs-lookup"><span data-stu-id="1bd0c-140">-Tag</span></span>
<span data-ttu-id="1bd0c-141">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-141">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd0c-142">-확인</span><span class="sxs-lookup"><span data-stu-id="1bd0c-142">-Confirm</span></span>
<span data-ttu-id="1bd0c-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bd0c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bd0c-144">-WhatIf</span></span>
<span data-ttu-id="1bd0c-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bd0c-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bd0c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bd0c-147">CommonParameters</span></span>
<span data-ttu-id="1bd0c-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bd0c-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bd0c-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bd0c-150">입력</span><span class="sxs-lookup"><span data-stu-id="1bd0c-150">INPUTS</span></span>

### <span data-ttu-id="1bd0c-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1bd0c-151">System.String</span></span>

### <span data-ttu-id="1bd0c-152">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-152">System.Int32</span></span>

### <span data-ttu-id="1bd0c-153">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="1bd0c-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1bd0c-154">PSNetworkInterfaceIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="1bd0c-155">PSFrontendIPConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="1bd0c-156">출력</span><span class="sxs-lookup"><span data-stu-id="1bd0c-156">OUTPUTS</span></span>

### <span data-ttu-id="1bd0c-157">PSVirtualNetworkTap에 대 한.</span><span class="sxs-lookup"><span data-stu-id="1bd0c-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="1bd0c-158">상속자</span><span class="sxs-lookup"><span data-stu-id="1bd0c-158">NOTES</span></span>

## <span data-ttu-id="1bd0c-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1bd0c-159">RELATED LINKS</span></span>

[<span data-ttu-id="1bd0c-160">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1bd0c-160">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="1bd0c-161">제거-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1bd0c-161">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="1bd0c-162">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1bd0c-162">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
