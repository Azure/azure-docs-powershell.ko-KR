---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/add-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: 63e42c7784fe34d726d6f9cb8db987db877c9248
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996053"
---
# <span data-ttu-id="573cd-101">Add-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="573cd-101">Add-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="573cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="573cd-102">SYNOPSIS</span></span>
<span data-ttu-id="573cd-103">로컬 레코드 집합 개체에 개인 DNS 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-103">Adds a Private DNS record to a local record set object.</span></span>

## <span data-ttu-id="573cd-104">구문</span><span class="sxs-lookup"><span data-stu-id="573cd-104">SYNTAX</span></span>

### <span data-ttu-id="573cd-105">A(기본값)</span><span class="sxs-lookup"><span data-stu-id="573cd-105">A (Default)</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="573cd-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="573cd-106">AAAA</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="573cd-107">MX</span><span class="sxs-lookup"><span data-stu-id="573cd-107">MX</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="573cd-108">PTR</span><span class="sxs-lookup"><span data-stu-id="573cd-108">PTR</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="573cd-109">TXT</span><span class="sxs-lookup"><span data-stu-id="573cd-109">TXT</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="573cd-110">SRV</span><span class="sxs-lookup"><span data-stu-id="573cd-110">SRV</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="573cd-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="573cd-111">CNAME</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="573cd-112">설명</span><span class="sxs-lookup"><span data-stu-id="573cd-112">DESCRIPTION</span></span>
<span data-ttu-id="573cd-113">Add-AzPrivateDnsRecordConfig cmdlet은 RecordSet 개체에 DNS(개인 도메인 이름 시스템) 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-113">The Add-AzPrivateDnsRecordConfig cmdlet adds a Private Domain Name System (DNS) record to a RecordSet object.</span></span> <span data-ttu-id="573cd-114">RecordSet 개체는 오프라인 개체로 변경되어 Microsoft Azure Private DNS 서비스에 대한 변경을 유지하기 위해 Set-AzPrivateDnsRecordSet cmdlet을 실행한 후에까지 개인 DNS 응답을 변경하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="573cd-115">SOA 레코드는 개인 DNS 영역이 만들어지며 개인 DNS 영역이 삭제될 때 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-115">SOA records are created when a Private DNS zone is created, and are removed when the Private DNS zone is deleted.</span></span> <span data-ttu-id="573cd-116">SOA 레코드를 추가하거나 제거할 수는 없지만 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-116">You cannot add or remove SOA records, but you can edit them.</span></span> <span data-ttu-id="573cd-117">RecordSet 개체를 매개 변수로 또는 파이프라인 연산자를 사용하여 이 cmdlet에 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-117">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="573cd-118">예제</span><span class="sxs-lookup"><span data-stu-id="573cd-118">EXAMPLES</span></span>

### <span data-ttu-id="573cd-119">예제 1: 레코드 집합에 A 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="573cd-119">Example 1: Add an A record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="573cd-120">이 예제에서는 기존 레코드 집합에 A 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-120">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="573cd-121">예제 2: 레코드 집합에 AAAA 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="573cd-121">Example 2: Add an AAAA record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="573cd-122">이 예제에서는 기존 레코드 집합에 AAAAA 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-122">This example adds an AAAAA record to an existing record set.</span></span>

### <span data-ttu-id="573cd-123">예제 3: 레코드 집합에 CNAME 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="573cd-123">Example 3: Add a CNAME record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="573cd-124">이 예제에서는 기존 레코드 집합에 CNAME 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-124">This example adds a CNAME record to an existing record set.</span></span>

### <span data-ttu-id="573cd-125">예제 4: 레코드 집합에 MX 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="573cd-125">Example 4: Add a MX record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name @ -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {[5,mail.microsoft.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="573cd-126">이 예제에서는 기존 레코드 집합에 MX 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-126">This example adds a MX record to an existing record set.</span></span>

### <span data-ttu-id="573cd-127">예제 5: 레코드 집합에 PTR 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="573cd-127">Example 5: Add a PTR record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="573cd-128">이 예제에서는 기존 레코드 집합에 PTR 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-128">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="573cd-129">예제 6: 레코드 집합에 SRV 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="573cd-129">Example 6: Add a SRV record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup-ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {[0,5,8080,sipservice.contoso.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="573cd-130">이 예제에서는 기존 레코드 집합에 SRV 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-130">This example adds a SRV record to an existing record set.</span></span>

