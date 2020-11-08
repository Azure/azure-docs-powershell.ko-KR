---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: 98d2bea18489a9ee84cd7c513989c0d9a4b5caf3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034422"
---
# <span data-ttu-id="af2ef-101">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="af2ef-101">New-AzDnsRecordSet</span></span>

## <span data-ttu-id="af2ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af2ef-102">SYNOPSIS</span></span>
<span data-ttu-id="af2ef-103">DNS 레코드 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-103">Creates a DNS record set.</span></span>

## <span data-ttu-id="af2ef-104">구문과</span><span class="sxs-lookup"><span data-stu-id="af2ef-104">SYNTAX</span></span>

### <span data-ttu-id="af2ef-105">필드 (기본값)</span><span class="sxs-lookup"><span data-stu-id="af2ef-105">Fields (Default)</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af2ef-106">AliasFields</span><span class="sxs-lookup"><span data-stu-id="af2ef-106">AliasFields</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af2ef-107">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="af2ef-107">Object</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af2ef-108">AliasObject</span><span class="sxs-lookup"><span data-stu-id="af2ef-108">AliasObject</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af2ef-109">설명은</span><span class="sxs-lookup"><span data-stu-id="af2ef-109">DESCRIPTION</span></span>
<span data-ttu-id="af2ef-110">**AzDnsRecordSet** cmdlet은 지정 된 이름 및 유형을 가진 새 DNS (Domain Name System) 레코드 집합을 지정한 영역에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-110">The **New-AzDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="af2ef-111">**레코드 집합** 개체는 이름 및 형식이 같은 DNS 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-111">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="af2ef-112">이름은 영역에 대해 상대적 이며 정규화 된 이름이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-112">Note that the name is relative to the zone and not the fully qualified name.</span></span>
<span data-ttu-id="af2ef-113">*Dnsrecords* 매개 변수는 레코드 집합의 레코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-113">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="af2ef-114">이 매개 변수는 New-AzDnsRecordConfig를 사용 하 여 생성 된 DNS 레코드 배열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-114">This parameter takes an array of DNS records, constructed using New-AzDnsRecordConfig.</span></span>
<span data-ttu-id="af2ef-115">파이프라인 연산자를 사용 하 여 **DnsZone** 개체를이 cmdlet에 전달 하거나, **DnsZone** 개체를 *zone* 매개 변수로 전달 하거나, 이름을 기준으로 영역을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-115">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>
<span data-ttu-id="af2ef-116">*확인* 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-116">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="af2ef-117">일치 하는 **레코드 집합** (이름 및 레코드 형식)이 이미 있는 경우 *Overwrite* 매개 변수를 지정 해야 하며 그렇지 않으면 Cmdlet에서 새 **레코드 집합** 을 만들지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-117">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="af2ef-118">예제의</span><span class="sxs-lookup"><span data-stu-id="af2ef-118">EXAMPLES</span></span>

### <span data-ttu-id="af2ef-119">예제 1: 형식 A의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="af2ef-119">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="af2ef-120">이 예제에서는 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-120">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="af2ef-121">레코드 집합은 A 형식이 고 TTL은 1 시간 (3600 초)입니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-121">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="af2ef-122">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-122">It contains a single DNS record.</span></span>

