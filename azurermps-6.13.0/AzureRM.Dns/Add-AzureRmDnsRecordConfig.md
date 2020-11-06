---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/add-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
ms.openlocfilehash: cc1f4186d63b67619734cbfad807d114e2be5463
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532463"
---
# <span data-ttu-id="ecb30-101">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="ecb30-101">Add-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="ecb30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecb30-102">SYNOPSIS</span></span>
<span data-ttu-id="ecb30-103">로컬 레코드 집합 개체에 DNS 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-103">Adds a DNS record to a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecb30-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ecb30-104">SYNTAX</span></span>

### <span data-ttu-id="ecb30-105">에서</span><span class="sxs-lookup"><span data-stu-id="ecb30-105">A</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecb30-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="ecb30-106">AAAA</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecb30-107">NS</span><span class="sxs-lookup"><span data-stu-id="ecb30-107">NS</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecb30-108">멕시코</span><span class="sxs-lookup"><span data-stu-id="ecb30-108">MX</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecb30-109">PTR 레코드로</span><span class="sxs-lookup"><span data-stu-id="ecb30-109">PTR</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecb30-110">라는</span><span class="sxs-lookup"><span data-stu-id="ecb30-110">TXT</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ecb30-111">SRV</span><span class="sxs-lookup"><span data-stu-id="ecb30-111">SRV</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecb30-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="ecb30-112">CNAME</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ecb30-113">Caa</span><span class="sxs-lookup"><span data-stu-id="ecb30-113">Caa</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecb30-114">설명은</span><span class="sxs-lookup"><span data-stu-id="ecb30-114">DESCRIPTION</span></span>
<span data-ttu-id="ecb30-115">**Add-AzureRmDnsRecordConfig** CMDLET은 DNS (Domain Name System) 레코드를 **레코드 집합** 개체에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-115">The **Add-AzureRmDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="ecb30-116">**레코드 집합** 개체는 오프 라인 개체 이며, MICROSOFT Azure DNS 서비스에 대 한 변경 내용을 유지 하기 위해 Set-AzureRmDnsRecordSet cmdlet을 실행 한 후에만 DNS 응답을 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="ecb30-117">SOA 레코드는 DNS 영역을 만들 때 만들어지며 DNS 영역이 삭제 되 면 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="ecb30-118">SOA 레코드를 추가 하거나 제거할 수는 없지만 편집할 수는 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-118">You cannot add or remove SOA records, but you can edit them.</span></span>
<span data-ttu-id="ecb30-119">이 cmdlet에는 **RecordSet** 개체를 매개 변수로 전달 하거나 파이프라인 연산자를 사용 하 여 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="ecb30-120">예제의</span><span class="sxs-lookup"><span data-stu-id="ecb30-120">EXAMPLES</span></span>

### <span data-ttu-id="ecb30-121">예제 1: 레코드 집합에 A 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="ecb30-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="ecb30-122">이 예제에서는 A 레코드를 기존 레코드 집합에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="ecb30-123">예제 2: 레코드 집합에 AAAA 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="ecb30-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="ecb30-124">다음은 기존 레코드 집합에 AAAA 레코드를 추가 하는 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="ecb30-125">예제 3: 레코드 집합에 CNAME 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="ecb30-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="ecb30-126">이 예제에서는 기존 레코드 집합에 CNAME 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="ecb30-127">CNAME 레코드 집합에는 레코드가 하나만 포함 될 수 있으므로, 처음에는 빈 레코드 집합 이거나, Remove-AzureRmDnsRecordConfig를 사용 하 여 기존 레코드를 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzureRmDnsRecordConfig.</span></span>

### <span data-ttu-id="ecb30-128">예제 4: 레코드 집합에 MX 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="ecb30-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="ecb30-129">이 예제에서는 기존 레코드 집합에 MX 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="ecb30-130">레코드 이름 "@"은 (는) apex 영역에서 레코드 집합을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="ecb30-131">예제 5: 레코드 집합에 NS 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="ecb30-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="ecb30-132">이 예제에서는 기존 레코드 집합에 NS 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="ecb30-133">예제 6: 레코드 집합에 PTR 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="ecb30-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="ecb30-134">이 예제에서는 기존 레코드 집합에 PTR 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="ecb30-135">예제 7: 레코드 집합에 SRV 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="ecb30-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="ecb30-136">이 예제에서는 기존 레코드 집합에 SRV 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="ecb30-137">예제 8: 레코드 집합에 TXT 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="ecb30-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Value "This is a TXT Record" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="ecb30-138">이 예제에서는 기존 레코드 집합에 TXT 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="ecb30-139">변수</span><span class="sxs-lookup"><span data-stu-id="ecb30-139">PARAMETERS</span></span>

