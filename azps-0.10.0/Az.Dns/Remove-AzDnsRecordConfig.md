---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: e00b31783554b8ea70760809c36f23a6a62575ca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876767"
---
# <span data-ttu-id="6af7b-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="6af7b-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="6af7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6af7b-102">SYNOPSIS</span></span>
<span data-ttu-id="6af7b-103">로컬 레코드 집합 개체에서 DNS 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="6af7b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6af7b-104">SYNTAX</span></span>

### <span data-ttu-id="6af7b-105">에서</span><span class="sxs-lookup"><span data-stu-id="6af7b-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="6af7b-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="6af7b-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="6af7b-107">NS</span><span class="sxs-lookup"><span data-stu-id="6af7b-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="6af7b-108">멕시코</span><span class="sxs-lookup"><span data-stu-id="6af7b-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="6af7b-109">PTR 레코드로</span><span class="sxs-lookup"><span data-stu-id="6af7b-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="6af7b-110">라는</span><span class="sxs-lookup"><span data-stu-id="6af7b-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="6af7b-111">SRV</span><span class="sxs-lookup"><span data-stu-id="6af7b-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="6af7b-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="6af7b-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="6af7b-113">설명은</span><span class="sxs-lookup"><span data-stu-id="6af7b-113">DESCRIPTION</span></span>
<span data-ttu-id="6af7b-114">**AzDnsRecordConfig** cmdlet은 레코드 집합에서 DNS (Domain Name System) 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-114">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="6af7b-115">**레코드 집합** 개체는 오프 라인 개체 이며, MICROSOFT Azure DNS 서비스에 대 한 변경 내용을 유지 하기 위해 Set-AzDnsRecordSet cmdlet을 실행 한 후에만 DNS 응답을 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="6af7b-116">레코드를 제거 하려면 해당 레코드 종류에 대 한 모든 필드가 정확히 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-116">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="6af7b-117">SOA 레코드를 추가 하거나 제거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-117">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="6af7b-118">SOA 레코드는 dns 영역이 생성 될 때 자동으로 만들어지고 DNS 영역이 삭제 되 면 자동으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-118">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>

<span data-ttu-id="6af7b-119">이 cmdlet에는 **RecordSet** 개체를 매개 변수로 전달 하거나 파이프라인 연산자를 사용 하 여 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="6af7b-120">예제의</span><span class="sxs-lookup"><span data-stu-id="6af7b-120">EXAMPLES</span></span>

### <span data-ttu-id="6af7b-121">예제 1: 레코드 집합에서 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="6af7b-121">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="6af7b-122">이 예제에서는 기존 레코드 집합에서 A 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-122">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="6af7b-123">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-123">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="6af7b-124">레코드 집합을 완전히 제거 하려면 제거-AzDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6af7b-124">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="6af7b-125">예제 2: 레코드 집합에서 AAAA 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="6af7b-125">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="6af7b-126">이 예제에서는 기존 레코드 집합에서 AAAA 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-126">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="6af7b-127">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-127">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="6af7b-128">레코드 집합을 완전히 제거 하려면 제거-AzDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6af7b-128">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="6af7b-129">예제 3: 레코드 집합에서 CNAME 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="6af7b-129">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="6af7b-130">이 예제에서는 기존 레코드 집합에서 CNAME 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-130">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="6af7b-131">CNAME 레코드 집합에는 레코드가 하나만 포함 될 수 있으므로 결과는 빈 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-131">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="6af7b-132">예제 4: 레코드 집합에서 MX 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="6af7b-132">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="6af7b-133">이 예제에서는 기존 레코드 집합에서 MX 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-133">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="6af7b-134">레코드 이름 "@"은 (는) apex 영역에서 레코드 집합을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-134">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="6af7b-135">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-135">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="6af7b-136">레코드 집합을 완전히 제거 하려면 제거-AzDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6af7b-136">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="6af7b-137">예제 5: 레코드 집합에서 NS 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="6af7b-137">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="6af7b-138">이 예제에서는 기존 레코드 집합에서 NS 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-138">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="6af7b-139">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-139">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="6af7b-140">레코드 집합을 완전히 제거 하려면 제거-AzDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6af7b-140">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="6af7b-141">예제 6: 레코드 집합에서 PTR 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="6af7b-141">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="6af7b-142">이 예제에서는 기존 레코드 집합에서 PTR 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-142">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="6af7b-143">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-143">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="6af7b-144">레코드 집합을 완전히 제거 하려면 제거-AzDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6af7b-144">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="6af7b-145">예제 7: 레코드 집합에서 SRV 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="6af7b-145">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="6af7b-146">이 예제에서는 기존 레코드 집합에서 SRV 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-146">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="6af7b-147">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-147">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="6af7b-148">레코드 집합을 완전히 제거 하려면 제거-AzDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6af7b-148">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="6af7b-149">예제 8: 레코드 집합에서 TXT 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="6af7b-149">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="6af7b-150">이 예제에서는 기존 레코드 집합에서 TXT 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-150">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="6af7b-151">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-151">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="6af7b-152">레코드 집합을 완전히 제거 하려면 제거-AzDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6af7b-152">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="6af7b-153">변수</span><span class="sxs-lookup"><span data-stu-id="6af7b-153">PARAMETERS</span></span>