### <span data-ttu-id="af2ef-123">예제 2: AAAA 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="af2ef-123">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="af2ef-124">이 예제에서는 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-124">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="af2ef-125">레코드 집합은 AAAA 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-125">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="af2ef-126">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-126">It contains a single DNS record.</span></span>
<span data-ttu-id="af2ef-127">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="af2ef-127">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="af2ef-128">예제 3: CNAME 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="af2ef-128">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="af2ef-129">이 예제에서는 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-129">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="af2ef-130">레코드 집합은 CNAME 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-130">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="af2ef-131">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-131">It contains a single DNS record.</span></span>
<span data-ttu-id="af2ef-132">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="af2ef-132">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="af2ef-133">예제 4: MX 유형의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="af2ef-133">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="af2ef-134">이 명령은 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-134">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="af2ef-135">레코드 집합은 MX 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-135">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="af2ef-136">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-136">It contains a single DNS record.</span></span>
<span data-ttu-id="af2ef-137">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="af2ef-137">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="af2ef-138">예제 5: NS 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="af2ef-138">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="af2ef-139">이 명령은 zone myzone.com에 ns1 이라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-139">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="af2ef-140">레코드 집합은 NS 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-140">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="af2ef-141">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-141">It contains a single DNS record.</span></span>
<span data-ttu-id="af2ef-142">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="af2ef-142">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="af2ef-143">예제 6: 형식 PTR의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="af2ef-143">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="af2ef-144">이 명령은 zone 3.2.1.in-in-addr.arpa에 4 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-144">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="af2ef-145">레코드 집합은 PTR 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-145">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="af2ef-146">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-146">It contains a single DNS record.</span></span>
<span data-ttu-id="af2ef-147">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="af2ef-147">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="af2ef-148">예제 7: SRV 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="af2ef-148">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="af2ef-149">이 명령은 zone myzone.com에서 _sip 이라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-149">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="af2ef-150">레코드 집합은 SRV 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-150">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="af2ef-151">IP 주소 2001.2.3.4를 가리키는 단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-151">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="af2ef-152">서비스 (sip) 및 프로토콜 (tcp)은 레코드 데이터의 일부가 아닌 레코드 집합 이름의 일부로 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-152">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="af2ef-153">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="af2ef-153">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="af2ef-154">예제 8: TXT 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="af2ef-154">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="af2ef-155">이 명령은 zone myzone.com에 text 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-155">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="af2ef-156">레코드 집합은 TXT 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-156">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="af2ef-157">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-157">It contains a single DNS record.</span></span>
<span data-ttu-id="af2ef-158">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="af2ef-158">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="af2ef-159">예제 9: zone apex에서 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="af2ef-159">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="af2ef-160">이 명령은 myzone.com 영역의 apex (또는 루트)에서 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-160">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="af2ef-161">이렇게 하려면 레코드 집합 이름이 "@"로 지정 됩니다 (큰따옴표 포함).</span><span class="sxs-lookup"><span data-stu-id="af2ef-161">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>
<span data-ttu-id="af2ef-162">영역 apex에서 CNAME 레코드를 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-162">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="af2ef-163">이것은 DNS 표준의 제약 조건입니다. Azure DNS의 제한이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-163">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>
<span data-ttu-id="af2ef-164">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="af2ef-164">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="af2ef-165">예제 10: 와일드 카드 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="af2ef-165">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="af2ef-166">이 명령은 zone myzone.com에 \* 이라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-166">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="af2ef-167">와일드 카드 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-167">This is a wildcard record set.</span></span>
<span data-ttu-id="af2ef-168">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="af2ef-168">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="af2ef-169">예제 11: 빈 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="af2ef-169">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="af2ef-170">이 명령은 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-170">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="af2ef-171">레코드 집합은 A 형식이 고 TTL은 1 시간 (3600 초)입니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-171">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="af2ef-172">나중에 레코드를 추가할 수 있는 자리 표시자 역할을 하는 빈 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-172">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="af2ef-173">예제 12: 레코드 집합 만들기 및 모든 확인 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="af2ef-173">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="af2ef-174">이 명령은 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-174">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="af2ef-175">*Overwrite* 매개 변수를 사용 하면이 레코드 집합에서 이름 및 형식이 같은 기존 레코드 집합을 덮어쓰게 되며 해당 레코드 집합의 기존 레코드는 손실 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-175">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="af2ef-176">값이 $False 인 *Confirm* 매개 변수는 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-176">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="af2ef-177">변수</span><span class="sxs-lookup"><span data-stu-id="af2ef-177">PARAMETERS</span></span>

### <span data-ttu-id="af2ef-178">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af2ef-178">-DefaultProfile</span></span>
<span data-ttu-id="af2ef-179">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="af2ef-179">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af2ef-180">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="af2ef-180">-DnsRecords</span></span>
<span data-ttu-id="af2ef-181">레코드 집합에 포함할 DNS 레코드의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-181">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="af2ef-182">New-AzDnsRecordConfig cmdlet을 사용 하 여 DNS 레코드 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-182">You can use the New-AzDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="af2ef-183">자세한 내용은 예제를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="af2ef-183">See the examples for more information.</span></span>

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

### <span data-ttu-id="af2ef-184">-Metadata</span><span class="sxs-lookup"><span data-stu-id="af2ef-184">-Metadata</span></span>
<span data-ttu-id="af2ef-185">레코드 집합과 연결할 메타 데이터의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="af2ef-186">메타 데이터는 해시 테이블로 표시 되는 이름-값 쌍 (@ {"Name" = "dept")을 사용 하 여 지정 됩니다. "Value" = "장바구니"}, @ {"Name" = "env"; "Value" = "production"}).</span><span class="sxs-lookup"><span data-stu-id="af2ef-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @(@{"Name"="dept"; "Value"="shopping"}, @{"Name"="env"; "Value"="production"}).</span></span>

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

### <span data-ttu-id="af2ef-187">-이름</span><span class="sxs-lookup"><span data-stu-id="af2ef-187">-Name</span></span>
<span data-ttu-id="af2ef-188">만들 **레코드 집합** 의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="af2ef-189">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="af2ef-189">-Overwrite</span></span>
<span data-ttu-id="af2ef-190">이 cmdlet이 이미 존재 하는 경우 지정 된 **레코드 집합** 을 덮어쓰게 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="af2ef-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="af2ef-191">-RecordType</span></span>
<span data-ttu-id="af2ef-192">만들려는 DNS 레코드의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-192">Specifies the type of DNS record to create.</span></span>
<span data-ttu-id="af2ef-193">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-193">Valid values are:</span></span>
- <span data-ttu-id="af2ef-194">에서</span><span class="sxs-lookup"><span data-stu-id="af2ef-194">A</span></span>
- <span data-ttu-id="af2ef-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="af2ef-195">AAAA</span></span>
- <span data-ttu-id="af2ef-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="af2ef-196">CNAME</span></span>
- <span data-ttu-id="af2ef-197">멕시코</span><span class="sxs-lookup"><span data-stu-id="af2ef-197">MX</span></span>
- <span data-ttu-id="af2ef-198">NS</span><span class="sxs-lookup"><span data-stu-id="af2ef-198">NS</span></span>
- <span data-ttu-id="af2ef-199">PTR 레코드로</span><span class="sxs-lookup"><span data-stu-id="af2ef-199">PTR</span></span>
- <span data-ttu-id="af2ef-200">SRV</span><span class="sxs-lookup"><span data-stu-id="af2ef-200">SRV</span></span>
- <span data-ttu-id="af2ef-201">TXT SOA 레코드는 영역이 생성 될 때 자동으로 만들어지므로 수동으로 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

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

