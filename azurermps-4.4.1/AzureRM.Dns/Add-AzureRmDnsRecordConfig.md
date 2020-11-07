---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
ms.openlocfilehash: 65ab77c7ad94224e3ab2c72072834c43ef1434a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704068"
---
# <span data-ttu-id="36f6b-101">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="36f6b-101">Add-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="36f6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36f6b-102">SYNOPSIS</span></span>
<span data-ttu-id="36f6b-103">로컬 레코드 집합 개체에 DNS 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-103">Adds a DNS record to a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36f6b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="36f6b-104">SYNTAX</span></span>

### <span data-ttu-id="36f6b-105">에서</span><span class="sxs-lookup"><span data-stu-id="36f6b-105">A</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36f6b-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="36f6b-106">AAAA</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36f6b-107">NS</span><span class="sxs-lookup"><span data-stu-id="36f6b-107">NS</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36f6b-108">멕시코</span><span class="sxs-lookup"><span data-stu-id="36f6b-108">MX</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36f6b-109">PTR 레코드로</span><span class="sxs-lookup"><span data-stu-id="36f6b-109">PTR</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36f6b-110">라는</span><span class="sxs-lookup"><span data-stu-id="36f6b-110">TXT</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36f6b-111">SRV</span><span class="sxs-lookup"><span data-stu-id="36f6b-111">SRV</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36f6b-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="36f6b-112">CNAME</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36f6b-113">설명은</span><span class="sxs-lookup"><span data-stu-id="36f6b-113">DESCRIPTION</span></span>
<span data-ttu-id="36f6b-114">**Add-AzureRmDnsRecordConfig** CMDLET은 DNS (Domain Name System) 레코드를 **레코드 집합** 개체에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-114">The **Add-AzureRmDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="36f6b-115">**레코드 집합** 개체는 오프 라인 개체 이며, MICROSOFT Azure DNS 서비스에 대 한 변경 내용을 유지 하기 위해 Set-AzureRmDnsRecordSet cmdlet을 실행 한 후에만 DNS 응답을 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="36f6b-116">SOA 레코드는 DNS 영역을 만들 때 만들어지며 DNS 영역이 삭제 되 면 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-116">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="36f6b-117">SOA 레코드를 추가 하거나 제거할 수는 없지만 편집할 수는 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-117">You cannot add or remove SOA records, but you can edit them.</span></span>

<span data-ttu-id="36f6b-118">이 cmdlet에는 **RecordSet** 개체를 매개 변수로 전달 하거나 파이프라인 연산자를 사용 하 여 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-118">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="36f6b-119">예제의</span><span class="sxs-lookup"><span data-stu-id="36f6b-119">EXAMPLES</span></span>

### <span data-ttu-id="36f6b-120">예제 1: 레코드 집합에 A 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="36f6b-120">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="36f6b-121">이 예제에서는 A 레코드를 기존 레코드 집합에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-121">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="36f6b-122">예제 2: 레코드 집합에 AAAA 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="36f6b-122">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="36f6b-123">다음은 기존 레코드 집합에 AAAA 레코드를 추가 하는 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-123">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="36f6b-124">예제 3: 레코드 집합에 CNAME 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="36f6b-124">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="36f6b-125">이 예제에서는 기존 레코드 집합에 CNAME 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-125">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="36f6b-126">CNAME 레코드 집합에는 레코드가 하나만 포함 될 수 있으므로, 처음에는 빈 레코드 집합 이거나, Remove-AzureRmDnsRecordConfig를 사용 하 여 기존 레코드를 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-126">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzureRmDnsRecordConfig.</span></span>

### <span data-ttu-id="36f6b-127">예제 4: 레코드 집합에 MX 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="36f6b-127">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="36f6b-128">이 예제에서는 기존 레코드 집합에 MX 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-128">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="36f6b-129">레코드 이름 "@"은 (는) apex 영역에서 레코드 집합을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-129">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="36f6b-130">예제 5: 레코드 집합에 NS 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="36f6b-130">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="36f6b-131">이 예제에서는 기존 레코드 집합에 NS 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-131">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="36f6b-132">예제 6: 레코드 집합에 PTR 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="36f6b-132">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="36f6b-133">이 예제에서는 기존 레코드 집합에 PTR 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-133">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="36f6b-134">예제 7: 레코드 집합에 SRV 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="36f6b-134">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="36f6b-135">이 예제에서는 기존 레코드 집합에 SRV 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-135">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="36f6b-136">예제 8: 레코드 집합에 TXT 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="36f6b-136">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Value "This is a TXT Record" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="36f6b-137">이 예제에서는 기존 레코드 집합에 TXT 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-137">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="36f6b-138">변수</span><span class="sxs-lookup"><span data-stu-id="36f6b-138">PARAMETERS</span></span>

