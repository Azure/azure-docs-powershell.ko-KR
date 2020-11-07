---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordSet.md
ms.openlocfilehash: 9896a8e1cfd2e3c0dc3887513d93e902260b82c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704031"
---
# <span data-ttu-id="9ce7e-101">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9ce7e-101">New-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="9ce7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ce7e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ce7e-103">DNS 레코드 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-103">Creates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ce7e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ce7e-104">SYNTAX</span></span>

### <span data-ttu-id="9ce7e-105">필드인</span><span class="sxs-lookup"><span data-stu-id="9ce7e-105">Fields</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ce7e-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="9ce7e-106">Object</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ce7e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9ce7e-107">DESCRIPTION</span></span>
<span data-ttu-id="9ce7e-108">**AzureRmDnsRecordSet** cmdlet은 지정 된 이름 및 유형을 가진 새 DNS (Domain Name System) 레코드 집합을 지정한 영역에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-108">The **New-AzureRmDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="9ce7e-109">**레코드 집합** 개체는 이름 및 형식이 같은 DNS 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-109">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="9ce7e-110">이름은 영역에 대해 상대적 이며 정규화 된 이름이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-110">Note that the name is relative to the zone and not the fully qualified name.</span></span>

<span data-ttu-id="9ce7e-111">*Dnsrecords* 매개 변수는 레코드 집합의 레코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-111">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="9ce7e-112">이 매개 변수는 New-AzureRmDnsRecordConfig를 사용 하 여 생성 된 DNS 레코드 배열을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-112">This parameter takes an array of DNS records, constructed using New-AzureRmDnsRecordConfig.</span></span>

<span data-ttu-id="9ce7e-113">파이프라인 연산자를 사용 하 여 **DnsZone** 개체를이 cmdlet에 전달 하거나, **DnsZone** 개체를 *zone* 매개 변수로 전달 하거나, 이름을 기준으로 영역을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-113">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>

<span data-ttu-id="9ce7e-114">*확인* 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-114">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="9ce7e-115">일치 하는 **레코드 집합** (이름 및 레코드 형식)이 이미 있는 경우 *Overwrite* 매개 변수를 지정 해야 하며 그렇지 않으면 Cmdlet에서 새 **레코드 집합** 을 만들지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-115">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="9ce7e-116">예제의</span><span class="sxs-lookup"><span data-stu-id="9ce7e-116">EXAMPLES</span></span>

### <span data-ttu-id="9ce7e-117">예제 1: 형식 A의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="9ce7e-117">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="9ce7e-118">이 예제에서는 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="9ce7e-119">레코드 집합은 A 형식이 고 TTL은 1 시간 (3600 초)입니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9ce7e-120">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="9ce7e-121">예제 2: AAAA 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="9ce7e-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="9ce7e-122">이 예제에서는 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="9ce7e-123">레코드 집합은 AAAA 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9ce7e-124">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-124">It contains a single DNS record.</span></span>

<span data-ttu-id="9ce7e-125">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9ce7e-126">예제 3: CNAME 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="9ce7e-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="9ce7e-127">이 예제에서는 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="9ce7e-128">레코드 집합은 CNAME 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9ce7e-129">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-129">It contains a single DNS record.</span></span>

<span data-ttu-id="9ce7e-130">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9ce7e-131">예제 4: MX 유형의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="9ce7e-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="9ce7e-132">이 명령은 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="9ce7e-133">레코드 집합은 MX 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9ce7e-134">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-134">It contains a single DNS record.</span></span>

<span data-ttu-id="9ce7e-135">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9ce7e-136">예제 5: NS 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="9ce7e-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="9ce7e-137">이 명령은 zone myzone.com에 ns1 이라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="9ce7e-138">레코드 집합은 NS 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9ce7e-139">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-139">It contains a single DNS record.</span></span>

<span data-ttu-id="9ce7e-140">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9ce7e-141">예제 6: 형식 PTR의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="9ce7e-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="9ce7e-142">이 명령은 zone 3.2.1.in-in-addr.arpa에 4 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="9ce7e-143">레코드 집합은 PTR 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9ce7e-144">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-144">It contains a single DNS record.</span></span>

<span data-ttu-id="9ce7e-145">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9ce7e-146">예제 7: SRV 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="9ce7e-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="9ce7e-147">이 명령은 zone myzone.com에서 _sip 이라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="9ce7e-148">레코드 집합은 SRV 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9ce7e-149">IP 주소 2001.2.3.4를 가리키는 단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="9ce7e-150">서비스 (sip) 및 프로토콜 (tcp)은 레코드 데이터의 일부가 아닌 레코드 집합 이름의 일부로 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="9ce7e-151">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9ce7e-152">예제 8: TXT 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="9ce7e-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="9ce7e-153">이 명령은 zone myzone.com에 text 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="9ce7e-154">레코드 집합은 TXT 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9ce7e-155">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-155">It contains a single DNS record.</span></span>

