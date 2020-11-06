---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordSet.md
ms.openlocfilehash: 7f271ee6a946356fe9cbf09379e2e620a240b733
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530989"
---
# <span data-ttu-id="35ca4-101">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="35ca4-101">New-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="35ca4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35ca4-102">SYNOPSIS</span></span>
<span data-ttu-id="35ca4-103">DNS 레코드 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-103">Creates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35ca4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="35ca4-104">SYNTAX</span></span>

### <span data-ttu-id="35ca4-105">필드 (기본값)</span><span class="sxs-lookup"><span data-stu-id="35ca4-105">Fields (Default)</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35ca4-106">AliasFields</span><span class="sxs-lookup"><span data-stu-id="35ca4-106">AliasFields</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35ca4-107">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="35ca4-107">Object</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35ca4-108">AliasObject</span><span class="sxs-lookup"><span data-stu-id="35ca4-108">AliasObject</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35ca4-109">설명은</span><span class="sxs-lookup"><span data-stu-id="35ca4-109">DESCRIPTION</span></span>
<span data-ttu-id="35ca4-110">**AzureRmDnsRecordSet** cmdlet은 지정 된 이름 및 유형을 가진 새 DNS (Domain Name System) 레코드 집합을 지정한 영역에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-110">The **New-AzureRmDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="35ca4-111">**레코드 집합** 개체는 이름 및 형식이 같은 DNS 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-111">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="35ca4-112">이름은 영역에 대해 상대적 이며 정규화 된 이름이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-112">Note that the name is relative to the zone and not the fully qualified name.</span></span>
<span data-ttu-id="35ca4-113">*Dnsrecords* 매개 변수는 레코드 집합의 레코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-113">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="35ca4-114">이 매개 변수는 New-AzureRmDnsRecordConfig를 사용 하 여 생성 된 DNS 레코드 배열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-114">This parameter takes an array of DNS records, constructed using New-AzureRmDnsRecordConfig.</span></span>
<span data-ttu-id="35ca4-115">파이프라인 연산자를 사용 하 여 **DnsZone** 개체를이 cmdlet에 전달 하거나, **DnsZone** 개체를 *zone* 매개 변수로 전달 하거나, 이름을 기준으로 영역을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-115">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>
<span data-ttu-id="35ca4-116">*확인* 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-116">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="35ca4-117">일치 하는 **레코드 집합** (이름 및 레코드 형식)이 이미 있는 경우 *Overwrite* 매개 변수를 지정 해야 하며 그렇지 않으면 Cmdlet에서 새 **레코드 집합** 을 만들지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-117">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="35ca4-118">예제의</span><span class="sxs-lookup"><span data-stu-id="35ca4-118">EXAMPLES</span></span>

### <span data-ttu-id="35ca4-119">예제 1: 형식 A의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="35ca4-119">Example 1: Create a RecordSet of type A</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzureRmDnsRecordConfig to add each record to the $Records array,
# then call New-AzureRmDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="35ca4-120">이 예제에서는 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-120">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="35ca4-121">레코드 집합은 A 형식이 고 TTL은 1 시간 (3600 초)입니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-121">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="35ca4-122">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-122">It contains a single DNS record.</span></span>