### <span data-ttu-id="36f6b-139">-Cname</span><span class="sxs-lookup"><span data-stu-id="36f6b-139">-Cname</span></span>
<span data-ttu-id="36f6b-140">CNAME (정식 이름) 레코드에 대 한 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-140">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="36f6b-141">-Exchange</span><span class="sxs-lookup"><span data-stu-id="36f6b-141">-Exchange</span></span>
<span data-ttu-id="36f6b-142">메일 교환 (MX) 레코드의 메일 교환 서버 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-142">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="36f6b-143">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="36f6b-143">-Ipv4Address</span></span>
<span data-ttu-id="36f6b-144">A 레코드에 대 한 IPv4 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-144">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="36f6b-145">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="36f6b-145">-Ipv6Address</span></span>
<span data-ttu-id="36f6b-146">AAAA 레코드에 대 한 IPv6 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-146">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="36f6b-147">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="36f6b-147">-Nsdname</span></span>
<span data-ttu-id="36f6b-148">NS (이름 서버) 레코드에 대 한 이름 서버 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-148">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="36f6b-149">-포트</span><span class="sxs-lookup"><span data-stu-id="36f6b-149">-Port</span></span>
<span data-ttu-id="36f6b-150">서비스 (SRV) 레코드의 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-150">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="36f6b-151">-기본 설정</span><span class="sxs-lookup"><span data-stu-id="36f6b-151">-Preference</span></span>
<span data-ttu-id="36f6b-152">MX 레코드에 대 한 기본 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-152">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="36f6b-153">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="36f6b-153">-Priority</span></span>
<span data-ttu-id="36f6b-154">SRV 레코드에 대 한 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-154">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="36f6b-155">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="36f6b-155">-Ptrdname</span></span>
<span data-ttu-id="36f6b-156">PTR (포인터 리소스) 레코드의 대상 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-156">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="36f6b-157">-레코드 집합</span><span class="sxs-lookup"><span data-stu-id="36f6b-157">-RecordSet</span></span>
<span data-ttu-id="36f6b-158">편집할 **레코드 집합** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-158">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="36f6b-159">-대상</span><span class="sxs-lookup"><span data-stu-id="36f6b-159">-Target</span></span>
<span data-ttu-id="36f6b-160">SRV 레코드의 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-160">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="36f6b-161">-값</span><span class="sxs-lookup"><span data-stu-id="36f6b-161">-Value</span></span>
<span data-ttu-id="36f6b-162">TXT 레코드에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-162">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="36f6b-163">-중량</span><span class="sxs-lookup"><span data-stu-id="36f6b-163">-Weight</span></span>
<span data-ttu-id="36f6b-164">SRV 레코드의 가중치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-164">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="36f6b-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f6b-165">-DefaultProfile</span></span>
<span data-ttu-id="36f6b-166">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36f6b-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f6b-167">CommonParameters</span></span>
<span data-ttu-id="36f6b-168">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36f6b-169">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36f6b-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f6b-170">입력</span><span class="sxs-lookup"><span data-stu-id="36f6b-170">INPUTS</span></span>

### <span data-ttu-id="36f6b-171">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="36f6b-171">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="36f6b-172">**RecordSet** 개체를이 cmdlet에 파이프 하 여 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-172">You can pipe a **RecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="36f6b-173">이는 **레코드 집합** 의 오프 라인 표현이 며, Set-AzureRmDnsRecordSet cmdlet을 실행할 때까지 변경 내용이 DNS 응답을 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-173">This is an offline representation of the **RecordSet** , and changes to it do not change DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet.</span></span>

## <span data-ttu-id="36f6b-174">출력</span><span class="sxs-lookup"><span data-stu-id="36f6b-174">OUTPUTS</span></span>

### <span data-ttu-id="36f6b-175">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="36f6b-175">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="36f6b-176">이 cmdlet은 수정 된 **레코드 집합** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-176">This cmdlet returns the modified **RecordSet** object.</span></span>
<span data-ttu-id="36f6b-177">또한 전달 된 개체는 직접 수정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36f6b-177">In addition, the object passed in is modified directly.</span></span>

## <span data-ttu-id="36f6b-178">상속자</span><span class="sxs-lookup"><span data-stu-id="36f6b-178">NOTES</span></span>

## <span data-ttu-id="36f6b-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36f6b-179">RELATED LINKS</span></span>

[<span data-ttu-id="36f6b-180">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="36f6b-180">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="36f6b-181">제거-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="36f6b-181">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="36f6b-182">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="36f6b-182">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
