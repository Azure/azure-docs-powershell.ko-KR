---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: b3ea1ab3bbe3edbc72b81c25817af40e9e5fc2a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958224"
---
# <span data-ttu-id="f810d-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f810d-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="f810d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f810d-102">SYNOPSIS</span></span>
<span data-ttu-id="f810d-103">공용 IP 주소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-103">Creates a public IP address.</span></span>

## <span data-ttu-id="f810d-104">구문</span><span class="sxs-lookup"><span data-stu-id="f810d-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <PSPublicIpTag[]>] [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f810d-105">설명</span><span class="sxs-lookup"><span data-stu-id="f810d-105">DESCRIPTION</span></span>
<span data-ttu-id="f810d-106">**New-AzPublicIpAddress** cmdlet은 공용 IP 주소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="f810d-107">예제</span><span class="sxs-lookup"><span data-stu-id="f810d-107">EXAMPLES</span></span>

### <span data-ttu-id="f810d-108">예제 1: 새 공용 IP 주소 만들기</span><span class="sxs-lookup"><span data-stu-id="f810d-108">Example 1: Create a new public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="f810d-109">이 명령은 새 공용 IP 주소 리소스를 만듭니다. 이 리소스의 공용 IP 주소를 $dnsPrefix.$location.cloudapp.azure.com에 대한 DNS 레코드가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="f810d-110">-AllocationMethod가 '정적'으로 지정되어 공용 IP 주소가 이 리소스에 즉시 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="f810d-111">'Dynamic'으로 지정된 경우 연결된 리소스(예: VM 또는 부하 균형기)를 시작하거나 만들 때만 공용 IP 주소가 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="f810d-112">예제 2: 역방향 FQDN을 사용하여 공용 IP 주소 만들기</span><span class="sxs-lookup"><span data-stu-id="f810d-112">Example 2: Create a public IP address with a reverse FQDN</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="f810d-113">이 명령은 새 공용 IP 주소 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="f810d-114">-ReverseFqdn 매개 변수를 사용하여 Azure는 이 리소스에 할당된 공용 IP 주소에 대한 DNS PTR 레코드(역방향 $customFqdn)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="f810d-115">전제품으로 $customFqdn(예: webapp.contoso.com)에는 $dnsPrefix.$location.cloudapp.azure.com을 $dnsPrefix CNAME 레코드가 $location 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="f810d-116">예제 3: IpTag를 사용하여 새 공용 IP 주소 만들기</span><span class="sxs-lookup"><span data-stu-id="f810d-116">Example 3: Create a new public IP address with IpTag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

<span data-ttu-id="f810d-117">이 명령은 새 공용 IP 주소 리소스를 만듭니다. 이 리소스의 공용 IP 주소를 $dnsPrefix.$location.cloudapp.azure.com에 대한 DNS 레코드가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="f810d-118">-AllocationMethod가 '정적'으로 지정되어 공용 IP 주소가 이 리소스에 즉시 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="f810d-119">'Dynamic'으로 지정된 경우 연결된 리소스(예: VM 또는 부하 균형기)를 시작하거나 만들 때만 공용 IP 주소가 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="f810d-120">Iptag는 리소스와 연결된 태그를 특정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="f810d-121">Iptag는 iptag를 사용하여 New-AzPublicIpTag -ipTags를 통해 입력으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-121">Iptag can be specified using New-AzPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="f810d-122">예제 4: 프리픽스에서 새 공용 IP 주소 만들기</span><span class="sxs-lookup"><span data-stu-id="f810d-122">Example 4: Create a new public IP address from a Prefix</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="f810d-123">이 명령은 새 공용 IP 주소 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="f810d-124">이 리소스의 공용 IP 주소를 $dnsPrefix.$location.cloudapp.azure.com에 대한 DNS 레코드가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="f810d-125">공용 IP 주소는 지정된 publicIpPrefix에서 이 리소스에 즉시 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="f810d-126">이 옵션은 'Standard' Sku 및 'Static' AllocationMethod에만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

