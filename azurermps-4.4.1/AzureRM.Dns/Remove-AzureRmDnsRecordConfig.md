---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordConfig.md
ms.openlocfilehash: 97d87464f49d9f43d6ab6fb08d0cd8034560a108
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534103"
---
# <span data-ttu-id="68203-101">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="68203-101">Remove-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="68203-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68203-102">SYNOPSIS</span></span>
<span data-ttu-id="68203-103">로컬 레코드 집합 개체에서 DNS 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-103">Removes a DNS record from a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68203-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68203-104">SYNTAX</span></span>

### <span data-ttu-id="68203-105">에서</span><span class="sxs-lookup"><span data-stu-id="68203-105">A</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68203-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="68203-106">AAAA</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68203-107">NS</span><span class="sxs-lookup"><span data-stu-id="68203-107">NS</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68203-108">멕시코</span><span class="sxs-lookup"><span data-stu-id="68203-108">MX</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68203-109">PTR 레코드로</span><span class="sxs-lookup"><span data-stu-id="68203-109">PTR</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68203-110">라는</span><span class="sxs-lookup"><span data-stu-id="68203-110">TXT</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68203-111">SRV</span><span class="sxs-lookup"><span data-stu-id="68203-111">SRV</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68203-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="68203-112">CNAME</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68203-113">설명은</span><span class="sxs-lookup"><span data-stu-id="68203-113">DESCRIPTION</span></span>
<span data-ttu-id="68203-114">**AzureRmDnsRecordConfig** cmdlet은 레코드 집합에서 DNS (Domain Name System) 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-114">The **Remove-AzureRmDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="68203-115">**레코드 집합** 개체는 오프 라인 개체 이며, MICROSOFT Azure DNS 서비스에 대 한 변경 내용을 유지 하기 위해 Set-AzureRmDnsRecordSet cmdlet을 실행 한 후에만 DNS 응답을 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68203-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="68203-116">레코드를 제거 하려면 해당 레코드 종류에 대 한 모든 필드가 정확히 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-116">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="68203-117">SOA 레코드를 추가 하거나 제거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="68203-117">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="68203-118">SOA 레코드는 dns 영역이 생성 될 때 자동으로 만들어지고 DNS 영역이 삭제 되 면 자동으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="68203-118">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>

<span data-ttu-id="68203-119">이 cmdlet에는 **RecordSet** 개체를 매개 변수로 전달 하거나 파이프라인 연산자를 사용 하 여 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68203-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="68203-120">예제의</span><span class="sxs-lookup"><span data-stu-id="68203-120">EXAMPLES</span></span>

### <span data-ttu-id="68203-121">예제 1: 레코드 집합에서 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="68203-121">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="68203-122">이 예제에서는 기존 레코드 집합에서 A 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-122">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="68203-123">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="68203-123">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="68203-124">레코드 집합을 완전히 제거 하려면 제거-AzureRmDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="68203-124">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="68203-125">예제 2: 레코드 집합에서 AAAA 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="68203-125">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="68203-126">이 예제에서는 기존 레코드 집합에서 AAAA 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-126">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="68203-127">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="68203-127">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="68203-128">레코드 집합을 완전히 제거 하려면 제거-AzureRmDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="68203-128">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="68203-129">예제 3: 레코드 집합에서 CNAME 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="68203-129">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="68203-130">이 예제에서는 기존 레코드 집합에서 CNAME 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-130">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="68203-131">CNAME 레코드 집합에는 레코드가 하나만 포함 될 수 있으므로 결과는 빈 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="68203-131">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="68203-132">예제 4: 레코드 집합에서 MX 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="68203-132">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="68203-133">이 예제에서는 기존 레코드 집합에서 MX 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-133">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="68203-134">레코드 이름 "@"은 (는) apex 영역에서 레코드 집합을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="68203-134">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="68203-135">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="68203-135">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="68203-136">레코드 집합을 완전히 제거 하려면 제거-AzureRmDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="68203-136">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="68203-137">예제 5: 레코드 집합에서 NS 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="68203-137">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="68203-138">이 예제에서는 기존 레코드 집합에서 NS 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-138">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="68203-139">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="68203-139">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="68203-140">레코드 집합을 완전히 제거 하려면 제거-AzureRmDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="68203-140">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="68203-141">예제 6: 레코드 집합에서 PTR 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="68203-141">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="68203-142">이 예제에서는 기존 레코드 집합에서 PTR 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-142">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="68203-143">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="68203-143">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="68203-144">레코드 집합을 완전히 제거 하려면 제거-AzureRmDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="68203-144">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="68203-145">예제 7: 레코드 집합에서 SRV 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="68203-145">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="68203-146">이 예제에서는 기존 레코드 집합에서 SRV 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-146">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="68203-147">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="68203-147">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="68203-148">레코드 집합을 완전히 제거 하려면 제거-AzureRmDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="68203-148">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="68203-149">예제 8: 레코드 집합에서 TXT 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="68203-149">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Value "This is a TXT Record"  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="68203-150">이 예제에서는 기존 레코드 집합에서 TXT 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-150">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="68203-151">레코드 집합의 유일한 레코드 이면 빈 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="68203-151">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="68203-152">레코드 집합을 완전히 제거 하려면 제거-AzureRmDnsRecordSet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="68203-152">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="68203-153">변수</span><span class="sxs-lookup"><span data-stu-id="68203-153">PARAMETERS</span></span>

