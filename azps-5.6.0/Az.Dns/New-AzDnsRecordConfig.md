---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: c85cc0b4ad60529cc57becb9ca864751d90a37c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984802"
---
# <span data-ttu-id="8f8b5-101">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="8f8b5-101">New-AzDnsRecordConfig</span></span>

## <span data-ttu-id="8f8b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f8b5-102">SYNOPSIS</span></span>
<span data-ttu-id="8f8b5-103">새 DNS 레코드 로컬 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-103">Creates a new DNS record local object.</span></span>

## <span data-ttu-id="8f8b5-104">구문</span><span class="sxs-lookup"><span data-stu-id="8f8b5-104">SYNTAX</span></span>

### <span data-ttu-id="8f8b5-105">A</span><span class="sxs-lookup"><span data-stu-id="8f8b5-105">A</span></span>
```
New-AzDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f8b5-106">Aaaa</span><span class="sxs-lookup"><span data-stu-id="8f8b5-106">Aaaa</span></span>
```
New-AzDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f8b5-107">Ns</span><span class="sxs-lookup"><span data-stu-id="8f8b5-107">Ns</span></span>
```
New-AzDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f8b5-108">Mx</span><span class="sxs-lookup"><span data-stu-id="8f8b5-108">Mx</span></span>
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f8b5-109">Ptr</span><span class="sxs-lookup"><span data-stu-id="8f8b5-109">Ptr</span></span>
```
New-AzDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f8b5-110">Txt</span><span class="sxs-lookup"><span data-stu-id="8f8b5-110">Txt</span></span>
```
New-AzDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f8b5-111">Srv</span><span class="sxs-lookup"><span data-stu-id="8f8b5-111">Srv</span></span>
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f8b5-112">CName</span><span class="sxs-lookup"><span data-stu-id="8f8b5-112">CName</span></span>
```
New-AzDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f8b5-113">Caa</span><span class="sxs-lookup"><span data-stu-id="8f8b5-113">Caa</span></span>
```
New-AzDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f8b5-114">설명</span><span class="sxs-lookup"><span data-stu-id="8f8b5-114">DESCRIPTION</span></span>
<span data-ttu-id="8f8b5-115">**New-AzDnsRecordConfig** cmdlet은 로컬 **DnsRecord 개체를 만듭니다.**</span><span class="sxs-lookup"><span data-stu-id="8f8b5-115">The **New-AzDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="8f8b5-116">이러한 개체의 배열은 *dnsRecords* 매개 변수를 사용하여 New-AzDnsRecordSet cmdlet에 전달되어 레코드 집합에서 만들 레코드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-116">An array of these objects is passed to the New-AzDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="8f8b5-117">예제</span><span class="sxs-lookup"><span data-stu-id="8f8b5-117">EXAMPLES</span></span>

### <span data-ttu-id="8f8b5-118">예제 1: A 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="8f8b5-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="8f8b5-119">이 예제에서는 영역 집합에 www라는 **RecordSet을** myzone.com.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-119">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="8f8b5-120">레코드 집합은 A 형식의 TTL이 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="8f8b5-121">단일 DNS 레코드가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-121">It contains a single DNS record.</span></span>

### <span data-ttu-id="8f8b5-122">예제 2: AAAA 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="8f8b5-122">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="8f8b5-123">이 예제에서는 영역 집합에 www라는 **RecordSet을** myzone.com.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-123">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="8f8b5-124">레코드 집합은 AAAA 형식이고 TTL이 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="8f8b5-125">단일 DNS 레코드가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-125">It contains a single DNS record.</span></span>
<span data-ttu-id="8f8b5-126">한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드 집합을 만들 경우 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-126">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="8f8b5-127">예제 3: CNAME 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="8f8b5-127">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="8f8b5-128">이 예제에서는 영역 집합에 www라는 **RecordSet을** myzone.com.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-128">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="8f8b5-129">레코드 집합은 CNAME 형식이며 TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="8f8b5-130">단일 DNS 레코드가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-130">It contains a single DNS record.</span></span>
<span data-ttu-id="8f8b5-131">한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드 집합을 만들 경우 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-131">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="8f8b5-132">예제 4: MX 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="8f8b5-132">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="8f8b5-133">이 명령은 영역 집합에 www라는 **RecordSet을** myzone.com.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-133">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="8f8b5-134">레코드 집합은 MX 형식이고 TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="8f8b5-135">단일 DNS 레코드가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-135">It contains a single DNS record.</span></span>
<span data-ttu-id="8f8b5-136">한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드 집합을 만들 경우 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-136">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="8f8b5-137">예제 5: NS 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="8f8b5-137">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="8f8b5-138">이 명령은 해당 영역의 ns1이라는 **RecordSet을** myzone.com.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-138">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="8f8b5-139">레코드 집합은 NS 형식이고 TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-139">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="8f8b5-140">단일 DNS 레코드가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-140">It contains a single DNS record.</span></span>
<span data-ttu-id="8f8b5-141">한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드 집합을 만들 경우 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-141">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="8f8b5-142">예제 6: PTR 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="8f8b5-142">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="8f8b5-143">이 명령은 **4라는 RecordSet을** 3.2.1.in-addr.arpa를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-143">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="8f8b5-144">레코드 집합은 PTR 형식으로, TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-144">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="8f8b5-145">단일 DNS 레코드가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-145">It contains a single DNS record.</span></span>
<span data-ttu-id="8f8b5-146">한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드 집합을 만들 경우 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-146">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="8f8b5-147">예제 7: SRV 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="8f8b5-147">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="8f8b5-148">이 명령은 _sip._tcp라는 **RecordSet을** myzone.com.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-148">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="8f8b5-149">레코드 집합은 SRV 형식이고 TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-149">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="8f8b5-150">IP 주소 2001.2.3.4를 지적하는 단일 DNS 레코드가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-150">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="8f8b5-151">서비스(sip) 및 프로토콜(tcp)은 레코드 데이터의 일부가 아닌 레코드 집합 이름의 일부로 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-151">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="8f8b5-152">한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드 집합을 만들 경우 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-152">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="8f8b5-153">예제 8: TXT 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="8f8b5-153">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="8f8b5-154">이 명령은 영역의 **레코드 집합이라는** myzone.com.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-154">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="8f8b5-155">레코드 집합은 TXT 형식이며 TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-155">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="8f8b5-156">단일 DNS 레코드가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-156">It contains a single DNS record.</span></span>
<span data-ttu-id="8f8b5-157">한 줄의 레코드만 사용하여 **RecordSet을** 만들거나 pn_PowerShell_short 레코드 집합을 만들 경우 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-157">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="8f8b5-158">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8f8b5-158">PARAMETERS</span></span>

### <span data-ttu-id="8f8b5-159">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="8f8b5-159">-CaaFlags</span></span>
<span data-ttu-id="8f8b5-160">추가할 CAA 레코드의 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-160">The flags for the CAA record to add.</span></span> <span data-ttu-id="8f8b5-161">0에서 255 사이의 숫자가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-161">Must be a number between 0 and 255.</span></span>

```yaml
Type: System.Byte
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f8b5-162">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="8f8b5-162">-CaaTag</span></span>
<span data-ttu-id="8f8b5-163">추가할 CAA 레코드의 태그 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-163">The tag field of the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f8b5-164">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="8f8b5-164">-CaaValue</span></span>
<span data-ttu-id="8f8b5-165">추가할 CAA 레코드의 값 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-165">The value field for the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f8b5-166">-Cname</span><span class="sxs-lookup"><span data-stu-id="8f8b5-166">-Cname</span></span>
<span data-ttu-id="8f8b5-167">CNAME(정형 이름) 레코드에 대한 도메인 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-167">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f8b5-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f8b5-168">-DefaultProfile</span></span>
<span data-ttu-id="8f8b5-169">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8f8b5-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f8b5-170">-Exchange</span><span class="sxs-lookup"><span data-stu-id="8f8b5-170">-Exchange</span></span>
<span data-ttu-id="8f8b5-171">MX(메일 교환) 레코드에 대한 메일 교환 서버 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-171">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f8b5-172">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="8f8b5-172">-Ipv4Address</span></span>
<span data-ttu-id="8f8b5-173">A 레코드에 대한 IPv4 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-173">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="8f8b5-174">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="8f8b5-174">-Ipv6Address</span></span>
<span data-ttu-id="8f8b5-175">AAAA 레코드에 대한 IPv6 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-175">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: Aaaa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f8b5-176">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="8f8b5-176">-Nsdname</span></span>
<span data-ttu-id="8f8b5-177">NS(이름 서버) 레코드의 이름 서버 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-177">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Ns
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f8b5-178">-Port</span><span class="sxs-lookup"><span data-stu-id="8f8b5-178">-Port</span></span>
<span data-ttu-id="8f8b5-179">SRV(서비스) 레코드에 대한 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-179">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f8b5-180">-기본 설정</span><span class="sxs-lookup"><span data-stu-id="8f8b5-180">-Preference</span></span>
<span data-ttu-id="8f8b5-181">MX 레코드에 대한 기본 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-181">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f8b5-182">-Priority</span><span class="sxs-lookup"><span data-stu-id="8f8b5-182">-Priority</span></span>
<span data-ttu-id="8f8b5-183">SRV 레코드에 대한 우선 순위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-183">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f8b5-184">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="8f8b5-184">-Ptrdname</span></span>
<span data-ttu-id="8f8b5-185">포인터 리소스(PTR) 레코드의 대상 도메인 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-185">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Ptr
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f8b5-186">-Target</span><span class="sxs-lookup"><span data-stu-id="8f8b5-186">-Target</span></span>
<span data-ttu-id="8f8b5-187">SRV 레코드에 대한 대상을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-187">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f8b5-188">-Value</span><span class="sxs-lookup"><span data-stu-id="8f8b5-188">-Value</span></span>
<span data-ttu-id="8f8b5-189">TXT 레코드의 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-189">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: Txt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f8b5-190">-Weight</span><span class="sxs-lookup"><span data-stu-id="8f8b5-190">-Weight</span></span>
<span data-ttu-id="8f8b5-191">SRV 레코드에 대한 가중치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-191">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f8b5-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f8b5-192">CommonParameters</span></span>
<span data-ttu-id="8f8b5-193">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f8b5-194">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8f8b5-194">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f8b5-195">입력</span><span class="sxs-lookup"><span data-stu-id="8f8b5-195">INPUTS</span></span>

### <span data-ttu-id="8f8b5-196">System.String</span><span class="sxs-lookup"><span data-stu-id="8f8b5-196">System.String</span></span>

### <span data-ttu-id="8f8b5-197">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="8f8b5-197">System.UInt16</span></span>

### <span data-ttu-id="8f8b5-198">System.Byte</span><span class="sxs-lookup"><span data-stu-id="8f8b5-198">System.Byte</span></span>

## <span data-ttu-id="8f8b5-199">출력</span><span class="sxs-lookup"><span data-stu-id="8f8b5-199">OUTPUTS</span></span>

### <span data-ttu-id="8f8b5-200">Microsoft.Azure.Commands.Dns.DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="8f8b5-200">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="8f8b5-201">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8f8b5-201">NOTES</span></span>

## <span data-ttu-id="8f8b5-202">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f8b5-202">RELATED LINKS</span></span>

[<span data-ttu-id="8f8b5-203">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="8f8b5-203">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="8f8b5-204">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="8f8b5-204">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="8f8b5-205">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="8f8b5-205">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)
