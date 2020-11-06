---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpAddress.md
ms.openlocfilehash: 98ea4632004787626237e5845f3c573b51a91934
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535959"
---
# <span data-ttu-id="83892-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="83892-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="83892-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83892-102">SYNOPSIS</span></span>
<span data-ttu-id="83892-103">공용 IP 주소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83892-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83892-104">구문과</span><span class="sxs-lookup"><span data-stu-id="83892-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83892-105">설명은</span><span class="sxs-lookup"><span data-stu-id="83892-105">DESCRIPTION</span></span>
<span data-ttu-id="83892-106">**새 AzureRmPublicIpAddress** cmdlet은 공용 IP 주소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83892-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="83892-107">예제의</span><span class="sxs-lookup"><span data-stu-id="83892-107">EXAMPLES</span></span>

### <span data-ttu-id="83892-108">1: 새 공용 IP 주소 만들기</span><span class="sxs-lookup"><span data-stu-id="83892-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="83892-109">이 명령은 새 공용 IP 주소 리소스를 만듭니다. $DnsPrefix에 대 한 DNS 레코드를 만듭니다. cloudapp.azure.com는이 리소스의 공개 IP 주소를 가리킵니다. $location.</span><span class="sxs-lookup"><span data-stu-id="83892-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="83892-110">-AllocationMethod가 ' Static '으로 지정 되어 있으므로 공용 IP 주소가이 리소스에 즉시 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83892-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="83892-111">' 동적 '으로 지정 되는 경우, 공용 IP 주소는 연결 된 리소스 (예: VM 또는 부하 분산 장치)를 시작 (또는 만드는 경우)에만 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83892-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="83892-112">2: 역방향 FQDN을 사용 하 여 공용 IP 주소 만들기</span><span class="sxs-lookup"><span data-stu-id="83892-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="83892-113">이 명령은 새 공용 IP 주소 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83892-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="83892-114">-ReverseFqdn 매개 변수를 사용 하는 경우 Azure는이 리소스에 할당 된 공용 IP 주소에 대 한 DNS PTR 레코드 (역방향 조회)를 만들어 명령에 지정 된 $customFqdn를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="83892-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="83892-115">사전 필수 요소로 서 $customFqdn (예를 들어 webapp.contoso.com)에는 $dnsPrefix $location. cloudapp.azure.com를 가리키는 DNS CNAME 레코드 (정방향 조회)가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="83892-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