### <span data-ttu-id="68203-154">-Cname</span><span class="sxs-lookup"><span data-stu-id="68203-154">-Cname</span></span>
<span data-ttu-id="68203-155">CNAME (정식 이름) 레코드에 대 한 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-155">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68203-156">-Exchange</span><span class="sxs-lookup"><span data-stu-id="68203-156">-Exchange</span></span>
<span data-ttu-id="68203-157">메일 교환 (MX) 레코드의 메일 교환 서버 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-157">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68203-158">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="68203-158">-Ipv4Address</span></span>
<span data-ttu-id="68203-159">A 레코드에 대 한 IPv4 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-159">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68203-160">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="68203-160">-Ipv6Address</span></span>
<span data-ttu-id="68203-161">AAAA 레코드에 대 한 IPv6 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-161">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68203-162">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="68203-162">-Nsdname</span></span>
<span data-ttu-id="68203-163">NS (이름 서버) 레코드에 대 한 이름 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-163">Specifies the name server for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68203-164">-포트</span><span class="sxs-lookup"><span data-stu-id="68203-164">-Port</span></span>
<span data-ttu-id="68203-165">서비스 (SRV) 레코드의 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-165">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68203-166">-기본 설정</span><span class="sxs-lookup"><span data-stu-id="68203-166">-Preference</span></span>
<span data-ttu-id="68203-167">MX 레코드에 대 한 기본 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-167">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68203-168">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="68203-168">-Priority</span></span>
<span data-ttu-id="68203-169">SRV 레코드에 대 한 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-169">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68203-170">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="68203-170">-Ptrdname</span></span>
<span data-ttu-id="68203-171">포인터 (PTR) 레코드의 대상 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-171">Specifies the target domain name of a pointer (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68203-172">-레코드 집합</span><span class="sxs-lookup"><span data-stu-id="68203-172">-RecordSet</span></span>
<span data-ttu-id="68203-173">제거할 레코드가 포함 된 **레코드 집합** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-173">Specifies the **RecordSet** object that contains the record to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68203-174">-대상</span><span class="sxs-lookup"><span data-stu-id="68203-174">-Target</span></span>
<span data-ttu-id="68203-175">SRV 레코드의 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-175">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68203-176">-값</span><span class="sxs-lookup"><span data-stu-id="68203-176">-Value</span></span>
<span data-ttu-id="68203-177">TXT 레코드에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-177">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68203-178">-중량</span><span class="sxs-lookup"><span data-stu-id="68203-178">-Weight</span></span>
<span data-ttu-id="68203-179">SRV 레코드의 가중치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-179">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68203-180">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68203-180">-DefaultProfile</span></span>
<span data-ttu-id="68203-181">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68203-181">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68203-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68203-182">CommonParameters</span></span>
<span data-ttu-id="68203-183">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68203-184">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68203-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68203-185">입력</span><span class="sxs-lookup"><span data-stu-id="68203-185">INPUTS</span></span>

### <span data-ttu-id="68203-186">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="68203-186">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="68203-187">이 cmdlet에 **Dnsrecordset** 개체를 파이프 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68203-187">You can pipe a **DnsRecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="68203-188">이는 레코드 집합의 오프 라인 표현이 며, Set-AzureRmDnsRecordSet을 실행 한 후에만 DNS 응답을 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68203-188">This is an offline representation of the record set and updates to it do not change DNS responses until after you run Set-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="68203-189">출력</span><span class="sxs-lookup"><span data-stu-id="68203-189">OUTPUTS</span></span>

### <span data-ttu-id="68203-190">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="68203-190">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="68203-191">이 cmdlet은 수정 된 **레코드 집합** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="68203-191">This cmdlet returns the modified **RecordSet** object.</span></span>

## <span data-ttu-id="68203-192">상속자</span><span class="sxs-lookup"><span data-stu-id="68203-192">NOTES</span></span>

## <span data-ttu-id="68203-193">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68203-193">RELATED LINKS</span></span>

[<span data-ttu-id="68203-194">추가-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="68203-194">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="68203-195">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="68203-195">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="68203-196">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="68203-196">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