### <span data-ttu-id="573cd-131">예제 7: 레코드 집합에 TXT 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="573cd-131">Example 7: Add a TXT record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Value "This is a TXT Record" | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {This is a TXT Record}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="573cd-132">이 예제에서는 기존 레코드 집합에 TXT 레코드를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-132">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="573cd-133">매개 변수</span><span class="sxs-lookup"><span data-stu-id="573cd-133">PARAMETERS</span></span>

### <span data-ttu-id="573cd-134">-Cname</span><span class="sxs-lookup"><span data-stu-id="573cd-134">-Cname</span></span>
<span data-ttu-id="573cd-135">추가할 CNAME 레코드의 정형 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-135">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="573cd-136">영역의 이름과 상대적이면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-136">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="573cd-137">종료점이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-137">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573cd-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="573cd-138">-DefaultProfile</span></span>
<span data-ttu-id="573cd-139">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="573cd-140">-Exchange</span><span class="sxs-lookup"><span data-stu-id="573cd-140">-Exchange</span></span>
<span data-ttu-id="573cd-141">추가할 MX 레코드의 메일 교환 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-141">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="573cd-142">영역의 이름과 상대적이면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-142">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="573cd-143">종료점이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-143">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573cd-144">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="573cd-144">-Ipv4Address</span></span>
<span data-ttu-id="573cd-145">추가할 A 레코드의 IPv4 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-145">The IPv4 address for the A record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573cd-146">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="573cd-146">-Ipv6Address</span></span>
<span data-ttu-id="573cd-147">추가할 AAAA 레코드의 IPv6 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-147">The IPv6 address for the AAAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573cd-148">-Port</span><span class="sxs-lookup"><span data-stu-id="573cd-148">-Port</span></span>
<span data-ttu-id="573cd-149">추가할 SRV 레코드의 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-149">The port number for the SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573cd-150">-기본 설정</span><span class="sxs-lookup"><span data-stu-id="573cd-150">-Preference</span></span>
<span data-ttu-id="573cd-151">추가할 MX 레코드의 기본 설정 값입니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-151">The preference value for the MX record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573cd-152">-Priority</span><span class="sxs-lookup"><span data-stu-id="573cd-152">-Priority</span></span>
<span data-ttu-id="573cd-153">추가할 우선 순위 값 SRV 레코드입니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-153">The priority value SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573cd-154">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="573cd-154">-Ptrdname</span></span>
<span data-ttu-id="573cd-155">추가할 PTR 레코드의 대상 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-155">The target host for the PTR record to add.</span></span>
<span data-ttu-id="573cd-156">영역의 이름과 상대적이면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-156">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="573cd-157">종료점이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-157">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573cd-158">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="573cd-158">-RecordSet</span></span>
<span data-ttu-id="573cd-159">레코드를 추가할 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-159">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="573cd-160">-Target</span><span class="sxs-lookup"><span data-stu-id="573cd-160">-Target</span></span>
<span data-ttu-id="573cd-161">추가할 SRV 레코드의 대상 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-161">The target host for the SRV record to add.</span></span>
<span data-ttu-id="573cd-162">영역의 이름과 상대적이면 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-162">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="573cd-163">종료점이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-163">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573cd-164">-Value</span><span class="sxs-lookup"><span data-stu-id="573cd-164">-Value</span></span>
<span data-ttu-id="573cd-165">추가할 TXT 레코드의 텍스트 값입니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-165">The text value for the TXT record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573cd-166">-Weight</span><span class="sxs-lookup"><span data-stu-id="573cd-166">-Weight</span></span>
<span data-ttu-id="573cd-167">추가할 SRV 레코드의 가중치 값입니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-167">The weight value for the SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="573cd-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="573cd-168">CommonParameters</span></span>
<span data-ttu-id="573cd-169">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="573cd-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="573cd-170">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="573cd-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="573cd-171">입력</span><span class="sxs-lookup"><span data-stu-id="573cd-171">INPUTS</span></span>

### <span data-ttu-id="573cd-172">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="573cd-172">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="573cd-173">출력</span><span class="sxs-lookup"><span data-stu-id="573cd-173">OUTPUTS</span></span>

### <span data-ttu-id="573cd-174">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="573cd-174">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="573cd-175">참고 사항</span><span class="sxs-lookup"><span data-stu-id="573cd-175">NOTES</span></span>

## <span data-ttu-id="573cd-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="573cd-176">RELATED LINKS</span></span>