### <span data-ttu-id="35ca4-123">예제 2: AAAA 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="35ca4-123">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="35ca4-124">이 예제에서는 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-124">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="35ca4-125">레코드 집합은 AAAA 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-125">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="35ca4-126">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-126">It contains a single DNS record.</span></span>
<span data-ttu-id="35ca4-127">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35ca4-127">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="35ca4-128">예제 3: CNAME 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="35ca4-128">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="35ca4-129">이 예제에서는 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-129">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="35ca4-130">레코드 집합은 CNAME 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-130">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="35ca4-131">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-131">It contains a single DNS record.</span></span>
<span data-ttu-id="35ca4-132">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35ca4-132">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="35ca4-133">예제 4: MX 유형의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="35ca4-133">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="35ca4-134">이 명령은 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-134">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="35ca4-135">레코드 집합은 MX 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-135">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="35ca4-136">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-136">It contains a single DNS record.</span></span>
<span data-ttu-id="35ca4-137">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35ca4-137">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="35ca4-138">예제 5: NS 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="35ca4-138">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="35ca4-139">이 명령은 zone myzone.com에 ns1 이라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-139">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="35ca4-140">레코드 집합은 NS 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-140">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="35ca4-141">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-141">It contains a single DNS record.</span></span>
<span data-ttu-id="35ca4-142">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35ca4-142">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="35ca4-143">예제 6: 형식 PTR의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="35ca4-143">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="35ca4-144">이 명령은 zone 3.2.1.in-in-addr.arpa에 4 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-144">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="35ca4-145">레코드 집합은 PTR 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-145">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="35ca4-146">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-146">It contains a single DNS record.</span></span>
<span data-ttu-id="35ca4-147">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35ca4-147">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="35ca4-148">예제 7: SRV 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="35ca4-148">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="35ca4-149">이 명령은 zone myzone.com에서 _sip 이라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-149">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="35ca4-150">레코드 집합은 SRV 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-150">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="35ca4-151">IP 주소 2001.2.3.4를 가리키는 단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-151">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="35ca4-152">서비스 (sip) 및 프로토콜 (tcp)은 레코드 데이터의 일부가 아닌 레코드 집합 이름의 일부로 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-152">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="35ca4-153">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35ca4-153">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="35ca4-154">예제 8: TXT 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="35ca4-154">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="35ca4-155">이 명령은 zone myzone.com에 text 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-155">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="35ca4-156">레코드 집합은 TXT 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-156">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="35ca4-157">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-157">It contains a single DNS record.</span></span>
<span data-ttu-id="35ca4-158">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35ca4-158">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="35ca4-159">예제 9: zone apex에서 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="35ca4-159">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="35ca4-160">이 명령은 myzone.com 영역의 apex (또는 루트)에서 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-160">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="35ca4-161">이렇게 하려면 레코드 집합 이름이 "@"로 지정 됩니다 (큰따옴표 포함).</span><span class="sxs-lookup"><span data-stu-id="35ca4-161">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>
<span data-ttu-id="35ca4-162">영역 apex에서 CNAME 레코드를 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-162">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="35ca4-163">이것은 DNS 표준의 제약 조건입니다. Azure DNS의 제한이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-163">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>
<span data-ttu-id="35ca4-164">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35ca4-164">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="35ca4-165">예제 10: 와일드 카드 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="35ca4-165">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="35ca4-166">이 명령은 zone myzone.com에 \* 이라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-166">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="35ca4-167">와일드 카드 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-167">This is a wildcard record set.</span></span>
<span data-ttu-id="35ca4-168">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35ca4-168">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="35ca4-169">예제 11: 빈 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="35ca4-169">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="35ca4-170">이 명령은 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-170">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="35ca4-171">레코드 집합은 A 형식이 고 TTL은 1 시간 (3600 초)입니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-171">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="35ca4-172">나중에 레코드를 추가할 수 있는 자리 표시자 역할을 하는 빈 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-172">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="35ca4-173">예제 12: 레코드 집합 만들기 및 모든 확인 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="35ca4-173">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="35ca4-174">이 명령은 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-174">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="35ca4-175">*Overwrite* 매개 변수를 사용 하면이 레코드 집합에서 이름 및 형식이 같은 기존 레코드 집합을 덮어쓰게 되며 해당 레코드 집합의 기존 레코드는 손실 됩니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-175">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="35ca4-176">값이 $False 인 *Confirm* 매개 변수는 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-176">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="35ca4-177">변수</span><span class="sxs-lookup"><span data-stu-id="35ca4-177">PARAMETERS</span></span>