### <span data-ttu-id="f810d-127">예제 5: 새 전역 공용 IP 주소 만들기</span><span class="sxs-lookup"><span data-stu-id="f810d-127">Example 5: Create a new global public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $domainNameLabel -Location $location -Sku Standard -Tier Global
```

<span data-ttu-id="f810d-128">이 명령은 새 전역 공용 IP 주소 리소스를 만듭니다. 이 리소스의 공용 IP 주소를 $dnsPrefix.$location.cloudapp.azure.com에 대한 DNS 레코드가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-128">This command creates a new global public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="f810d-129">전역 공용 IP 주소가 이 리소스에 즉시 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-129">A global public IP address is immediately allocated to this resource.</span></span>
<span data-ttu-id="f810d-130">이 옵션은 'Standard' Sku 및 'Static' AllocationMethod에만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-130">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="f810d-131">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f810d-131">PARAMETERS</span></span>

### <span data-ttu-id="f810d-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="f810d-132">-AllocationMethod</span></span>
<span data-ttu-id="f810d-133">공용 IP 주소를 할당할 메서드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-133">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="f810d-134">이 매개 변수에 대해 허용되는 값은 정적 또는 동적입니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-134">The acceptable values for this parameter are: Static or Dynamic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f810d-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f810d-135">-AsJob</span></span>
<span data-ttu-id="f810d-136">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f810d-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f810d-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f810d-137">-DefaultProfile</span></span>
<span data-ttu-id="f810d-138">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f810d-139">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="f810d-139">-DomainNameLabel</span></span>
<span data-ttu-id="f810d-140">공용 IP 주소에 대한 상대 DNS 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-140">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="f810d-141">-Force</span><span class="sxs-lookup"><span data-stu-id="f810d-141">-Force</span></span>
<span data-ttu-id="f810d-142">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f810d-143">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f810d-143">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="f810d-144">유휴 시간(분)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-144">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="f810d-145">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="f810d-145">-IpAddressVersion</span></span>
<span data-ttu-id="f810d-146">IP 주소의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-146">Specifies the version of the IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f810d-147">-IpTag</span><span class="sxs-lookup"><span data-stu-id="f810d-147">-IpTag</span></span>
<span data-ttu-id="f810d-148">IpTag 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-148">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f810d-149">-Location</span><span class="sxs-lookup"><span data-stu-id="f810d-149">-Location</span></span>
<span data-ttu-id="f810d-150">공용 IP 주소를 만들 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-150">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="f810d-151">-Name</span><span class="sxs-lookup"><span data-stu-id="f810d-151">-Name</span></span>
<span data-ttu-id="f810d-152">이 cmdlet이 만드는 공용 IP 주소의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-152">Specifies the name of the public IP address that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f810d-153">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f810d-153">-PublicIpPrefix</span></span>
<span data-ttu-id="f810d-154">공용 IP 주소를 할당할 PSPublicIpPrefix를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-154">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f810d-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f810d-155">-ResourceGroupName</span></span>
<span data-ttu-id="f810d-156">공용 IP 주소를 만들 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-156">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="f810d-157">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="f810d-157">-ReverseFqdn</span></span>
<span data-ttu-id="f810d-158">역방향 완전 자격을 갖춘 도메인 이름(FQDN)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-158">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="f810d-159">-Sku</span><span class="sxs-lookup"><span data-stu-id="f810d-159">-Sku</span></span>
<span data-ttu-id="f810d-160">공용 IP Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-160">The public IP Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f810d-161">-Tag</span><span class="sxs-lookup"><span data-stu-id="f810d-161">-Tag</span></span>
<span data-ttu-id="f810d-162">해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-162">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f810d-163">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="f810d-163">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f810d-164">-Tier</span><span class="sxs-lookup"><span data-stu-id="f810d-164">-Tier</span></span>
<span data-ttu-id="f810d-165">공용 IP Sku 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-165">The public IP Sku Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f810d-166">-Zone</span><span class="sxs-lookup"><span data-stu-id="f810d-166">-Zone</span></span>
<span data-ttu-id="f810d-167">리소스에 할당된 IP를 표시하는 가용성 영역 목록이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-167">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="f810d-168">-확인</span><span class="sxs-lookup"><span data-stu-id="f810d-168">-Confirm</span></span>
<span data-ttu-id="f810d-169">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f810d-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f810d-170">-WhatIf</span></span>
<span data-ttu-id="f810d-171">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f810d-172">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f810d-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f810d-173">CommonParameters</span></span>
<span data-ttu-id="f810d-174">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f810d-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f810d-175">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f810d-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f810d-176">입력</span><span class="sxs-lookup"><span data-stu-id="f810d-176">INPUTS</span></span>

### <span data-ttu-id="f810d-177">System.String</span><span class="sxs-lookup"><span data-stu-id="f810d-177">System.String</span></span>

### <span data-ttu-id="f810d-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span><span class="sxs-lookup"><span data-stu-id="f810d-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span></span>

### <span data-ttu-id="f810d-179">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f810d-179">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

### <span data-ttu-id="f810d-180">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f810d-180">System.Int32</span></span>

### <span data-ttu-id="f810d-181">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f810d-181">System.String[]</span></span>

### <span data-ttu-id="f810d-182">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f810d-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f810d-183">출력</span><span class="sxs-lookup"><span data-stu-id="f810d-183">OUTPUTS</span></span>

### <span data-ttu-id="f810d-184">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f810d-184">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="f810d-185">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f810d-185">NOTES</span></span>

## <span data-ttu-id="f810d-186">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f810d-186">RELATED LINKS</span></span>

[<span data-ttu-id="f810d-187">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f810d-187">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="f810d-188">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f810d-188">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="f810d-189">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f810d-189">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
