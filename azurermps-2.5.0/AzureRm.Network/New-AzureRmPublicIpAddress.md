---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: 032090bb494718a6420f54960106fe9c5fa9871c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881802"
---
# <span data-ttu-id="03c83-101">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="03c83-101">New-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="03c83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03c83-102">SYNOPSIS</span></span>
<span data-ttu-id="03c83-103">공용 IP 주소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-103">Creates a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03c83-104">구문과</span><span class="sxs-lookup"><span data-stu-id="03c83-104">SYNTAX</span></span>

```
New-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03c83-105">설명은</span><span class="sxs-lookup"><span data-stu-id="03c83-105">DESCRIPTION</span></span>
<span data-ttu-id="03c83-106">**새 AzureRmPublicIpAddress** cmdlet은 공용 IP 주소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-106">The **New-AzureRmPublicIpAddress** cmdlet creates a public IP address.</span></span>

## <span data-ttu-id="03c83-107">예제의</span><span class="sxs-lookup"><span data-stu-id="03c83-107">EXAMPLES</span></span>

### <span data-ttu-id="03c83-108">1: 새 공용 IP 주소 만들기</span><span class="sxs-lookup"><span data-stu-id="03c83-108">1: Create a new public IP address</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

<span data-ttu-id="03c83-109">이 명령은 새 공용 IP 주소 리소스를 만듭니다. $DnsPrefix에 대 한 DNS 레코드를 만듭니다. cloudapp.azure.com는이 리소스의 공개 IP 주소를 가리킵니다. $location.</span><span class="sxs-lookup"><span data-stu-id="03c83-109">This command creates a new public IP address resource.A DNS record is created for $dnsPrefix.$location.cloudapp.azure.com pointing to the public IP address of this resource.</span></span> <span data-ttu-id="03c83-110">-AllocationMethod가 ' Static '으로 지정 되어 있으므로 공용 IP 주소가이 리소스에 즉시 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-110">A public IP address is immediately allocated to this resource as the -AllocationMethod is specified as 'Static'.</span></span> <span data-ttu-id="03c83-111">' 동적 '으로 지정 되는 경우, 공용 IP 주소는 연결 된 리소스 (예: VM 또는 부하 분산 장치)를 시작 (또는 만드는 경우)에만 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-111">If it is specified as 'Dynamic', a public IP address gets allocated only when you start (or create) the associated resource (like a VM or load balancer).</span></span>

### <span data-ttu-id="03c83-112">2: 역방향 FQDN을 사용 하 여 공용 IP 주소 만들기</span><span class="sxs-lookup"><span data-stu-id="03c83-112">2: Create a public IP address with a reverse FQDN</span></span>
```
$publicIp = New-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

<span data-ttu-id="03c83-113">이 명령은 새 공용 IP 주소 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-113">This command creates a new public IP address resource.</span></span> <span data-ttu-id="03c83-114">-ReverseFqdn 매개 변수를 사용 하는 경우 Azure는이 리소스에 할당 된 공용 IP 주소에 대 한 DNS PTR 레코드 (역방향 조회)를 만들어 명령에 지정 된 $customFqdn를 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-114">With the -ReverseFqdn parameter, Azure creates a DNS PTR record (reverse-lookup) for the public IP address allocated to this resource, pointing to the $customFqdn specified in the command.</span></span> <span data-ttu-id="03c83-115">사전 필수 요소로 서 $customFqdn (예를 들어 webapp.contoso.com)에는 $dnsPrefix $location. cloudapp.azure.com를 가리키는 DNS CNAME 레코드 (정방향 조회)가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-115">As a pre-requisite, the $customFqdn (say webapp.contoso.com) should have a DNS CNAME record (forward-lookup) pointing to $dnsPrefix.$location.cloudapp.azure.com.</span></span>

## <span data-ttu-id="03c83-116">변수</span><span class="sxs-lookup"><span data-stu-id="03c83-116">PARAMETERS</span></span>

### <span data-ttu-id="03c83-117">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="03c83-117">-AllocationMethod</span></span>
<span data-ttu-id="03c83-118">공용 IP 주소를 할당 하는 데 사용할 메서드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-118">Specifies the method with which to allocate the public IP address.</span></span>
<span data-ttu-id="03c83-119">이 매개 변수에 허용 되는 값은 Static 또는 Dynamic입니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-119">The acceptable values for this parameter are: Static or Dynamic.</span></span>

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

