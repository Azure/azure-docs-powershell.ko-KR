---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: a5f3871f0ab63d875c2a0389c5585f0871fb0cb9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875958"
---
# <span data-ttu-id="3186c-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="3186c-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="3186c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3186c-102">SYNOPSIS</span></span>
<span data-ttu-id="3186c-103">로컬 레코드 집합 개체에 DNS 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="3186c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3186c-104">SYNTAX</span></span>

### <span data-ttu-id="3186c-105">에서</span><span class="sxs-lookup"><span data-stu-id="3186c-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="3186c-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="3186c-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="3186c-107">NS</span><span class="sxs-lookup"><span data-stu-id="3186c-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="3186c-108">멕시코</span><span class="sxs-lookup"><span data-stu-id="3186c-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="3186c-109">PTR 레코드로</span><span class="sxs-lookup"><span data-stu-id="3186c-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="3186c-110">라는</span><span class="sxs-lookup"><span data-stu-id="3186c-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="3186c-111">SRV</span><span class="sxs-lookup"><span data-stu-id="3186c-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="3186c-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="3186c-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="3186c-113">설명은</span><span class="sxs-lookup"><span data-stu-id="3186c-113">DESCRIPTION</span></span>
<span data-ttu-id="3186c-114">**Add-AzDnsRecordConfig** CMDLET은 DNS (Domain Name System) 레코드를 **레코드 집합** 개체에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-114">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="3186c-115">**레코드 집합** 개체는 오프 라인 개체 이며, MICROSOFT Azure DNS 서비스에 대 한 변경 내용을 유지 하기 위해 Set-AzDnsRecordSet cmdlet을 실행 한 후에만 DNS 응답을 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="3186c-116">SOA 레코드는 DNS 영역을 만들 때 만들어지며 DNS 영역이 삭제 되 면 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-116">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="3186c-117">SOA 레코드를 추가 하거나 제거할 수는 없지만 편집할 수는 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-117">You cannot add or remove SOA records, but you can edit them.</span></span>

<span data-ttu-id="3186c-118">이 cmdlet에는 **RecordSet** 개체를 매개 변수로 전달 하거나 파이프라인 연산자를 사용 하 여 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-118">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="3186c-119">예제의</span><span class="sxs-lookup"><span data-stu-id="3186c-119">EXAMPLES</span></span>

### <span data-ttu-id="3186c-120">예제 1: 레코드 집합에 A 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="3186c-120">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="3186c-121">이 예제에서는 A 레코드를 기존 레코드 집합에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-121">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="3186c-122">예제 2: 레코드 집합에 AAAA 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="3186c-122">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="3186c-123">다음은 기존 레코드 집합에 AAAA 레코드를 추가 하는 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-123">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="3186c-124">예제 3: 레코드 집합에 CNAME 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="3186c-124">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="3186c-125">이 예제에서는 기존 레코드 집합에 CNAME 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-125">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="3186c-126">CNAME 레코드 집합에는 레코드가 하나만 포함 될 수 있으므로, 처음에는 빈 레코드 집합 이거나, Remove-AzDnsRecordConfig를 사용 하 여 기존 레코드를 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-126">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="3186c-127">예제 4: 레코드 집합에 MX 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="3186c-127">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="3186c-128">이 예제에서는 기존 레코드 집합에 MX 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-128">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="3186c-129">레코드 이름 "@"은 (는) apex 영역에서 레코드 집합을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-129">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="3186c-130">예제 5: 레코드 집합에 NS 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="3186c-130">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="3186c-131">이 예제에서는 기존 레코드 집합에 NS 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-131">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="3186c-132">예제 6: 레코드 집합에 PTR 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="3186c-132">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="3186c-133">이 예제에서는 기존 레코드 집합에 PTR 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-133">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="3186c-134">예제 7: 레코드 집합에 SRV 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="3186c-134">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="3186c-135">이 예제에서는 기존 레코드 집합에 SRV 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-135">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="3186c-136">예제 8: 레코드 집합에 TXT 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="3186c-136">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="3186c-137">이 예제에서는 기존 레코드 집합에 TXT 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-137">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="3186c-138">변수</span><span class="sxs-lookup"><span data-stu-id="3186c-138">PARAMETERS</span></span>

