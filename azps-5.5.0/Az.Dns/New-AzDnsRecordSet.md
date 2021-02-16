---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: bb2e9a9729ed911902e493422109cae764ad6d5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209616"
---
# <span data-ttu-id="c3083-101">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c3083-101">New-AzDnsRecordSet</span></span>

## <span data-ttu-id="c3083-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3083-102">SYNOPSIS</span></span>
<span data-ttu-id="c3083-103">DNS 레코드 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-103">Creates a DNS record set.</span></span>

## <span data-ttu-id="c3083-104">구문</span><span class="sxs-lookup"><span data-stu-id="c3083-104">SYNTAX</span></span>

### <span data-ttu-id="c3083-105">필드(기본값)</span><span class="sxs-lookup"><span data-stu-id="c3083-105">Fields (Default)</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3083-106">AliasFields</span><span class="sxs-lookup"><span data-stu-id="c3083-106">AliasFields</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3083-107">개체</span><span class="sxs-lookup"><span data-stu-id="c3083-107">Object</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3083-108">AliasObject</span><span class="sxs-lookup"><span data-stu-id="c3083-108">AliasObject</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3083-109">설명</span><span class="sxs-lookup"><span data-stu-id="c3083-109">DESCRIPTION</span></span>
<span data-ttu-id="c3083-110">**New-AzDnsRecordSet** cmdlet은 지정된 이름 및 지정된 영역의 형식을 사용하여 새 DNS(도메인 이름 시스템) 레코드 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-110">The **New-AzDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="c3083-111">**RecordSet** 개체는 이름과 형식이 같은 DNS 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-111">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="c3083-112">이름은 영역과 상대적인 것이고, 정식 이름이 아닌 것을 참고합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-112">Note that the name is relative to the zone and not the fully qualified name.</span></span>
<span data-ttu-id="c3083-113">*DnsRecords 매개* 변수는 레코드 집합의 레코드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-113">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="c3083-114">이 매개 변수는 New-AzDnsRecordConfig를 사용하여 생성된 DNS 레코드의 배열을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-114">This parameter takes an array of DNS records, constructed using New-AzDnsRecordConfig.</span></span>
<span data-ttu-id="c3083-115">파이프라인 연산자를 사용하여 **DnsZone** 개체를 이 cmdlet에 전달하거나 **DnsZone** 개체를 영역  매개 변수로 전달하거나 이름으로 영역 지정을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-115">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>
<span data-ttu-id="c3083-116">*Confirm* 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-116">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="c3083-117">일치하는 **RecordSet이** 이미 있는 경우(동일한 이름 및 레코드 형식) *덮어써서* 매개 변수를 지정해야 합니다. 그렇지 않으면 cmdlet에서 새 **RecordSet을 만들지 않습니다.**</span><span class="sxs-lookup"><span data-stu-id="c3083-117">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="c3083-118">예제</span><span class="sxs-lookup"><span data-stu-id="c3083-118">EXAMPLES</span></span>

### <span data-ttu-id="c3083-119">예제 1: A 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="c3083-119">Example 1: Create a RecordSet of type A</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzDnsRecordConfig to add each record to the $Records array,
# then call New-AzDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c3083-120">이 예제에서는 영역 집합에 www라는 **RecordSet을** myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c3083-120">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="c3083-121">레코드 집합은 형식 A로, TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-121">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c3083-122">단일 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-122">It contains a single DNS record.</span></span>