### <span data-ttu-id="af2ef-202">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af2ef-202">-ResourceGroupName</span></span>
<span data-ttu-id="af2ef-203">DNS 영역이 포함 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-203">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="af2ef-204">또한 *ZoneName* 매개 변수를 지정 하 여 영역 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-204">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>
<span data-ttu-id="af2ef-205">또는 *zone* 매개 변수를 사용 하 여 DNS 영역 개체를 전달 하 여 영역 및 리소스 그룹을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-205">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="af2ef-206">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="af2ef-206">-TargetResourceId</span></span>
<span data-ttu-id="af2ef-207">별칭 대상 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-207">Alias Target Resource Id.</span></span>

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

### <span data-ttu-id="af2ef-208">-Ttl</span><span class="sxs-lookup"><span data-stu-id="af2ef-208">-Ttl</span></span>
<span data-ttu-id="af2ef-209">DNS 레코드 집합에 대 한 TTL (Time to Live)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-209">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

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

### <span data-ttu-id="af2ef-210">-Zone</span><span class="sxs-lookup"><span data-stu-id="af2ef-210">-Zone</span></span>
<span data-ttu-id="af2ef-211">**레코드 집합** 을 만들 DnsZone를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-211">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="af2ef-212">또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용 하 여 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-212">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="af2ef-213">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="af2ef-213">-ZoneName</span></span>
<span data-ttu-id="af2ef-214">**레코드 집합** 을 만들 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-214">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="af2ef-215">또한 *ResourceGroupName* 매개 변수를 사용 하 여 영역을 포함 하는 리소스 그룹을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-215">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="af2ef-216">또는 *zone* 매개 변수를 사용 하 여 DNS 영역 개체를 전달 하 여 영역 및 리소스 그룹을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-216">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="af2ef-217">-확인</span><span class="sxs-lookup"><span data-stu-id="af2ef-217">-Confirm</span></span>
<span data-ttu-id="af2ef-218">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-218">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af2ef-219">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af2ef-219">-WhatIf</span></span>
<span data-ttu-id="af2ef-220">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-220">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af2ef-221">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-221">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af2ef-222">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af2ef-222">CommonParameters</span></span>
<span data-ttu-id="af2ef-223">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-223">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af2ef-224">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af2ef-224">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af2ef-225">입력</span><span class="sxs-lookup"><span data-stu-id="af2ef-225">INPUTS</span></span>

### <span data-ttu-id="af2ef-226">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="af2ef-226">System.String</span></span>

### <span data-ttu-id="af2ef-227">DnsZone에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="af2ef-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="af2ef-228">시스템. UInt32</span><span class="sxs-lookup"><span data-stu-id="af2ef-228">System.UInt32</span></span>

### <span data-ttu-id="af2ef-229">RecordType를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-229">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="af2ef-230">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="af2ef-230">System.Collections.Hashtable</span></span>

### <span data-ttu-id="af2ef-231">Microsoft. Dns. DnsRecordBase []</span><span class="sxs-lookup"><span data-stu-id="af2ef-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span></span>

## <span data-ttu-id="af2ef-232">출력</span><span class="sxs-lookup"><span data-stu-id="af2ef-232">OUTPUTS</span></span>

### <span data-ttu-id="af2ef-233">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="af2ef-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="af2ef-234">상속자</span><span class="sxs-lookup"><span data-stu-id="af2ef-234">NOTES</span></span>
<span data-ttu-id="af2ef-235">*확인* 매개 변수를 사용 하 여이 cmdlet이 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-235">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="af2ef-236">기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 변수의 값이 중간 인지 아래 인지 여부를 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-236">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="af2ef-237">*확인* 또는 *확인: $True* 를 지정 하는 경우이 cmdlet을 실행 하기 전에 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-237">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="af2ef-238">*확인: $False* 를 지정 하면 cmdlet에서 확인을 요구 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af2ef-238">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="af2ef-239">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af2ef-239">RELATED LINKS</span></span>

[<span data-ttu-id="af2ef-240">추가-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="af2ef-240">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="af2ef-241">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="af2ef-241">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="af2ef-242">새로운 AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="af2ef-242">New-AzDnsRecordConfig</span></span>](./New-AzDnsRecordConfig.md)

[<span data-ttu-id="af2ef-243">제거-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="af2ef-243">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="af2ef-244">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="af2ef-244">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