### <span data-ttu-id="35ca4-178">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35ca4-178">-DefaultProfile</span></span>
<span data-ttu-id="35ca4-179">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="35ca4-179">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35ca4-180">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="35ca4-180">-DnsRecords</span></span>
<span data-ttu-id="35ca4-181">레코드 집합에 포함할 DNS 레코드의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-181">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="35ca4-182">New-AzureRmDnsRecordConfig cmdlet을 사용 하 여 DNS 레코드 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-182">You can use the New-AzureRmDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="35ca4-183">자세한 내용은 예제를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35ca4-183">See the examples for more information.</span></span>

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

### <span data-ttu-id="35ca4-184">-Metadata</span><span class="sxs-lookup"><span data-stu-id="35ca4-184">-Metadata</span></span>
<span data-ttu-id="35ca4-185">레코드 집합과 연결할 메타 데이터의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="35ca4-186">메타 데이터는 해시 테이블로 표시 되는 이름-값 쌍 (@ {"Name" = "dept")을 사용 하 여 지정 됩니다. "Value" = "장바구니"}, @ {"Name" = "env"; "Value" = "production"}).</span><span class="sxs-lookup"><span data-stu-id="35ca4-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @(@{"Name"="dept"; "Value"="shopping"}, @{"Name"="env"; "Value"="production"}).</span></span>

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

### <span data-ttu-id="35ca4-187">-이름</span><span class="sxs-lookup"><span data-stu-id="35ca4-187">-Name</span></span>
<span data-ttu-id="35ca4-188">만들 **레코드 집합** 의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="35ca4-189">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="35ca4-189">-Overwrite</span></span>
<span data-ttu-id="35ca4-190">이 cmdlet이 이미 존재 하는 경우 지정 된 **레코드 집합** 을 덮어쓰게 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="35ca4-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="35ca4-191">-RecordType</span></span>
<span data-ttu-id="35ca4-192">만들려는 DNS 레코드의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-192">Specifies the type of DNS record to create.</span></span>
<span data-ttu-id="35ca4-193">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-193">Valid values are:</span></span>
- <span data-ttu-id="35ca4-194">에서</span><span class="sxs-lookup"><span data-stu-id="35ca4-194">A</span></span>
- <span data-ttu-id="35ca4-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="35ca4-195">AAAA</span></span>
- <span data-ttu-id="35ca4-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="35ca4-196">CNAME</span></span>
- <span data-ttu-id="35ca4-197">멕시코</span><span class="sxs-lookup"><span data-stu-id="35ca4-197">MX</span></span>
- <span data-ttu-id="35ca4-198">NS</span><span class="sxs-lookup"><span data-stu-id="35ca4-198">NS</span></span>
- <span data-ttu-id="35ca4-199">PTR 레코드로</span><span class="sxs-lookup"><span data-stu-id="35ca4-199">PTR</span></span>
- <span data-ttu-id="35ca4-200">SRV</span><span class="sxs-lookup"><span data-stu-id="35ca4-200">SRV</span></span>
- <span data-ttu-id="35ca4-201">TXT SOA 레코드는 영역이 생성 될 때 자동으로 만들어지므로 수동으로 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

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

### <span data-ttu-id="35ca4-202">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35ca4-202">-ResourceGroupName</span></span>
<span data-ttu-id="35ca4-203">DNS 영역이 포함 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-203">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="35ca4-204">또한 *ZoneName* 매개 변수를 지정 하 여 영역 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-204">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>
<span data-ttu-id="35ca4-205">또는 *zone* 매개 변수를 사용 하 여 DNS 영역 개체를 전달 하 여 영역 및 리소스 그룹을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-205">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="35ca4-206">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="35ca4-206">-TargetResourceId</span></span>
<span data-ttu-id="35ca4-207">별칭 대상 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-207">Alias Target Resource Id.</span></span>

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