### <span data-ttu-id="c3083-123">예제 2: AAAA 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="c3083-123">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c3083-124">이 예제에서는 영역 집합에 www라는 **RecordSet을** myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c3083-124">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="c3083-125">레코드 집합은 AAAA 형식의 TTL(1시간)(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-125">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c3083-126">단일 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-126">It contains a single DNS record.</span></span>
<span data-ttu-id="c3083-127">한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드가 여러 개 있는 레코드 집합을 만들 경우 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-127">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c3083-128">예제 3: CNAME 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="c3083-128">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c3083-129">이 예제에서는 영역 이름에 www라는 **RecordSet을** myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c3083-129">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="c3083-130">레코드 집합은 CNAME 형식이고 TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-130">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c3083-131">단일 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-131">It contains a single DNS record.</span></span>
<span data-ttu-id="c3083-132">한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드가 여러 개 있는 레코드 집합을 만들 경우 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-132">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c3083-133">예제 4: MX 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="c3083-133">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c3083-134">이 명령은 영역 집합에 www라는 **RecordSet을** myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c3083-134">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="c3083-135">레코드 집합은 MX 형식이고 TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-135">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c3083-136">단일 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-136">It contains a single DNS record.</span></span>
<span data-ttu-id="c3083-137">한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드 집합을 만들거나 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-137">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c3083-138">예제 5: NS 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="c3083-138">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c3083-139">이 명령은 영역 집합에 ns1이라는 **RecordSet을** myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c3083-139">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="c3083-140">레코드 집합은 NS 형식으로, TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-140">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c3083-141">단일 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-141">It contains a single DNS record.</span></span>
<span data-ttu-id="c3083-142">한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드가 여러 개 있는 레코드 집합을 만들 경우 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-142">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c3083-143">예제 6: PTR 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="c3083-143">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="c3083-144">이 명령은 **4라는 RecordSet을** 3.2.1.in-addr.arpa입니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-144">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="c3083-145">레코드 집합은 PTR 형식으로, TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-145">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c3083-146">단일 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-146">It contains a single DNS record.</span></span>
<span data-ttu-id="c3083-147">한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드가 여러 개 있는 레코드 집합을 만들 경우 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-147">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c3083-148">예제 7: SRV 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="c3083-148">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c3083-149">이 명령은 _sip._tcp라는 **RecordSet을** myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c3083-149">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="c3083-150">레코드 집합은 SRV 형식으로, TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-150">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c3083-151">IP 주소 2001.2.3.4를 포인터로 하는 단일 DNS 레코드가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-151">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="c3083-152">서비스(sip) 및 프로토콜(tcp)은 레코드 데이터의 일부가 아닌 레코드 집합 이름의 일부로 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-152">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="c3083-153">한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드가 여러 개 있는 레코드 집합을 만들 경우 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-153">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c3083-154">예제 8: TXT 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="c3083-154">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c3083-155">이 명령은 영역 이름의 **RecordSet** 텍스트를 myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c3083-155">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="c3083-156">레코드 집합은 TXT 형식으로, TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-156">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c3083-157">단일 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-157">It contains a single DNS record.</span></span>
<span data-ttu-id="c3083-158">한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드가 여러 개 있는 레코드 집합을 만들 경우 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-158">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c3083-159">예제 9: 영역 apex에서 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="c3083-159">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c3083-160">이 명령은 영역의 루트 또는 루트에 **RecordSet을** myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c3083-160">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="c3083-161">이를 위해 레코드 집합 이름은 "@"(따옴표 포함)로 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-161">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>
<span data-ttu-id="c3083-162">영역의 apex에는 CNAME 레코드를 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-162">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="c3083-163">DNS 표준의 제약 조건입니다. Azure DNS의 제한 사항이 아닌 경우</span><span class="sxs-lookup"><span data-stu-id="c3083-163">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>
<span data-ttu-id="c3083-164">한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드가 여러 개 있는 레코드 집합을 만들 경우 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-164">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c3083-165">예제 10: 와일드카드 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="c3083-165">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c3083-166">이 명령은 영역 집합에 \*라는 **RecordSet을** myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c3083-166">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="c3083-167">와일드카드 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-167">This is a wildcard record set.</span></span>
<span data-ttu-id="c3083-168">한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드가 여러 개 있는 레코드 집합을 만들 경우 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-168">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c3083-169">예제 11: 빈 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="c3083-169">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="c3083-170">이 명령은 영역 집합에 www라는 **RecordSet을** myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c3083-170">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="c3083-171">레코드 집합은 형식 A로, TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-171">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c3083-172">빈 레코드 집합으로, 나중에 레코드를 추가할 수 있는 자리 홀더 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-172">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="c3083-173">예제 12: 레코드 집합 만들기 및 모든 확인 표시 안</span><span class="sxs-lookup"><span data-stu-id="c3083-173">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="c3083-174">이 명령은 **RecordSet을 만듭니다.**</span><span class="sxs-lookup"><span data-stu-id="c3083-174">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="c3083-175">*덮어덮어* 사용 매개 변수를 사용하면 이 레코드 집합이 이름과 형식이 같은 기존 레코드 집합을 덮어 덮어습니다(해당 레코드 집합의 기존 레코드가 손실).</span><span class="sxs-lookup"><span data-stu-id="c3083-175">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="c3083-176">값과 함께 *Confirm* $False 확인 프롬프트를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-176">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="c3083-177">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3083-177">PARAMETERS</span></span>