### <span data-ttu-id="83892-116">3: IpTag를 사용 하 여 새 공용 IP 주소 만들기</span><span class="sxs-lookup"><span data-stu-id="83892-116">3: Create a new public IP address with IpTag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags ipTag
```

<span data-ttu-id="83892-117">이 명령은 새 공용 IP 주소 리소스를 만듭니다. $DnsPrefix에 대 한 DNS 레코드를 만듭니다. cloudapp.azure.com는이 리소스의 공개 IP 주소를 가리킵니다. $location.</span><span class="sxs-lookup"><span data-stu-id="83892-117">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="83892-118">-AllocationMethod가 ' Static '으로 지정 되어 있으므로 공용 IP 주소가이 리소스에 즉시 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83892-118">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="83892-119">' 동적 '으로 지정 되는 경우, 공용 IP 주소는 연결 된 리소스 (예: VM 또는 부하 분산 장치)를 시작 (또는 만드는 경우)에만 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83892-119">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span> <span data-ttu-id="83892-120">Iptag는 resource와 연결 된 특정 태그에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="83892-120">An Iptag is used to specific the Tags associated with resource.</span></span> <span data-ttu-id="83892-121">New-AzureRmPublicIpTag를 사용 하 여 iptag를 지정 하 고-Iptag를 통해 입력으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83892-121">Iptag can be specified using New-AzureRmPublicIpTag and passed as input through -IpTags.</span></span>

## <span data-ttu-id="83892-122">변수</span><span class="sxs-lookup"><span data-stu-id="83892-122">PARAMETERS</span></span>

### <span data-ttu-id="83892-123">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="83892-123">-AllocationMethod</span></span>
<span data-ttu-id="83892-124">공용 IP 주소를 할당 하는 데 사용할 메서드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83892-124">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="83892-125">이 매개 변수에 허용 되는 값은 Static 또는 Dynamic입니다.</span><span class="sxs-lookup"><span data-stu-id="83892-125">The acceptable values for this parameter are: Static or Dynamic.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83892-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83892-126">-AsJob</span></span>
<span data-ttu-id="83892-127">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="83892-127">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83892-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83892-128">-DefaultProfile</span></span>
<span data-ttu-id="83892-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83892-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83892-130">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="83892-130">-DomainNameLabel</span></span>
<span data-ttu-id="83892-131">공용 IP 주소에 대 한 상대 DNS 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83892-131">Specifies the relative DNS name for a public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83892-132">-Force</span><span class="sxs-lookup"><span data-stu-id="83892-132">-Force</span></span>
<span data-ttu-id="83892-133">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="83892-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83892-134">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="83892-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="83892-135">유휴 시간 제한 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83892-135">Specifies the idle time-out, in minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83892-136">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="83892-136">-IpAddressVersion</span></span>
<span data-ttu-id="83892-137">IP 주소의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83892-137">Specifies the version of the IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83892-138">-IpTag</span><span class="sxs-lookup"><span data-stu-id="83892-138">-IpTag</span></span>
<span data-ttu-id="83892-139">IpTag 목록.</span><span class="sxs-lookup"><span data-stu-id="83892-139">IpTag List.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpTag]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83892-140">-위치</span><span class="sxs-lookup"><span data-stu-id="83892-140">-Location</span></span>
<span data-ttu-id="83892-141">공용 IP 주소를 만들 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83892-141">Specifies the region in which to create a public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83892-142">-이름</span><span class="sxs-lookup"><span data-stu-id="83892-142">-Name</span></span>
<span data-ttu-id="83892-143">이 cmdlet이 만드는 공용 IP 주소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83892-143">Specifies the name of the public IP address that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83892-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83892-144">-ResourceGroupName</span></span>
<span data-ttu-id="83892-145">공용 IP 주소를 만들 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83892-145">Specifies the name of the resource group in which to create a public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83892-146">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="83892-146">-ReverseFqdn</span></span>
<span data-ttu-id="83892-147">역방향 FQDN (정규화 된 도메인 이름)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83892-147">Specifies a reverse fully qualified domain name (FQDN).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83892-148">-Sku</span><span class="sxs-lookup"><span data-stu-id="83892-148">-Sku</span></span>
<span data-ttu-id="83892-149">공용 IP Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83892-149">The public IP Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83892-150">태그</span><span class="sxs-lookup"><span data-stu-id="83892-150">-Tag</span></span>
<span data-ttu-id="83892-151">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="83892-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="83892-152">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="83892-152">For example:</span></span>

<span data-ttu-id="83892-153">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="83892-153">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83892-154">-Zone</span><span class="sxs-lookup"><span data-stu-id="83892-154">-Zone</span></span>
<span data-ttu-id="83892-155">리소스에 대해 할당 된 IP를 나타내는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="83892-155">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="83892-156">-확인</span><span class="sxs-lookup"><span data-stu-id="83892-156">-Confirm</span></span>
<span data-ttu-id="83892-157">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="83892-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83892-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83892-158">-WhatIf</span></span>
<span data-ttu-id="83892-159">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="83892-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83892-160">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83892-160">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83892-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83892-161">CommonParameters</span></span>
<span data-ttu-id="83892-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="83892-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83892-163">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83892-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83892-164">입력</span><span class="sxs-lookup"><span data-stu-id="83892-164">INPUTS</span></span>

### <span data-ttu-id="83892-165">않아야</span><span class="sxs-lookup"><span data-stu-id="83892-165">None</span></span>
<span data-ttu-id="83892-166">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83892-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="83892-167">출력</span><span class="sxs-lookup"><span data-stu-id="83892-167">OUTPUTS</span></span>

### <span data-ttu-id="83892-168">PSPublicIpAddress에 대 한.</span><span class="sxs-lookup"><span data-stu-id="83892-168">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="83892-169">상속자</span><span class="sxs-lookup"><span data-stu-id="83892-169">NOTES</span></span>

## <span data-ttu-id="83892-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83892-170">RELATED LINKS</span></span>

[<span data-ttu-id="83892-171">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="83892-171">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="83892-172">제거-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="83892-172">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="83892-173">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="83892-173">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
