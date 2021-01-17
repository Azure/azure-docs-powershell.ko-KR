---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: c9390514ad7680a047ca145c8fe71feda0ab1b51
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489864"
---
# <span data-ttu-id="b8033-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="b8033-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="b8033-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8033-102">SYNOPSIS</span></span>
<span data-ttu-id="b8033-103">로컬 레코드 집합 개체에 DNS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="b8033-104">구문</span><span class="sxs-lookup"><span data-stu-id="b8033-104">SYNTAX</span></span>

### <span data-ttu-id="b8033-105">A</span><span class="sxs-lookup"><span data-stu-id="b8033-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8033-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="b8033-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8033-107">NS</span><span class="sxs-lookup"><span data-stu-id="b8033-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8033-108">MX</span><span class="sxs-lookup"><span data-stu-id="b8033-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8033-109">PTR</span><span class="sxs-lookup"><span data-stu-id="b8033-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8033-110">TXT</span><span class="sxs-lookup"><span data-stu-id="b8033-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8033-111">SRV</span><span class="sxs-lookup"><span data-stu-id="b8033-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8033-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="b8033-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8033-113">Caa</span><span class="sxs-lookup"><span data-stu-id="b8033-113">Caa</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8033-114">설명</span><span class="sxs-lookup"><span data-stu-id="b8033-114">DESCRIPTION</span></span>
<span data-ttu-id="b8033-115">**Add-AzDnsRecordConfig** cmdlet은 RecordSet 개체에 DNS(도메인 이름 시스템) **레코드를 추가합니다.**</span><span class="sxs-lookup"><span data-stu-id="b8033-115">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="b8033-116">**RecordSet** 개체는 오프라인 개체로, 변경 내용은 Microsoft Azure DNS 서비스에 대한 변경 내용을 유지하기 위해 Set-AzDnsRecordSet cmdlet을 실행한 후에까지 DNS 응답을 변경하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="b8033-117">SOA 레코드는 DNS 영역이 만들어지며 DNS 영역이 삭제될 때 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="b8033-118">SOA 레코드를 추가하거나 제거할 수는 없지만 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-118">You cannot add or remove SOA records, but you can edit them.</span></span>
<span data-ttu-id="b8033-119">RecordSet 개체를  매개 변수로 또는 파이프라인 연산자를 사용하여 이 cmdlet에 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="b8033-120">예제</span><span class="sxs-lookup"><span data-stu-id="b8033-120">EXAMPLES</span></span>

### <span data-ttu-id="b8033-121">예제 1: 레코드 집합에 A 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="b8033-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="b8033-122">이 예제에서는 기존 레코드 집합에 A 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="b8033-123">예제 2: 레코드 집합에 AAAA 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="b8033-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="b8033-124">이 예제에서는 기존 레코드 집합에 AAAA 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="b8033-125">예제 3: 레코드 집합에 CNAME 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="b8033-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="b8033-126">이 예제에서는 기존 레코드 집합에 CNAME 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="b8033-127">CNAME 레코드 집합은 최대 하나의 레코드를 포함할 수 있기 때문에 처음에는 빈 레코드 집합이 되어야 합니다. 또는 Remove-AzDnsRecordConfig를 사용하여 기존 레코드를 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="b8033-128">예제 4: 레코드 집합에 MX 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="b8033-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="b8033-129">이 예제에서는 기존 레코드 집합에 MX 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="b8033-130">레코드 이름 "@"은 영역 apex에 있는 레코드 집합을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="b8033-131">예제 5: 레코드 집합에 NS 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="b8033-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="b8033-132">이 예제에서는 기존 레코드 집합에 NS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="b8033-133">예제 6: 레코드 집합에 PTR 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="b8033-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="b8033-134">이 예제에서는 기존 레코드 집합에 PTR 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="b8033-135">예제 7: 레코드 집합에 SRV 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="b8033-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="b8033-136">이 예제에서는 기존 레코드 집합에 SRV 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="b8033-137">예제 8: 레코드 집합에 TXT 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="b8033-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="b8033-138">이 예제에서는 기존 레코드 집합에 TXT 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="b8033-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8033-139">PARAMETERS</span></span>