<span data-ttu-id="9ce7e-156">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9ce7e-157">예제 9: zone apex에서 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="9ce7e-157">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="9ce7e-158">이 명령은 myzone.com 영역의 apex (또는 루트)에서 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-158">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="9ce7e-159">이렇게 하려면 레코드 집합 이름이 "@"로 지정 됩니다 (큰따옴표 포함).</span><span class="sxs-lookup"><span data-stu-id="9ce7e-159">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>

<span data-ttu-id="9ce7e-160">영역 apex에서 CNAME 레코드를 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-160">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="9ce7e-161">이것은 DNS 표준의 제약 조건입니다. Azure DNS의 제한이 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-161">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>

<span data-ttu-id="9ce7e-162">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-162">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9ce7e-163">예제 10: 와일드 카드 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="9ce7e-163">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="9ce7e-164">이 명령은 zone myzone.com에 \* 이라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-164">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="9ce7e-165">와일드 카드 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-165">This is a wildcard record set.</span></span>

<span data-ttu-id="9ce7e-166">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-166">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9ce7e-167">예제 11: 빈 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="9ce7e-167">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="9ce7e-168">이 명령은 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-168">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="9ce7e-169">레코드 집합은 A 형식이 고 TTL은 1 시간 (3600 초)입니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-169">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="9ce7e-170">나중에 레코드를 추가할 수 있는 자리 표시자 역할을 하는 빈 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-170">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="9ce7e-171">예제 12: 레코드 집합 만들기 및 모든 확인 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="9ce7e-171">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="9ce7e-172">이 명령은 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-172">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="9ce7e-173">*Overwrite* 매개 변수를 사용 하면이 레코드 집합에서 이름 및 형식이 같은 기존 레코드 집합을 덮어쓰게 되며 해당 레코드 집합의 기존 레코드는 손실 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-173">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="9ce7e-174">값이 $False 인 *Confirm* 매개 변수는 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-174">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="9ce7e-175">변수</span><span class="sxs-lookup"><span data-stu-id="9ce7e-175">PARAMETERS</span></span>

### <span data-ttu-id="9ce7e-176">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ce7e-176">-DefaultProfile</span></span>
<span data-ttu-id="9ce7e-177">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9ce7e-177">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ce7e-178">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="9ce7e-178">-DnsRecords</span></span>
<span data-ttu-id="9ce7e-179">레코드 집합에 포함할 DNS 레코드의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-179">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="9ce7e-180">New-AzureRmDnsRecordConfig cmdlet을 사용 하 여 DNS 레코드 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-180">You can use the New-AzureRmDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="9ce7e-181">자세한 내용은 예제를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-181">See the examples for more information.</span></span>

