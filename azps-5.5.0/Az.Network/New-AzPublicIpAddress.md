---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 8c48c7ec1f651348309c012275287bd88dd42bcc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184356"
---
# <span data-ttu-id="22f3c-101">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="22f3c-101">New-AzPublicIpAddress</span></span>

## <span data-ttu-id="22f3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="22f3c-103">공용 IP 주소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-103">Creates a public IP address.</span></span>

## <span data-ttu-id="22f3c-104">구문</span><span class="sxs-lookup"><span data-stu-id="22f3c-104">SYNTAX</span></span>

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <PSPublicIpTag[]>] [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22f3c-105">설명</span><span class="sxs-lookup"><span data-stu-id="22f3c-105">DESCRIPTION</span></span>
<span data-ttu-id="22f3c-106">**New-AzPublicIpAddress** cmdlet은 공용 IP 주소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-106">The **New-AzPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="22f3c-107">예제</span><span class="sxs-lookup"><span data-stu-id="22f3c-107">EXAMPLES</span></span>

### <span data-ttu-id="22f3c-108">예제 1: 새 공용 IP 주소 만들기</span><span class="sxs-lookup"><span data-stu-id="22f3c-108">Example 1: Create a new public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="22f3c-109">이 명령은 새 공용 IP 주소 리소스를 만듭니다. 이 리소스의 공용 IP 주소를 $dnsPrefix.$location.cloudapp.azure.com에 대한 DNS 레코드가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="22f3c-110">-AllocationMethod가 'Static'으로 지정되어 공용 IP 주소가 이 리소스에 즉시 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="22f3c-111">'동적'으로 지정된 경우 공용 IP 주소는 연결된 리소스(예: VM 또는 부하 분배기)를 시작하거나 만들 때만 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="22f3c-112">예제 2: 역방향 FQDN을 사용하여 공용 IP 주소 만들기</span><span class="sxs-lookup"><span data-stu-id="22f3c-112">Example 2: Create a public IP address with a reverse FQDN</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="22f3c-113">이 명령은 새 공용 IP 주소 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="22f3c-114">-ReverseFqdn 매개 변수를 사용하여 Azure는 이 리소스에 할당된 공용 IP 주소에 대한 DNS PTR 레코드(역방향 $customFqdn)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="22f3c-115">전제로 $customFqdn(예: webapp.contoso.com)에는 $dnsPrefix.$location.cloudapp.azure.com을 $dnsPrefix CNAME 레코드(전달-lookup)가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="22f3c-116">예제 3: IpTag를 사용하여 새 공용 IP 주소 만들기</span><span class="sxs-lookup"><span data-stu-id="22f3c-116">Example 3: Create a new public IP address with IpTag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

<span data-ttu-id="22f3c-117">이 명령은 새 공용 IP 주소 리소스를 만듭니다. 이 리소스의 공용 IP 주소를 $dnsPrefix.$location.cloudapp.azure.com에 대한 DNS 레코드가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="22f3c-118">-AllocationMethod가 'Static'으로 지정되어 공용 IP 주소가 이 리소스에 즉시 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="22f3c-119">'동적'으로 지정된 경우 공용 IP 주소는 연결된 리소스(예: VM 또는 부하 분배기)를 시작하거나 만들 때만 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="22f3c-120">Iptag는 리소스와 연결된 태그를 구체화하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="22f3c-121">Iptag는 iptag를 사용하여 New-AzPublicIpTag -IpTags를 통해 입력으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-121">Iptag can be specified using New-AzPublicIpTag and passed as input through -IpTags.</span></span>

### <span data-ttu-id="22f3c-122">예제 4: Prefix에서 새 공용 IP 주소 만들기</span><span class="sxs-lookup"><span data-stu-id="22f3c-122">Example 4: Create a new public IP address from a Prefix</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

<span data-ttu-id="22f3c-123">이 명령은 새 공용 IP 주소 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-123">This command creates a new public IP address resource.</span></span> <span data-ttu-id="22f3c-124">이 리소스의 공용 IP 주소를 $dnsPrefix.$location.cloudapp.azure.com에 대한 DNS 레코드가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-124">A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="22f3c-125">공용 IP 주소는 지정된 publicIpPrefix에서 이 리소스에 즉시 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-125">A public IP address is immediately allocated to this resource from the publicIpPrefix specified.</span></span>
<span data-ttu-id="22f3c-126">이 옵션은 'Standard' SKU 및 'Static' AllocationMethod에서만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-126">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

### <span data-ttu-id="22f3c-127">예제 5: 새 전역 공용 IP 주소 만들기</span><span class="sxs-lookup"><span data-stu-id="22f3c-127">Example 5: Create a new global public IP address</span></span>
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $domainNameLabel -Location $location -Sku Standard -Tier Global
```

<span data-ttu-id="22f3c-128">이 명령은 새 전역 공용 IP 주소 리소스를 만듭니다. 이 리소스의 공용 IP 주소를 $dnsPrefix.$location.cloudapp.azure.com에 대한 DNS 레코드가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-128">This command creates a new global public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="22f3c-129">전역 공용 IP 주소는 이 리소스에 즉시 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-129">A global public IP address is immediately allocated to this resource.</span></span>
<span data-ttu-id="22f3c-130">이 옵션은 'Standard' SKU 및 'Static' AllocationMethod에서만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-130">This option is only supported for the 'Standard' Sku and 'Static' AllocationMethod.</span></span>

## <span data-ttu-id="22f3c-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22f3c-131">PARAMETERS</span></span>

### <span data-ttu-id="22f3c-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="22f3c-132">-AllocationMethod</span></span>
<span data-ttu-id="22f3c-133">공용 IP 주소를 할당할 메서드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-133">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="22f3c-134">이 매개 변수에 허용되는 값은 정적 또는 동적입니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-134">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="22f3c-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22f3c-135">-AsJob</span></span>
<span data-ttu-id="22f3c-136">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="22f3c-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22f3c-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22f3c-137">-DefaultProfile</span></span>
<span data-ttu-id="22f3c-138">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22f3c-139">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="22f3c-139">-DomainNameLabel</span></span>
<span data-ttu-id="22f3c-140">공용 IP 주소에 대한 상대 DNS 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-140">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="22f3c-141">-Force</span><span class="sxs-lookup"><span data-stu-id="22f3c-141">-Force</span></span>
<span data-ttu-id="22f3c-142">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="22f3c-143">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="22f3c-143">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="22f3c-144">유휴 시간(분)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-144">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="22f3c-145">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="22f3c-145">-IpAddressVersion</span></span>
<span data-ttu-id="22f3c-146">IP 주소의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-146">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="22f3c-147">-IpTag</span><span class="sxs-lookup"><span data-stu-id="22f3c-147">-IpTag</span></span>
<span data-ttu-id="22f3c-148">IpTag 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-148">IpTag List.</span></span>

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

### <span data-ttu-id="22f3c-149">-Location</span><span class="sxs-lookup"><span data-stu-id="22f3c-149">-Location</span></span>
<span data-ttu-id="22f3c-150">공용 IP 주소를 만들 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-150">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="22f3c-151">-Name</span><span class="sxs-lookup"><span data-stu-id="22f3c-151">-Name</span></span>
<span data-ttu-id="22f3c-152">이 cmdlet에서 만드는 공용 IP 주소의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-152">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="22f3c-153">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="22f3c-153">-PublicIpPrefix</span></span>
<span data-ttu-id="22f3c-154">공용 IP 주소를 할당할 PSPublicIpPrefix를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-154">Specifies the PSPublicIpPrefix from which to allocate the public IP address.</span></span>

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

### <span data-ttu-id="22f3c-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22f3c-155">-ResourceGroupName</span></span>
<span data-ttu-id="22f3c-156">공용 IP 주소를 만들 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-156">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="22f3c-157">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="22f3c-157">-ReverseFqdn</span></span>
<span data-ttu-id="22f3c-158">역방향 FQDN(정식 도메인 이름)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-158">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="22f3c-159">-Sku</span><span class="sxs-lookup"><span data-stu-id="22f3c-159">-Sku</span></span>
<span data-ttu-id="22f3c-160">공용 IP SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-160">The public IP Sku name.</span></span>

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

### <span data-ttu-id="22f3c-161">-Tag</span><span class="sxs-lookup"><span data-stu-id="22f3c-161">-Tag</span></span>
<span data-ttu-id="22f3c-162">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-162">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="22f3c-163">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="22f3c-163">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="22f3c-164">-Tier</span><span class="sxs-lookup"><span data-stu-id="22f3c-164">-Tier</span></span>
<span data-ttu-id="22f3c-165">공용 IP SKU 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-165">The public IP Sku Tier.</span></span>

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

### <span data-ttu-id="22f3c-166">-Zone</span><span class="sxs-lookup"><span data-stu-id="22f3c-166">-Zone</span></span>
<span data-ttu-id="22f3c-167">리소스에 할당된 IP를 표시하는 가용성 영역 목록이 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-167">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="22f3c-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22f3c-168">-Confirm</span></span>
<span data-ttu-id="22f3c-169">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22f3c-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22f3c-170">-WhatIf</span></span>
<span data-ttu-id="22f3c-171">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="22f3c-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22f3c-172">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22f3c-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22f3c-173">CommonParameters</span></span>
<span data-ttu-id="22f3c-174">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="22f3c-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22f3c-175">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="22f3c-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22f3c-176">입력</span><span class="sxs-lookup"><span data-stu-id="22f3c-176">INPUTS</span></span>

### <span data-ttu-id="22f3c-177">System.String</span><span class="sxs-lookup"><span data-stu-id="22f3c-177">System.String</span></span>

### <span data-ttu-id="22f3c-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span><span class="sxs-lookup"><span data-stu-id="22f3c-178">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]</span></span>

### <span data-ttu-id="22f3c-179">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="22f3c-179">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

### <span data-ttu-id="22f3c-180">System.Int32</span><span class="sxs-lookup"><span data-stu-id="22f3c-180">System.Int32</span></span>

### <span data-ttu-id="22f3c-181">System.String[]</span><span class="sxs-lookup"><span data-stu-id="22f3c-181">System.String[]</span></span>

### <span data-ttu-id="22f3c-182">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="22f3c-182">System.Collections.Hashtable</span></span>

## <span data-ttu-id="22f3c-183">출력</span><span class="sxs-lookup"><span data-stu-id="22f3c-183">OUTPUTS</span></span>

### <span data-ttu-id="22f3c-184">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="22f3c-184">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="22f3c-185">참고 사항</span><span class="sxs-lookup"><span data-stu-id="22f3c-185">NOTES</span></span>

## <span data-ttu-id="22f3c-186">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22f3c-186">RELATED LINKS</span></span>

[<span data-ttu-id="22f3c-187">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="22f3c-187">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="22f3c-188">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="22f3c-188">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="22f3c-189">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="22f3c-189">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)