### <span data-ttu-id="3186c-139">-Cname</span><span class="sxs-lookup"><span data-stu-id="3186c-139">-Cname</span></span>
<span data-ttu-id="3186c-140">CNAME (정식 이름) 레코드에 대 한 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-140">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-141">-Exchange</span><span class="sxs-lookup"><span data-stu-id="3186c-141">-Exchange</span></span>
<span data-ttu-id="3186c-142">메일 교환 (MX) 레코드의 메일 교환 서버 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-142">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-143">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="3186c-143">-Ipv4Address</span></span>
<span data-ttu-id="3186c-144">A 레코드에 대 한 IPv4 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-144">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: String
Parameter Sets: A
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-145">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="3186c-145">-Ipv6Address</span></span>
<span data-ttu-id="3186c-146">AAAA 레코드에 대 한 IPv6 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-146">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-147">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="3186c-147">-Nsdname</span></span>
<span data-ttu-id="3186c-148">NS (이름 서버) 레코드에 대 한 이름 서버 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-148">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-149">-포트</span><span class="sxs-lookup"><span data-stu-id="3186c-149">-Port</span></span>
<span data-ttu-id="3186c-150">서비스 (SRV) 레코드의 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-150">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-151">-기본 설정</span><span class="sxs-lookup"><span data-stu-id="3186c-151">-Preference</span></span>
<span data-ttu-id="3186c-152">MX 레코드에 대 한 기본 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-152">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-153">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="3186c-153">-Priority</span></span>
<span data-ttu-id="3186c-154">SRV 레코드에 대 한 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-154">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-155">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="3186c-155">-Ptrdname</span></span>
<span data-ttu-id="3186c-156">PTR (포인터 리소스) 레코드의 대상 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-156">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-157">-레코드 집합</span><span class="sxs-lookup"><span data-stu-id="3186c-157">-RecordSet</span></span>
<span data-ttu-id="3186c-158">편집할 **레코드 집합** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-158">Specifies the **RecordSet** object to edit.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-159">-대상</span><span class="sxs-lookup"><span data-stu-id="3186c-159">-Target</span></span>
<span data-ttu-id="3186c-160">SRV 레코드의 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-160">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-161">-값</span><span class="sxs-lookup"><span data-stu-id="3186c-161">-Value</span></span>
<span data-ttu-id="3186c-162">TXT 레코드에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-162">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-163">-중량</span><span class="sxs-lookup"><span data-stu-id="3186c-163">-Weight</span></span>
<span data-ttu-id="3186c-164">SRV 레코드의 가중치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-164">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3186c-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3186c-165">CommonParameters</span></span>
<span data-ttu-id="3186c-166">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3186c-167">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3186c-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3186c-168">입력</span><span class="sxs-lookup"><span data-stu-id="3186c-168">INPUTS</span></span>

### <span data-ttu-id="3186c-169">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3186c-169">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="3186c-170">**RecordSet** 개체를이 cmdlet에 파이프 하 여 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-170">You can pipe a **RecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="3186c-171">이는 **레코드 집합** 의 오프 라인 표현이 며, Set-AzDnsRecordSet cmdlet을 실행할 때까지 변경 내용이 DNS 응답을 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-171">This is an offline representation of the **RecordSet** , and changes to it do not change DNS responses until after you run the Set-AzDnsRecordSet cmdlet.</span></span>

## <span data-ttu-id="3186c-172">출력</span><span class="sxs-lookup"><span data-stu-id="3186c-172">OUTPUTS</span></span>

### <span data-ttu-id="3186c-173">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3186c-173">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="3186c-174">이 cmdlet은 수정 된 **레코드 집합** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-174">This cmdlet returns the modified **RecordSet** object.</span></span>
<span data-ttu-id="3186c-175">또한 전달 된 개체는 직접 수정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3186c-175">In addition, the object passed in is modified directly.</span></span>

## <span data-ttu-id="3186c-176">상속자</span><span class="sxs-lookup"><span data-stu-id="3186c-176">NOTES</span></span>

## <span data-ttu-id="3186c-177">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3186c-177">RELATED LINKS</span></span>

[<span data-ttu-id="3186c-178">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3186c-178">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="3186c-179">제거-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="3186c-179">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="3186c-180">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3186c-180">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