### <span data-ttu-id="03c83-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03c83-120">-AsJob</span></span>
<span data-ttu-id="03c83-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="03c83-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03c83-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c83-122">-DefaultProfile</span></span>
<span data-ttu-id="03c83-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03c83-124">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="03c83-124">-DomainNameLabel</span></span>
<span data-ttu-id="03c83-125">공용 IP 주소에 대 한 상대 DNS 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-125">Specifies the relative DNS name for a public IP address.</span></span>

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

### <span data-ttu-id="03c83-126">-Force</span><span class="sxs-lookup"><span data-stu-id="03c83-126">-Force</span></span>
<span data-ttu-id="03c83-127">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="03c83-128">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="03c83-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="03c83-129">유휴 시간 제한 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-129">Specifies the idle time-out, in minutes.</span></span>

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

### <span data-ttu-id="03c83-130">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="03c83-130">-IpAddressVersion</span></span>
<span data-ttu-id="03c83-131">IP 주소의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-131">Specifies the version of the IP address.</span></span>

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

### <span data-ttu-id="03c83-132">-위치</span><span class="sxs-lookup"><span data-stu-id="03c83-132">-Location</span></span>
<span data-ttu-id="03c83-133">공용 IP 주소를 만들 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-133">Specifies the region in which to create a public IP address.</span></span>

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

### <span data-ttu-id="03c83-134">-이름</span><span class="sxs-lookup"><span data-stu-id="03c83-134">-Name</span></span>
<span data-ttu-id="03c83-135">이 cmdlet이 만드는 공용 IP 주소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-135">Specifies the name of the public IP address that this cmdlet creates.</span></span>

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

### <span data-ttu-id="03c83-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03c83-136">-ResourceGroupName</span></span>
<span data-ttu-id="03c83-137">공용 IP 주소를 만들 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-137">Specifies the name of the resource group in which to create a public IP address.</span></span>

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

### <span data-ttu-id="03c83-138">-ReverseFqdn</span><span class="sxs-lookup"><span data-stu-id="03c83-138">-ReverseFqdn</span></span>
<span data-ttu-id="03c83-139">역방향 FQDN (정규화 된 도메인 이름)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-139">Specifies a reverse fully qualified domain name (FQDN).</span></span>

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

### <span data-ttu-id="03c83-140">-Sku</span><span class="sxs-lookup"><span data-stu-id="03c83-140">-Sku</span></span>
<span data-ttu-id="03c83-141">공용 IP Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-141">The public IP Sku name.</span></span>

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

### <span data-ttu-id="03c83-142">태그</span><span class="sxs-lookup"><span data-stu-id="03c83-142">-Tag</span></span>
<span data-ttu-id="03c83-143">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="03c83-144">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="03c83-144">For example:</span></span>

<span data-ttu-id="03c83-145">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="03c83-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="03c83-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="03c83-146">-Zone</span></span>
<span data-ttu-id="03c83-147">리소스에 대해 할당 된 IP를 나타내는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-147">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="03c83-148">-확인</span><span class="sxs-lookup"><span data-stu-id="03c83-148">-Confirm</span></span>
<span data-ttu-id="03c83-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03c83-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03c83-150">-WhatIf</span></span>
<span data-ttu-id="03c83-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03c83-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03c83-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c83-153">CommonParameters</span></span>
<span data-ttu-id="03c83-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="03c83-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c83-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03c83-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c83-156">입력</span><span class="sxs-lookup"><span data-stu-id="03c83-156">INPUTS</span></span>

## <span data-ttu-id="03c83-157">출력</span><span class="sxs-lookup"><span data-stu-id="03c83-157">OUTPUTS</span></span>

### <span data-ttu-id="03c83-158">PSPublicIpAddress에 대 한.</span><span class="sxs-lookup"><span data-stu-id="03c83-158">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="03c83-159">상속자</span><span class="sxs-lookup"><span data-stu-id="03c83-159">NOTES</span></span>

## <span data-ttu-id="03c83-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03c83-160">RELATED LINKS</span></span>

[<span data-ttu-id="03c83-161">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="03c83-161">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="03c83-162">제거-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="03c83-162">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="03c83-163">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="03c83-163">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)