### <span data-ttu-id="c3083-178">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3083-178">-DefaultProfile</span></span>
<span data-ttu-id="c3083-179">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c3083-179">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3083-180">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="c3083-180">-DnsRecords</span></span>
<span data-ttu-id="c3083-181">레코드 집합에 포함할 DNS 레코드의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-181">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="c3083-182">New-AzDnsRecordConfig cmdlet을 사용하여 DNS 레코드 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-182">You can use the New-AzDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="c3083-183">자세한 내용은 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c3083-183">See the examples for more information.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordBase[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3083-184">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c3083-184">-Metadata</span></span>
<span data-ttu-id="c3083-185">RecordSet과 연결되는 메타데이터 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="c3083-186">메타데이터는 해시 테이블로 표현되는 이름-값 쌍(예: @{"dept"="shopping";")을 사용하여 지정됩니다. env"="production"}.</span><span class="sxs-lookup"><span data-stu-id="c3083-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @{"dept"="shopping";"env"="production"}.</span></span>

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

### <span data-ttu-id="c3083-187">-Name</span><span class="sxs-lookup"><span data-stu-id="c3083-187">-Name</span></span>
<span data-ttu-id="c3083-188">만들 **RecordSet의 이름을** 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="c3083-189">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="c3083-189">-Overwrite</span></span>
<span data-ttu-id="c3083-190">이 cmdlet이 이미 있는 경우 지정된 **RecordSet을** 덮어써야 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="c3083-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="c3083-191">-RecordType</span></span>
<span data-ttu-id="c3083-192">만들 DNS 레코드의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-192">Specifies the type of DNS record to create.</span></span>
<span data-ttu-id="c3083-193">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="c3083-193">Valid values are:</span></span>
- <span data-ttu-id="c3083-194">A</span><span class="sxs-lookup"><span data-stu-id="c3083-194">A</span></span>
- <span data-ttu-id="c3083-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="c3083-195">AAAA</span></span>
- <span data-ttu-id="c3083-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="c3083-196">CNAME</span></span>
- <span data-ttu-id="c3083-197">MX</span><span class="sxs-lookup"><span data-stu-id="c3083-197">MX</span></span>
- <span data-ttu-id="c3083-198">NS</span><span class="sxs-lookup"><span data-stu-id="c3083-198">NS</span></span>
- <span data-ttu-id="c3083-199">PTR</span><span class="sxs-lookup"><span data-stu-id="c3083-199">PTR</span></span>
- <span data-ttu-id="c3083-200">SRV</span><span class="sxs-lookup"><span data-stu-id="c3083-200">SRV</span></span>
- <span data-ttu-id="c3083-201">영역이 만들어지면 TXT SOA 레코드가 자동으로 만들어지며 수동으로 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3083-202">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3083-202">-ResourceGroupName</span></span>
<span data-ttu-id="c3083-203">DNS 영역이 포함된 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-203">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="c3083-204">영역 이름을 지정하려면 *ZoneName* 매개 변수도 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-204">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>
<span data-ttu-id="c3083-205">또는 영역 매개 변수를 사용하여 DNS 영역 개체를 전달하여 영역 및 리소스 그룹을 지정할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-205">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3083-206">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c3083-206">-TargetResourceId</span></span>
<span data-ttu-id="c3083-207">별칭 대상 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-207">Alias Target Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3083-208">-Ttl</span><span class="sxs-lookup"><span data-stu-id="c3083-208">-Ttl</span></span>
<span data-ttu-id="c3083-209">DNS RecordSet에 대한 TTL(Time to Live)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-209">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: Fields, Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3083-210">-Zone</span><span class="sxs-lookup"><span data-stu-id="c3083-210">-Zone</span></span>
<span data-ttu-id="c3083-211">RecordSet을 만들 DnsZone을 **지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="c3083-211">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="c3083-212">또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용하여 지역을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-212">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3083-213">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="c3083-213">-ZoneName</span></span>
<span data-ttu-id="c3083-214">RecordSet을 만들 영역의 이름을 **지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="c3083-214">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="c3083-215">*ResourceGroupName* 매개 변수를 사용하여 영역이 포함된 리소스 그룹도 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-215">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="c3083-216">또는 영역 매개 변수를 사용하여 DNS 영역 개체를 전달하여 영역 및 리소스 그룹을 지정할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-216">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3083-217">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3083-217">-Confirm</span></span>
<span data-ttu-id="c3083-218">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-218">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3083-219">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3083-219">-WhatIf</span></span>
<span data-ttu-id="c3083-220">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c3083-220">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3083-221">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-221">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3083-222">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3083-222">CommonParameters</span></span>
<span data-ttu-id="c3083-223">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-223">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3083-224">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c3083-224">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3083-225">입력</span><span class="sxs-lookup"><span data-stu-id="c3083-225">INPUTS</span></span>

### <span data-ttu-id="c3083-226">System.String</span><span class="sxs-lookup"><span data-stu-id="c3083-226">System.String</span></span>

### <span data-ttu-id="c3083-227">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="c3083-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="c3083-228">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="c3083-228">System.UInt32</span></span>

### <span data-ttu-id="c3083-229">Microsoft.Azure.Management.Dns.Models.RecordType</span><span class="sxs-lookup"><span data-stu-id="c3083-229">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="c3083-230">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c3083-230">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c3083-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span><span class="sxs-lookup"><span data-stu-id="c3083-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span></span>

## <span data-ttu-id="c3083-232">출력</span><span class="sxs-lookup"><span data-stu-id="c3083-232">OUTPUTS</span></span>

### <span data-ttu-id="c3083-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c3083-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="c3083-234">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c3083-234">NOTES</span></span>
<span data-ttu-id="c3083-235">*Confirm* 매개 변수를 사용하여 이 cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-235">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="c3083-236">기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 값이 Medium 또는 lower인 경우 확인을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-236">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="c3083-237">*Confirm* 또는 *Confirm:$True* 지정하는 경우 이 cmdlet은 실행 전에 확인을 요청하는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-237">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="c3083-238">*Confirm:$False* 지정하면 cmdlet에서 확인 메시지를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3083-238">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c3083-239">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3083-239">RELATED LINKS</span></span>

[<span data-ttu-id="c3083-240">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="c3083-240">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="c3083-241">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c3083-241">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="c3083-242">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="c3083-242">New-AzDnsRecordConfig</span></span>](./New-AzDnsRecordConfig.md)

[<span data-ttu-id="c3083-243">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c3083-243">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="c3083-244">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c3083-244">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
