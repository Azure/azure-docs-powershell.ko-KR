---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkTap.md
ms.openlocfilehash: 0ac64d9b1aee363a1681b8d62da2ecf73574f7cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202686"
---
# <span data-ttu-id="7162c-101">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7162c-101">New-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="7162c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7162c-102">SYNOPSIS</span></span>
<span data-ttu-id="7162c-103">VirtualNetworkTap 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7162c-103">Creates a VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="7162c-104">구문</span><span class="sxs-lookup"><span data-stu-id="7162c-104">SYNTAX</span></span>

### <span data-ttu-id="7162c-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="7162c-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>]
 [-DestinationNetworkInterfaceIPConfiguration <PSNetworkInterfaceIPConfiguration>]
 [-DestinationLoadBalancerFrontEndIPConfiguration <PSFrontendIPConfiguration>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7162c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7162c-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-DestinationPort <Int32>]
 [-Location <String>] [-Tag <Hashtable>] [-DestinationNetworkInterfaceIPConfigurationId <String>]
 [-DestinationLoadBalancerFrontEndIPConfigurationId <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7162c-107">설명</span><span class="sxs-lookup"><span data-stu-id="7162c-107">DESCRIPTION</span></span>
<span data-ttu-id="7162c-108">**New-AzVirtualNetworkTap** cmdlet은 Azure 가상 네트워크 탭 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7162c-108">The **New-AzVirtualNetworkTap** cmdlet creates an Azure virtual network tap resource.</span></span>

## <span data-ttu-id="7162c-109">예제</span><span class="sxs-lookup"><span data-stu-id="7162c-109">EXAMPLES</span></span>

### <span data-ttu-id="7162c-110">예제 1: Azure 가상 네트워크 탭 만들기</span><span class="sxs-lookup"><span data-stu-id="7162c-110">Example 1: Create an Azure virtual network tap</span></span>
```
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationPort 8888 -DestinationNetworkInterfaceIPConfiguration $destinationNic.IpConfigurations[0]
```

<span data-ttu-id="7162c-111">이 명령은 대상 VM 구성 세부 정보(DestinationIpConfiguration, DestinationPort)가 있는 "VirtualNetworkTap1"이라는 가상 네트워크 탭을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7162c-111">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (DestinationIpConfiguration, DestinationPort).</span></span>
<span data-ttu-id="7162c-112">모든 원본 탭으로 구성된 VM의 트래픽이 이 대상 IP + 포트로 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="7162c-112">All the source tap configured VM's traffic will be routed to this Destination IP + Port.</span></span>

### <span data-ttu-id="7162c-113">예제 2: LoadBalancer IP를 사용하여 Azure 가상 네트워크 탭 만들기</span><span class="sxs-lookup"><span data-stu-id="7162c-113">Example 2: Create an Azure virtual network tap using LoadBalancer IP</span></span>
```
# Create LoadBalancer
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\>New-AzVirtualNetworkTap -Name "VirtualNetworkTap1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -DestinationLoadBalancerFrontEndIPConfiguration $frontend
```

<span data-ttu-id="7162c-114">이 명령은 대상 VM 구성 세부 정보(FrontEndIpConfiguration)가 있는 "VirtualNetworkTap1"이라는 가상 네트워크 탭을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7162c-114">This command creates a virtual network tap named "VirtualNetworkTap1" which has destination VM configuration details (FrontEndIpConfiguration).</span></span>
<span data-ttu-id="7162c-115">모든 원본 탭으로 구성된 VM의 트래픽이 이 LoadBalancer IpConfiguration으로 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="7162c-115">All the source tap configured VM's traffic will be routed to this LoadBalancer IpConfiguration.</span></span> <span data-ttu-id="7162c-116">기본 대상 포트는 4789입니다.</span><span class="sxs-lookup"><span data-stu-id="7162c-116">Default Destination Port is 4789.</span></span>

## <span data-ttu-id="7162c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7162c-117">PARAMETERS</span></span>

### <span data-ttu-id="7162c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7162c-118">-AsJob</span></span>
<span data-ttu-id="7162c-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7162c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7162c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7162c-120">-DefaultProfile</span></span>
<span data-ttu-id="7162c-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7162c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7162c-122">-DestinationLoadBalancerFrontEndIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7162c-122">-DestinationLoadBalancerFrontEndIPConfiguration</span></span>
<span data-ttu-id="7162c-123">대상 부하 균형 조정기 프런트 엔드 IP 구성 리소스에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="7162c-123">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="7162c-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7162c-124">-DestinationLoadBalancerFrontEndIPConfigurationId</span></span>
<span data-ttu-id="7162c-125">대상 부하 균형 조정기 프런트 엔드 IP 구성 리소스에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="7162c-125">The reference of the destination load balancer front end IP configuration resource.</span></span>

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

### <span data-ttu-id="7162c-126">-DestinationNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7162c-126">-DestinationNetworkInterfaceIPConfiguration</span></span>
<span data-ttu-id="7162c-127">대상 네트워크 인터페이스 IP 구성 리소스에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="7162c-127">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="7162c-128">-DestinationNetworkInterfaceIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7162c-128">-DestinationNetworkInterfaceIPConfigurationId</span></span>
<span data-ttu-id="7162c-129">대상 네트워크 인터페이스 IP 구성 리소스에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="7162c-129">The reference of the destination network interface IP configuration resource.</span></span>

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

### <span data-ttu-id="7162c-130">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="7162c-130">-DestinationPort</span></span>
<span data-ttu-id="7162c-131">패킷 수집기 대상 포트</span><span class="sxs-lookup"><span data-stu-id="7162c-131">The Destination Port of the packet collector</span></span>

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

### <span data-ttu-id="7162c-132">-Force</span><span class="sxs-lookup"><span data-stu-id="7162c-132">-Force</span></span>
<span data-ttu-id="7162c-133">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7162c-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7162c-134">-Location</span><span class="sxs-lookup"><span data-stu-id="7162c-134">-Location</span></span>
<span data-ttu-id="7162c-135">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7162c-135">The location.</span></span>

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

### <span data-ttu-id="7162c-136">-Name</span><span class="sxs-lookup"><span data-stu-id="7162c-136">-Name</span></span>
<span data-ttu-id="7162c-137">탭의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7162c-137">The name of the tap.</span></span>

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

### <span data-ttu-id="7162c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7162c-138">-ResourceGroupName</span></span>
<span data-ttu-id="7162c-139">가상 네트워크 탭의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7162c-139">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="7162c-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="7162c-140">-Tag</span></span>
<span data-ttu-id="7162c-141">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="7162c-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7162c-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7162c-142">-Confirm</span></span>
<span data-ttu-id="7162c-143">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7162c-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7162c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7162c-144">-WhatIf</span></span>
<span data-ttu-id="7162c-145">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7162c-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7162c-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7162c-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7162c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7162c-147">CommonParameters</span></span>
<span data-ttu-id="7162c-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7162c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7162c-149">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7162c-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7162c-150">입력</span><span class="sxs-lookup"><span data-stu-id="7162c-150">INPUTS</span></span>

### <span data-ttu-id="7162c-151">System.String</span><span class="sxs-lookup"><span data-stu-id="7162c-151">System.String</span></span>

### <span data-ttu-id="7162c-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="7162c-152">System.Int32</span></span>

### <span data-ttu-id="7162c-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7162c-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7162c-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7162c-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

### <span data-ttu-id="7162c-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7162c-155">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="7162c-156">출력</span><span class="sxs-lookup"><span data-stu-id="7162c-156">OUTPUTS</span></span>

### <span data-ttu-id="7162c-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7162c-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="7162c-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7162c-158">NOTES</span></span>

## <span data-ttu-id="7162c-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7162c-159">RELATED LINKS</span></span>

[<span data-ttu-id="7162c-160">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7162c-160">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="7162c-161">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7162c-161">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="7162c-162">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7162c-162">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
