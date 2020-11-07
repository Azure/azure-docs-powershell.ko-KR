---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6368cffa168772a384deb99f5a8388aef84f85b2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882249"
---
# <span data-ttu-id="ea960-101">New-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="ea960-101">New-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="ea960-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea960-102">SYNOPSIS</span></span>
<span data-ttu-id="ea960-103">새 DNS 레코드 로컬 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-103">Creates a new DNS record local object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea960-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea960-104">SYNTAX</span></span>

### <span data-ttu-id="ea960-105">에서</span><span class="sxs-lookup"><span data-stu-id="ea960-105">A</span></span>
```
New-AzureRmDnsRecordConfig -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="ea960-106">Aaaa</span><span class="sxs-lookup"><span data-stu-id="ea960-106">Aaaa</span></span>
```
New-AzureRmDnsRecordConfig -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="ea960-107">Ns</span><span class="sxs-lookup"><span data-stu-id="ea960-107">Ns</span></span>
```
New-AzureRmDnsRecordConfig -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="ea960-108">멕시코</span><span class="sxs-lookup"><span data-stu-id="ea960-108">Mx</span></span>
```
New-AzureRmDnsRecordConfig -Exchange <String> -Preference <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="ea960-109">Ptr 레코드로</span><span class="sxs-lookup"><span data-stu-id="ea960-109">Ptr</span></span>
```
New-AzureRmDnsRecordConfig -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="ea960-110">라는</span><span class="sxs-lookup"><span data-stu-id="ea960-110">Txt</span></span>
```
New-AzureRmDnsRecordConfig -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="ea960-111">Srv</span><span class="sxs-lookup"><span data-stu-id="ea960-111">Srv</span></span>
```
New-AzureRmDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="ea960-112">CName</span><span class="sxs-lookup"><span data-stu-id="ea960-112">CName</span></span>
```
New-AzureRmDnsRecordConfig -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="ea960-113">설명은</span><span class="sxs-lookup"><span data-stu-id="ea960-113">DESCRIPTION</span></span>
<span data-ttu-id="ea960-114">**AzureRmDnsRecordConfig** cmdlet은 로컬 **dnsrecord** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-114">The **New-AzureRmDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="ea960-115">이 개체의 배열은 *dnsrecords* 매개 변수를 사용 하 여 New-AzureRmDnsRecordSet cmdlet에 전달 되며, 레코드 집합에서 만들 레코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-115">An array of these objects is passed to the New-AzureRmDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="ea960-116">예제의</span><span class="sxs-lookup"><span data-stu-id="ea960-116">EXAMPLES</span></span>

### <span data-ttu-id="ea960-117">예제 1: 형식 A의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="ea960-117">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="ea960-118">이 예제에서는 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="ea960-119">레코드 집합은 A 형식이 고 TTL은 1 시간 (3600 초)입니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ea960-120">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="ea960-121">예제 2: AAAA 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="ea960-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ea960-122">이 예제에서는 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="ea960-123">레코드 집합은 AAAA 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ea960-124">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-124">It contains a single DNS record.</span></span>

<span data-ttu-id="ea960-125">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea960-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ea960-126">예제 3: CNAME 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="ea960-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ea960-127">이 예제에서는 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="ea960-128">레코드 집합은 CNAME 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ea960-129">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-129">It contains a single DNS record.</span></span>

<span data-ttu-id="ea960-130">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea960-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ea960-131">예제 4: MX 유형의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="ea960-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ea960-132">이 명령은 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="ea960-133">레코드 집합은 MX 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ea960-134">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-134">It contains a single DNS record.</span></span>

<span data-ttu-id="ea960-135">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea960-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ea960-136">예제 5: NS 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="ea960-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ea960-137">이 명령은 zone myzone.com에 ns1 이라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="ea960-138">레코드 집합은 NS 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ea960-139">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-139">It contains a single DNS record.</span></span>

<span data-ttu-id="ea960-140">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea960-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ea960-141">예제 6: 형식 PTR의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="ea960-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="ea960-142">이 명령은 zone 3.2.1.in-in-addr.arpa에 4 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="ea960-143">레코드 집합은 PTR 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ea960-144">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-144">It contains a single DNS record.</span></span>

