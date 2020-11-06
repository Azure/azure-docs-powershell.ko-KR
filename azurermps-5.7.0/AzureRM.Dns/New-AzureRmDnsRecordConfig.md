---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordConfig.md
ms.openlocfilehash: f44472ac83c1d92baab5d4c7c3b4c8d325e3dfbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532844"
---
# <span data-ttu-id="276b8-101">New-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="276b8-101">New-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="276b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="276b8-102">SYNOPSIS</span></span>
<span data-ttu-id="276b8-103">새 DNS 레코드 로컬 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-103">Creates a new DNS record local object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="276b8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="276b8-104">SYNTAX</span></span>

### <span data-ttu-id="276b8-105">에서</span><span class="sxs-lookup"><span data-stu-id="276b8-105">A</span></span>
```
New-AzureRmDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="276b8-106">Aaaa</span><span class="sxs-lookup"><span data-stu-id="276b8-106">Aaaa</span></span>
```
New-AzureRmDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="276b8-107">Ns</span><span class="sxs-lookup"><span data-stu-id="276b8-107">Ns</span></span>
```
New-AzureRmDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="276b8-108">멕시코</span><span class="sxs-lookup"><span data-stu-id="276b8-108">Mx</span></span>
```
New-AzureRmDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="276b8-109">Ptr 레코드로</span><span class="sxs-lookup"><span data-stu-id="276b8-109">Ptr</span></span>
```
New-AzureRmDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="276b8-110">라는</span><span class="sxs-lookup"><span data-stu-id="276b8-110">Txt</span></span>
```
New-AzureRmDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="276b8-111">Srv</span><span class="sxs-lookup"><span data-stu-id="276b8-111">Srv</span></span>
```
New-AzureRmDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="276b8-112">CName</span><span class="sxs-lookup"><span data-stu-id="276b8-112">CName</span></span>
```
New-AzureRmDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="276b8-113">Caa</span><span class="sxs-lookup"><span data-stu-id="276b8-113">Caa</span></span>
```
New-AzureRmDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="276b8-114">설명은</span><span class="sxs-lookup"><span data-stu-id="276b8-114">DESCRIPTION</span></span>
<span data-ttu-id="276b8-115">**AzureRmDnsRecordConfig** cmdlet은 로컬 **dnsrecord** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-115">The **New-AzureRmDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="276b8-116">이 개체의 배열은 *dnsrecords* 매개 변수를 사용 하 여 New-AzureRmDnsRecordSet cmdlet에 전달 되며, 레코드 집합에서 만들 레코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-116">An array of these objects is passed to the New-AzureRmDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="276b8-117">예제의</span><span class="sxs-lookup"><span data-stu-id="276b8-117">EXAMPLES</span></span>

### <span data-ttu-id="276b8-118">예제 1: 형식 A의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="276b8-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="276b8-119">이 예제에서는 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-119">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="276b8-120">레코드 집합은 A 형식이 고 TTL은 1 시간 (3600 초)입니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="276b8-121">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-121">It contains a single DNS record.</span></span>

### <span data-ttu-id="276b8-122">예제 2: AAAA 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="276b8-122">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="276b8-123">이 예제에서는 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-123">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="276b8-124">레코드 집합은 AAAA 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="276b8-125">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-125">It contains a single DNS record.</span></span>

<span data-ttu-id="276b8-126">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="276b8-126">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="276b8-127">예제 3: CNAME 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="276b8-127">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="276b8-128">이 예제에서는 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-128">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="276b8-129">레코드 집합은 CNAME 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="276b8-130">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-130">It contains a single DNS record.</span></span>

<span data-ttu-id="276b8-131">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="276b8-131">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="276b8-132">예제 4: MX 유형의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="276b8-132">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="276b8-133">이 명령은 zone myzone.com에서 www 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-133">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="276b8-134">레코드 집합은 MX 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="276b8-135">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-135">It contains a single DNS record.</span></span>

<span data-ttu-id="276b8-136">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="276b8-136">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="276b8-137">예제 5: NS 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="276b8-137">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="276b8-138">이 명령은 zone myzone.com에 ns1 이라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-138">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="276b8-139">레코드 집합은 NS 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-139">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="276b8-140">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-140">It contains a single DNS record.</span></span>

<span data-ttu-id="276b8-141">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="276b8-141">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="276b8-142">예제 6: 형식 PTR의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="276b8-142">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="276b8-143">이 명령은 zone 3.2.1.in-in-addr.arpa에 4 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-143">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="276b8-144">레코드 집합은 PTR 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-144">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="276b8-145">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-145">It contains a single DNS record.</span></span>

<span data-ttu-id="276b8-146">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="276b8-146">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="276b8-147">예제 7: SRV 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="276b8-147">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="276b8-148">이 명령은 zone myzone.com에서 _sip 이라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-148">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="276b8-149">레코드 집합은 SRV 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-149">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="276b8-150">IP 주소 2001.2.3.4를 가리키는 단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-150">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="276b8-151">서비스 (sip) 및 프로토콜 (tcp)은 레코드 데이터의 일부가 아닌 레코드 집합 이름의 일부로 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-151">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="276b8-152">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="276b8-152">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="276b8-153">예제 8: TXT 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="276b8-153">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="276b8-154">이 명령은 zone myzone.com에 text 라는 **레코드 집합** 을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-154">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="276b8-155">레코드 집합은 TXT 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-155">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="276b8-156">단일 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-156">It contains a single DNS record.</span></span>

<span data-ttu-id="276b8-157">Pn_PowerShell_short 한 줄만 사용 하 여 **레코드** 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="276b8-157">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="276b8-158">변수</span><span class="sxs-lookup"><span data-stu-id="276b8-158">PARAMETERS</span></span>

### <span data-ttu-id="276b8-159">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="276b8-159">-CaaFlags</span></span>
<span data-ttu-id="276b8-160">추가할 CAA 레코드에 대 한 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-160">The flags for the CAA record to add.</span></span> <span data-ttu-id="276b8-161">0에서 255 사이의 숫자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-161">Must be a number between 0 and 255.</span></span>

```yaml
Type: Byte
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276b8-162">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="276b8-162">-CaaTag</span></span>
<span data-ttu-id="276b8-163">추가할 CAA 레코드의 tag 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-163">The tag field of the CAA record to add.</span></span>