### <span data-ttu-id="b8033-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="b8033-140">-CaaFlags</span></span>
<span data-ttu-id="b8033-141">추가할 CAA 레코드에 대한 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="b8033-142">0에서 255 사이의 숫자가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-142">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="b8033-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="b8033-143">-CaaTag</span></span>
<span data-ttu-id="b8033-144">추가할 CAA 레코드의 태그 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-144">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="b8033-145">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="b8033-145">-CaaValue</span></span>
<span data-ttu-id="b8033-146">추가할 CAA 레코드의 값 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-146">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="b8033-147">-Cname</span><span class="sxs-lookup"><span data-stu-id="b8033-147">-Cname</span></span>
<span data-ttu-id="b8033-148">CNAME(정형 이름) 레코드의 도메인 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="b8033-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8033-149">-DefaultProfile</span></span>
<span data-ttu-id="b8033-150">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b8033-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8033-151">-Exchange</span><span class="sxs-lookup"><span data-stu-id="b8033-151">-Exchange</span></span>
<span data-ttu-id="b8033-152">MX(메일 교환) 레코드의 메일 교환 서버 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="b8033-153">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="b8033-153">-Ipv4Address</span></span>
<span data-ttu-id="b8033-154">A 레코드에 대한 IPv4 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-154">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="b8033-155">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="b8033-155">-Ipv6Address</span></span>
<span data-ttu-id="b8033-156">AAAA 레코드에 대한 IPv6 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-156">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="b8033-157">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="b8033-157">-Nsdname</span></span>
<span data-ttu-id="b8033-158">NS(이름 서버) 레코드의 이름 서버 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-158">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="b8033-159">-Port</span><span class="sxs-lookup"><span data-stu-id="b8033-159">-Port</span></span>
<span data-ttu-id="b8033-160">SRV(서비스) 레코드에 대한 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-160">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="b8033-161">-Preference</span><span class="sxs-lookup"><span data-stu-id="b8033-161">-Preference</span></span>
<span data-ttu-id="b8033-162">MX 레코드에 대한 기본 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-162">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="b8033-163">-Priority</span><span class="sxs-lookup"><span data-stu-id="b8033-163">-Priority</span></span>
<span data-ttu-id="b8033-164">SRV 레코드에 대한 우선 순위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-164">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="b8033-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="b8033-165">-Ptrdname</span></span>
<span data-ttu-id="b8033-166">PTR(포인터 리소스) 레코드의 대상 도메인 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="b8033-167">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="b8033-167">-RecordSet</span></span>
<span data-ttu-id="b8033-168">편집할 **RecordSet** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-168">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="b8033-169">-Target</span><span class="sxs-lookup"><span data-stu-id="b8033-169">-Target</span></span>
<span data-ttu-id="b8033-170">SRV 레코드의 대상을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-170">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="b8033-171">-Value</span><span class="sxs-lookup"><span data-stu-id="b8033-171">-Value</span></span>
<span data-ttu-id="b8033-172">TXT 레코드의 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-172">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="b8033-173">-Weight</span><span class="sxs-lookup"><span data-stu-id="b8033-173">-Weight</span></span>
<span data-ttu-id="b8033-174">SRV 레코드의 가중치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-174">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="b8033-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8033-175">CommonParameters</span></span>
<span data-ttu-id="b8033-176">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b8033-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8033-177">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b8033-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8033-178">입력</span><span class="sxs-lookup"><span data-stu-id="b8033-178">INPUTS</span></span>

### <span data-ttu-id="b8033-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b8033-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="b8033-180">System.String</span><span class="sxs-lookup"><span data-stu-id="b8033-180">System.String</span></span>

### <span data-ttu-id="b8033-181">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="b8033-181">System.UInt16</span></span>

### <span data-ttu-id="b8033-182">System.Byte</span><span class="sxs-lookup"><span data-stu-id="b8033-182">System.Byte</span></span>

## <span data-ttu-id="b8033-183">출력</span><span class="sxs-lookup"><span data-stu-id="b8033-183">OUTPUTS</span></span>

### <span data-ttu-id="b8033-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b8033-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="b8033-185">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b8033-185">NOTES</span></span>

## <span data-ttu-id="b8033-186">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8033-186">RELATED LINKS</span></span>

[<span data-ttu-id="b8033-187">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b8033-187">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="b8033-188">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="b8033-188">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="b8033-189">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b8033-189">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