### <span data-ttu-id="35ca4-208">-Ttl</span><span class="sxs-lookup"><span data-stu-id="35ca4-208">-Ttl</span></span>
<span data-ttu-id="35ca4-209">DNS 레코드 집합에 대 한 TTL (Time to Live)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-209">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

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

### <span data-ttu-id="35ca4-210">-Zone</span><span class="sxs-lookup"><span data-stu-id="35ca4-210">-Zone</span></span>
<span data-ttu-id="35ca4-211">**레코드 집합** 을 만들 DnsZone를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-211">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="35ca4-212">또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용 하 여 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-212">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="35ca4-213">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="35ca4-213">-ZoneName</span></span>
<span data-ttu-id="35ca4-214">**레코드 집합** 을 만들 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-214">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="35ca4-215">또한 *ResourceGroupName* 매개 변수를 사용 하 여 영역을 포함 하는 리소스 그룹을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-215">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="35ca4-216">또는 *zone* 매개 변수를 사용 하 여 DNS 영역 개체를 전달 하 여 영역 및 리소스 그룹을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-216">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="35ca4-217">-확인</span><span class="sxs-lookup"><span data-stu-id="35ca4-217">-Confirm</span></span>
<span data-ttu-id="35ca4-218">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-218">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35ca4-219">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35ca4-219">-WhatIf</span></span>
<span data-ttu-id="35ca4-220">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-220">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35ca4-221">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-221">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35ca4-222">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ca4-222">CommonParameters</span></span>
<span data-ttu-id="35ca4-223">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-223">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35ca4-224">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35ca4-224">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ca4-225">입력</span><span class="sxs-lookup"><span data-stu-id="35ca4-225">INPUTS</span></span>

### <span data-ttu-id="35ca4-226">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="35ca4-226">System.String</span></span>

### <span data-ttu-id="35ca4-227">DnsZone에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="35ca4-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="35ca4-228">매개 변수: Zone (ByValue)</span><span class="sxs-lookup"><span data-stu-id="35ca4-228">Parameters: Zone (ByValue)</span></span>

### <span data-ttu-id="35ca4-229">시스템. UInt32</span><span class="sxs-lookup"><span data-stu-id="35ca4-229">System.UInt32</span></span>

### <span data-ttu-id="35ca4-230">RecordType를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-230">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="35ca4-231">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="35ca4-231">System.Collections.Hashtable</span></span>

### <span data-ttu-id="35ca4-232">Microsoft. Dns. DnsRecordBase []</span><span class="sxs-lookup"><span data-stu-id="35ca4-232">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span></span>
<span data-ttu-id="35ca4-233">매개 변수: DnsRecords (ByValue)</span><span class="sxs-lookup"><span data-stu-id="35ca4-233">Parameters: DnsRecords (ByValue)</span></span>

## <span data-ttu-id="35ca4-234">출력</span><span class="sxs-lookup"><span data-stu-id="35ca4-234">OUTPUTS</span></span>

### <span data-ttu-id="35ca4-235">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="35ca4-235">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="35ca4-236">상속자</span><span class="sxs-lookup"><span data-stu-id="35ca4-236">NOTES</span></span>
<span data-ttu-id="35ca4-237">*확인* 매개 변수를 사용 하 여이 cmdlet이 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-237">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="35ca4-238">기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 변수의 값이 중간 인지 아래 인지 여부를 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-238">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="35ca4-239">*확인* 또는 *확인: $True* 를 지정 하는 경우이 cmdlet을 실행 하기 전에 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-239">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="35ca4-240">*확인: $False* 를 지정 하면 cmdlet에서 확인을 요구 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35ca4-240">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="35ca4-241">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35ca4-241">RELATED LINKS</span></span>

[<span data-ttu-id="35ca4-242">추가-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="35ca4-242">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="35ca4-243">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="35ca4-243">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="35ca4-244">새로운 AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="35ca4-244">New-AzureRmDnsRecordConfig</span></span>](./New-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="35ca4-245">제거-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="35ca4-245">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="35ca4-246">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="35ca4-246">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