### <span data-ttu-id="6af7b-154">-Cname</span><span class="sxs-lookup"><span data-stu-id="6af7b-154">-Cname</span></span>
<span data-ttu-id="6af7b-155">CNAME (정식 이름) 레코드에 대 한 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-155">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="6af7b-156">-Exchange</span><span class="sxs-lookup"><span data-stu-id="6af7b-156">-Exchange</span></span>
<span data-ttu-id="6af7b-157">메일 교환 (MX) 레코드의 메일 교환 서버 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-157">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="6af7b-158">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="6af7b-158">-Ipv4Address</span></span>
<span data-ttu-id="6af7b-159">A 레코드에 대 한 IPv4 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-159">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="6af7b-160">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="6af7b-160">-Ipv6Address</span></span>
<span data-ttu-id="6af7b-161">AAAA 레코드에 대 한 IPv6 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-161">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="6af7b-162">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="6af7b-162">-Nsdname</span></span>
<span data-ttu-id="6af7b-163">NS (이름 서버) 레코드에 대 한 이름 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-163">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="6af7b-164">-포트</span><span class="sxs-lookup"><span data-stu-id="6af7b-164">-Port</span></span>
<span data-ttu-id="6af7b-165">서비스 (SRV) 레코드의 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-165">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="6af7b-166">-기본 설정</span><span class="sxs-lookup"><span data-stu-id="6af7b-166">-Preference</span></span>
<span data-ttu-id="6af7b-167">MX 레코드에 대 한 기본 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-167">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="6af7b-168">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="6af7b-168">-Priority</span></span>
<span data-ttu-id="6af7b-169">SRV 레코드에 대 한 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-169">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="6af7b-170">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="6af7b-170">-Ptrdname</span></span>
<span data-ttu-id="6af7b-171">포인터 (PTR) 레코드의 대상 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-171">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="6af7b-172">-레코드 집합</span><span class="sxs-lookup"><span data-stu-id="6af7b-172">-RecordSet</span></span>
<span data-ttu-id="6af7b-173">제거할 레코드가 포함 된 **레코드 집합** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-173">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="6af7b-174">-대상</span><span class="sxs-lookup"><span data-stu-id="6af7b-174">-Target</span></span>
<span data-ttu-id="6af7b-175">SRV 레코드의 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-175">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="6af7b-176">-값</span><span class="sxs-lookup"><span data-stu-id="6af7b-176">-Value</span></span>
<span data-ttu-id="6af7b-177">TXT 레코드에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-177">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="6af7b-178">-중량</span><span class="sxs-lookup"><span data-stu-id="6af7b-178">-Weight</span></span>
<span data-ttu-id="6af7b-179">SRV 레코드의 가중치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-179">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="6af7b-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6af7b-180">CommonParameters</span></span>
<span data-ttu-id="6af7b-181">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6af7b-182">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6af7b-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6af7b-183">입력</span><span class="sxs-lookup"><span data-stu-id="6af7b-183">INPUTS</span></span>

### <span data-ttu-id="6af7b-184">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6af7b-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="6af7b-185">이 cmdlet에 **Dnsrecordset** 개체를 파이프 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-185">You can pipe a **DnsRecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="6af7b-186">이는 레코드 집합의 오프 라인 표현이 며, Set-AzDnsRecordSet을 실행 한 후에만 DNS 응답을 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-186">This is an offline representation of the record set and updates to it do not change DNS responses until after you run Set-AzDnsRecordSet.</span></span>

## <span data-ttu-id="6af7b-187">출력</span><span class="sxs-lookup"><span data-stu-id="6af7b-187">OUTPUTS</span></span>

### <span data-ttu-id="6af7b-188">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6af7b-188">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="6af7b-189">이 cmdlet은 수정 된 **레코드 집합** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6af7b-189">This cmdlet returns the modified **RecordSet** object.</span></span>

## <span data-ttu-id="6af7b-190">상속자</span><span class="sxs-lookup"><span data-stu-id="6af7b-190">NOTES</span></span>

## <span data-ttu-id="6af7b-191">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6af7b-191">RELATED LINKS</span></span>

[<span data-ttu-id="6af7b-192">추가-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="6af7b-192">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="6af7b-193">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6af7b-193">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="6af7b-194">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6af7b-194">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