```yaml
Type: String
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276b8-164">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="276b8-164">-CaaValue</span></span>
<span data-ttu-id="276b8-165">추가할 CAA 레코드에 대 한 값 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-165">The value field for the CAA record to add.</span></span>

```yaml
Type: String
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="276b8-166">-Cname</span><span class="sxs-lookup"><span data-stu-id="276b8-166">-Cname</span></span>
<span data-ttu-id="276b8-167">CNAME (정식 이름) 레코드에 대 한 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-167">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="276b8-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="276b8-168">-DefaultProfile</span></span>
<span data-ttu-id="276b8-169">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="276b8-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="276b8-170">-Exchange</span><span class="sxs-lookup"><span data-stu-id="276b8-170">-Exchange</span></span>
<span data-ttu-id="276b8-171">메일 교환 (MX) 레코드의 메일 교환 서버 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-171">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="276b8-172">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="276b8-172">-Ipv4Address</span></span>
<span data-ttu-id="276b8-173">A 레코드에 대 한 IPv4 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-173">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="276b8-174">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="276b8-174">-Ipv6Address</span></span>
<span data-ttu-id="276b8-175">AAAA 레코드에 대 한 IPv6 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-175">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="276b8-176">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="276b8-176">-Nsdname</span></span>
<span data-ttu-id="276b8-177">NS (이름 서버) 레코드에 대 한 이름 서버 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-177">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="276b8-178">-포트</span><span class="sxs-lookup"><span data-stu-id="276b8-178">-Port</span></span>
<span data-ttu-id="276b8-179">서비스 (SRV) 레코드의 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-179">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="276b8-180">-기본 설정</span><span class="sxs-lookup"><span data-stu-id="276b8-180">-Preference</span></span>
<span data-ttu-id="276b8-181">MX 레코드에 대 한 기본 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-181">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="276b8-182">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="276b8-182">-Priority</span></span>
<span data-ttu-id="276b8-183">SRV 레코드에 대 한 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-183">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="276b8-184">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="276b8-184">-Ptrdname</span></span>
<span data-ttu-id="276b8-185">PTR (포인터 리소스) 레코드의 대상 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-185">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="276b8-186">-대상</span><span class="sxs-lookup"><span data-stu-id="276b8-186">-Target</span></span>
<span data-ttu-id="276b8-187">SRV 레코드의 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-187">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="276b8-188">-값</span><span class="sxs-lookup"><span data-stu-id="276b8-188">-Value</span></span>
<span data-ttu-id="276b8-189">TXT 레코드에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-189">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="276b8-190">-중량</span><span class="sxs-lookup"><span data-stu-id="276b8-190">-Weight</span></span>
<span data-ttu-id="276b8-191">SRV 레코드의 가중치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-191">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="276b8-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="276b8-192">CommonParameters</span></span>
<span data-ttu-id="276b8-193">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="276b8-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="276b8-194">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="276b8-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="276b8-195">입력</span><span class="sxs-lookup"><span data-stu-id="276b8-195">INPUTS</span></span>

### <span data-ttu-id="276b8-196">않아야.</span><span class="sxs-lookup"><span data-stu-id="276b8-196">None.</span></span>

## <span data-ttu-id="276b8-197">출력</span><span class="sxs-lookup"><span data-stu-id="276b8-197">OUTPUTS</span></span>

### <span data-ttu-id="276b8-198">Microsoft. Dns. DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="276b8-198">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="276b8-199">상속자</span><span class="sxs-lookup"><span data-stu-id="276b8-199">NOTES</span></span>

## <span data-ttu-id="276b8-200">관련 링크</span><span class="sxs-lookup"><span data-stu-id="276b8-200">RELATED LINKS</span></span>

[<span data-ttu-id="276b8-201">추가-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="276b8-201">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="276b8-202">새로운 AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="276b8-202">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="276b8-203">제거-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="276b8-203">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)