<span data-ttu-id="ea960-145">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea960-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ea960-146">예제 7: SRV 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="ea960-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ea960-147">이 명령은 zone myzone.com에서 _sip 이라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="ea960-148">레코드 집합은 SRV 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ea960-149">IP 주소 2001.2.3.4를 가리키는 단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="ea960-150">서비스 (sip) 및 프로토콜 (tcp)은 레코드 데이터의 일부가 아닌 레코드 집합 이름의 일부로 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="ea960-151">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea960-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="ea960-152">예제 8: TXT 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="ea960-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="ea960-153">이 명령은 zone myzone.com에 text 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="ea960-154">레코드 집합은 TXT 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="ea960-155">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-155">It contains a single DNS record.</span></span>

<span data-ttu-id="ea960-156">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea960-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="ea960-157">변수</span><span class="sxs-lookup"><span data-stu-id="ea960-157">PARAMETERS</span></span>

### <span data-ttu-id="ea960-158">-Cname</span><span class="sxs-lookup"><span data-stu-id="ea960-158">-Cname</span></span>
<span data-ttu-id="ea960-159">CNAME (정식 이름) 레코드에 대 한 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-159">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea960-160">-Exchange</span><span class="sxs-lookup"><span data-stu-id="ea960-160">-Exchange</span></span>
<span data-ttu-id="ea960-161">메일 교환 (MX) 레코드의 메일 교환 서버 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-161">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea960-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="ea960-162">-Ipv4Address</span></span>
<span data-ttu-id="ea960-163">A 레코드에 대 한 IPv4 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-163">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="ea960-164">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="ea960-164">-Ipv6Address</span></span>
<span data-ttu-id="ea960-165">AAAA 레코드에 대 한 IPv6 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-165">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: Aaaa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea960-166">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="ea960-166">-Nsdname</span></span>
<span data-ttu-id="ea960-167">NS (이름 서버) 레코드에 대 한 이름 서버 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-167">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: Ns
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea960-168">-포트</span><span class="sxs-lookup"><span data-stu-id="ea960-168">-Port</span></span>
<span data-ttu-id="ea960-169">서비스 (SRV) 레코드의 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-169">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea960-170">-기본 설정</span><span class="sxs-lookup"><span data-stu-id="ea960-170">-Preference</span></span>
<span data-ttu-id="ea960-171">MX 레코드에 대 한 기본 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-171">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea960-172">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="ea960-172">-Priority</span></span>
<span data-ttu-id="ea960-173">SRV 레코드에 대 한 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-173">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea960-174">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="ea960-174">-Ptrdname</span></span>
<span data-ttu-id="ea960-175">PTR (포인터 리소스) 레코드의 대상 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-175">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: Ptr
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea960-176">-대상</span><span class="sxs-lookup"><span data-stu-id="ea960-176">-Target</span></span>
<span data-ttu-id="ea960-177">SRV 레코드의 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-177">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea960-178">-값</span><span class="sxs-lookup"><span data-stu-id="ea960-178">-Value</span></span>
<span data-ttu-id="ea960-179">TXT 레코드에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-179">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: Txt
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea960-180">-중량</span><span class="sxs-lookup"><span data-stu-id="ea960-180">-Weight</span></span>
<span data-ttu-id="ea960-181">SRV 레코드의 가중치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-181">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea960-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea960-182">CommonParameters</span></span>
<span data-ttu-id="ea960-183">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea960-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea960-184">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea960-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea960-185">입력</span><span class="sxs-lookup"><span data-stu-id="ea960-185">INPUTS</span></span>

### <span data-ttu-id="ea960-186">않아야.</span><span class="sxs-lookup"><span data-stu-id="ea960-186">None.</span></span>

## <span data-ttu-id="ea960-187">출력</span><span class="sxs-lookup"><span data-stu-id="ea960-187">OUTPUTS</span></span>

### <span data-ttu-id="ea960-188">Microsoft. Dns. DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="ea960-188">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="ea960-189">상속자</span><span class="sxs-lookup"><span data-stu-id="ea960-189">NOTES</span></span>

## <span data-ttu-id="ea960-190">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea960-190">RELATED LINKS</span></span>

[<span data-ttu-id="ea960-191">추가-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="ea960-191">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="ea960-192">새로운 AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ea960-192">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="ea960-193">제거-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="ea960-193">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)