### <span data-ttu-id="ecb30-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="ecb30-140">-CaaFlags</span></span>
<span data-ttu-id="ecb30-141">추가할 CAA 레코드에 대 한 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="ecb30-142">0에서 255 사이의 숫자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-142">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="ecb30-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="ecb30-143">-CaaTag</span></span>
<span data-ttu-id="ecb30-144">추가할 CAA 레코드의 tag 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-144">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="ecb30-145">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="ecb30-145">-CaaValue</span></span>
<span data-ttu-id="ecb30-146">추가할 CAA 레코드에 대 한 값 필드입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-146">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="ecb30-147">-Cname</span><span class="sxs-lookup"><span data-stu-id="ecb30-147">-Cname</span></span>
<span data-ttu-id="ecb30-148">CNAME (정식 이름) 레코드에 대 한 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="ecb30-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb30-149">-DefaultProfile</span></span>
<span data-ttu-id="ecb30-150">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ecb30-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecb30-151">-Exchange</span><span class="sxs-lookup"><span data-stu-id="ecb30-151">-Exchange</span></span>
<span data-ttu-id="ecb30-152">메일 교환 (MX) 레코드의 메일 교환 서버 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="ecb30-153">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="ecb30-153">-Ipv4Address</span></span>
<span data-ttu-id="ecb30-154">A 레코드에 대 한 IPv4 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-154">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="ecb30-155">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="ecb30-155">-Ipv6Address</span></span>
<span data-ttu-id="ecb30-156">AAAA 레코드에 대 한 IPv6 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-156">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="ecb30-157">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="ecb30-157">-Nsdname</span></span>
<span data-ttu-id="ecb30-158">NS (이름 서버) 레코드에 대 한 이름 서버 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-158">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="ecb30-159">-포트</span><span class="sxs-lookup"><span data-stu-id="ecb30-159">-Port</span></span>
<span data-ttu-id="ecb30-160">서비스 (SRV) 레코드의 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-160">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="ecb30-161">-기본 설정</span><span class="sxs-lookup"><span data-stu-id="ecb30-161">-Preference</span></span>
<span data-ttu-id="ecb30-162">MX 레코드에 대 한 기본 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-162">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="ecb30-163">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="ecb30-163">-Priority</span></span>
<span data-ttu-id="ecb30-164">SRV 레코드에 대 한 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-164">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="ecb30-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="ecb30-165">-Ptrdname</span></span>
<span data-ttu-id="ecb30-166">PTR (포인터 리소스) 레코드의 대상 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="ecb30-167">-레코드 집합</span><span class="sxs-lookup"><span data-stu-id="ecb30-167">-RecordSet</span></span>
<span data-ttu-id="ecb30-168">편집할 **레코드 집합** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-168">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="ecb30-169">-대상</span><span class="sxs-lookup"><span data-stu-id="ecb30-169">-Target</span></span>
<span data-ttu-id="ecb30-170">SRV 레코드의 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-170">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="ecb30-171">-값</span><span class="sxs-lookup"><span data-stu-id="ecb30-171">-Value</span></span>
<span data-ttu-id="ecb30-172">TXT 레코드에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-172">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="ecb30-173">-중량</span><span class="sxs-lookup"><span data-stu-id="ecb30-173">-Weight</span></span>
<span data-ttu-id="ecb30-174">SRV 레코드의 가중치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-174">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="ecb30-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb30-175">CommonParameters</span></span>
<span data-ttu-id="ecb30-176">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb30-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb30-177">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecb30-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb30-178">입력</span><span class="sxs-lookup"><span data-stu-id="ecb30-178">INPUTS</span></span>

### <span data-ttu-id="ecb30-179">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ecb30-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="ecb30-180">매개 변수: 레코드 집합 (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ecb30-180">Parameters: RecordSet (ByValue)</span></span>

### <span data-ttu-id="ecb30-181">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ecb30-181">System.String</span></span>

### <span data-ttu-id="ecb30-182">시스템 UInt16</span><span class="sxs-lookup"><span data-stu-id="ecb30-182">System.UInt16</span></span>

### <span data-ttu-id="ecb30-183">시스템 바이트</span><span class="sxs-lookup"><span data-stu-id="ecb30-183">System.Byte</span></span>

## <span data-ttu-id="ecb30-184">출력</span><span class="sxs-lookup"><span data-stu-id="ecb30-184">OUTPUTS</span></span>

### <span data-ttu-id="ecb30-185">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ecb30-185">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="ecb30-186">상속자</span><span class="sxs-lookup"><span data-stu-id="ecb30-186">NOTES</span></span>

## <span data-ttu-id="ecb30-187">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecb30-187">RELATED LINKS</span></span>

[<span data-ttu-id="ecb30-188">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ecb30-188">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="ecb30-189">제거-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="ecb30-189">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="ecb30-190">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ecb30-190">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