```yaml
Type: DnsRecordBase[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ce7e-182">-Force</span><span class="sxs-lookup"><span data-stu-id="9ce7e-182">-Force</span></span>
<span data-ttu-id="9ce7e-183">이 매개 변수는이 cmdlet에 대해 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-183">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="9ce7e-184">이후 릴리스에서 제거 될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-184">It will be removed in a future release.</span></span>

<span data-ttu-id="9ce7e-185">이 cmdlet이 comfirmation를 묻는 메시지를 표시할지 여부를 제어 하려면 *Confirm* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-185">To control whether this cmdlet prompts you for comfirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="9ce7e-186">-Metadata</span><span class="sxs-lookup"><span data-stu-id="9ce7e-186">-Metadata</span></span>
<span data-ttu-id="9ce7e-187">레코드 집합과 연결할 메타 데이터의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-187">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="9ce7e-188">메타 데이터는 해시 테이블로 표시 되는 이름-값 쌍 (@ {"Name" = "dept")을 사용 하 여 지정 됩니다. "Value" = "장바구니"}, @ {"Name" = "env"; "Value" = "production"}).</span><span class="sxs-lookup"><span data-stu-id="9ce7e-188">Metadata is specified using name-value pairs that are represented as hash tables, for example @(@{"Name"="dept"; "Value"="shopping"}, @{"Name"="env"; "Value"="production"}).</span></span>

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

### <span data-ttu-id="9ce7e-189">-이름</span><span class="sxs-lookup"><span data-stu-id="9ce7e-189">-Name</span></span>
<span data-ttu-id="9ce7e-190">만들 **레코드 집합** 의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-190">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="9ce7e-191">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="9ce7e-191">-Overwrite</span></span>
<span data-ttu-id="9ce7e-192">이 cmdlet이 이미 존재 하는 경우 지정 된 **레코드 집합** 을 덮어쓰게 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-192">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="9ce7e-193">-RecordType</span><span class="sxs-lookup"><span data-stu-id="9ce7e-193">-RecordType</span></span>
<span data-ttu-id="9ce7e-194">만들려는 DNS 레코드의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-194">Specifies the type of DNS record to create.</span></span>

<span data-ttu-id="9ce7e-195">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-195">Valid values are:</span></span>

- <span data-ttu-id="9ce7e-196">에서</span><span class="sxs-lookup"><span data-stu-id="9ce7e-196">A</span></span>
- <span data-ttu-id="9ce7e-197">AAAA</span><span class="sxs-lookup"><span data-stu-id="9ce7e-197">AAAA</span></span>
- <span data-ttu-id="9ce7e-198">CNAME</span><span class="sxs-lookup"><span data-stu-id="9ce7e-198">CNAME</span></span>
- <span data-ttu-id="9ce7e-199">멕시코</span><span class="sxs-lookup"><span data-stu-id="9ce7e-199">MX</span></span>
- <span data-ttu-id="9ce7e-200">NS</span><span class="sxs-lookup"><span data-stu-id="9ce7e-200">NS</span></span>
- <span data-ttu-id="9ce7e-201">PTR 레코드로</span><span class="sxs-lookup"><span data-stu-id="9ce7e-201">PTR</span></span>
- <span data-ttu-id="9ce7e-202">SRV</span><span class="sxs-lookup"><span data-stu-id="9ce7e-202">SRV</span></span>
- <span data-ttu-id="9ce7e-203">라는</span><span class="sxs-lookup"><span data-stu-id="9ce7e-203">TXT</span></span>

<span data-ttu-id="9ce7e-204">SOA 레코드는 영역을 만들 때 자동으로 만들어지므로 수동으로 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-204">SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ce7e-205">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ce7e-205">-ResourceGroupName</span></span>
<span data-ttu-id="9ce7e-206">DNS 영역이 포함 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-206">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="9ce7e-207">또한 *ZoneName* 매개 변수를 지정 하 여 영역 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-207">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>

<span data-ttu-id="9ce7e-208">또는 *zone* 매개 변수를 사용 하 여 DNS 영역 개체를 전달 하 여 영역 및 리소스 그룹을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-208">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ce7e-209">-Ttl</span><span class="sxs-lookup"><span data-stu-id="9ce7e-209">-Ttl</span></span>
<span data-ttu-id="9ce7e-210">DNS 레코드 집합에 대 한 TTL (Time to Live)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-210">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ce7e-211">-Zone</span><span class="sxs-lookup"><span data-stu-id="9ce7e-211">-Zone</span></span>
<span data-ttu-id="9ce7e-212">**레코드 집합** 을 만들 DnsZone를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-212">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="9ce7e-213">또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용 하 여 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-213">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ce7e-214">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="9ce7e-214">-ZoneName</span></span>
<span data-ttu-id="9ce7e-215">**레코드 집합** 을 만들 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-215">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="9ce7e-216">또한 *ResourceGroupName* 매개 변수를 사용 하 여 영역을 포함 하는 리소스 그룹을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-216">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="9ce7e-217">또는 *zone* 매개 변수를 사용 하 여 DNS 영역 개체를 전달 하 여 영역 및 리소스 그룹을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-217">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ce7e-218">-확인</span><span class="sxs-lookup"><span data-stu-id="9ce7e-218">-Confirm</span></span>
<span data-ttu-id="9ce7e-219">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ce7e-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ce7e-220">-WhatIf</span></span>
<span data-ttu-id="9ce7e-221">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ce7e-222">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ce7e-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ce7e-223">CommonParameters</span></span>
<span data-ttu-id="9ce7e-224">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ce7e-225">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ce7e-225">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ce7e-226">입력</span><span class="sxs-lookup"><span data-stu-id="9ce7e-226">INPUTS</span></span>

### <span data-ttu-id="9ce7e-227">DnsZone에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="9ce7e-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="9ce7e-228">DnsZone 개체를이 cmdlet에 파이프 하 여 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-228">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="9ce7e-229">출력</span><span class="sxs-lookup"><span data-stu-id="9ce7e-229">OUTPUTS</span></span>

### <span data-ttu-id="9ce7e-230">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9ce7e-230">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="9ce7e-231">이 cmdlet은 **레코드 집합** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-231">This cmdlet returns a **RecordSet** object.</span></span>

## <span data-ttu-id="9ce7e-232">상속자</span><span class="sxs-lookup"><span data-stu-id="9ce7e-232">NOTES</span></span>
<span data-ttu-id="9ce7e-233">*확인* 매개 변수를 사용 하 여이 cmdlet이 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-233">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="9ce7e-234">기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 변수의 값이 중간 인지 아래 인지 여부를 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-234">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="9ce7e-235">*확인* 또는 *확인: $True* 를 지정 하는 경우이 cmdlet을 실행 하기 전에 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-235">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="9ce7e-236">*확인: $False* 를 지정 하면 cmdlet에서 확인을 요구 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ce7e-236">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9ce7e-237">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ce7e-237">RELATED LINKS</span></span>

[<span data-ttu-id="9ce7e-238">추가-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="9ce7e-238">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="9ce7e-239">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9ce7e-239">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="9ce7e-240">새로운 AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="9ce7e-240">New-AzureRmDnsRecordConfig</span></span>](./New-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="9ce7e-241">제거-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9ce7e-241">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="9ce7e-242">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9ce7e-242">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
