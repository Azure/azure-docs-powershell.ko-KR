---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/add-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: af3e2e3494aa7f7f98856db3709d4716f5b04e44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699790"
---
# <span data-ttu-id="c7096-101">Add-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="c7096-101">Add-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="c7096-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7096-102">SYNOPSIS</span></span>
<span data-ttu-id="c7096-103">로컬 레코드 집합 개체에 개인 DNS 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-103">Adds a Private DNS record to a local record set object.</span></span>

## <span data-ttu-id="c7096-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c7096-104">SYNTAX</span></span>

### <span data-ttu-id="c7096-105">A (기본값)</span><span class="sxs-lookup"><span data-stu-id="c7096-105">A (Default)</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7096-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="c7096-106">AAAA</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7096-107">멕시코</span><span class="sxs-lookup"><span data-stu-id="c7096-107">MX</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7096-108">PTR 레코드로</span><span class="sxs-lookup"><span data-stu-id="c7096-108">PTR</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7096-109">라는</span><span class="sxs-lookup"><span data-stu-id="c7096-109">TXT</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7096-110">SRV</span><span class="sxs-lookup"><span data-stu-id="c7096-110">SRV</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7096-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="c7096-111">CNAME</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7096-112">설명은</span><span class="sxs-lookup"><span data-stu-id="c7096-112">DESCRIPTION</span></span>
<span data-ttu-id="c7096-113">Add-AzPrivateDnsRecordConfig cmdlet은 개인 DNS (Domain Name System) 레코드를 레코드 집합 개체에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-113">The Add-AzPrivateDnsRecordConfig cmdlet adds a Private Domain Name System (DNS) record to a RecordSet object.</span></span> <span data-ttu-id="c7096-114">레코드 집합 개체는 오프 라인 개체 이며, Microsoft Azure 개인 DNS 서비스에 대 한 변경 내용을 유지 하기 위해 Set-AzPrivateDnsRecordSet cmdlet을 실행 한 후에만 개인 DNS 응답을 변경 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="c7096-115">SOA 레코드는 개인 DNS 영역을 만들 때 만들어지며, 개인 DNS 영역이 삭제 되 면 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-115">SOA records are created when a Private DNS zone is created, and are removed when the Private DNS zone is deleted.</span></span> <span data-ttu-id="c7096-116">SOA 레코드를 추가 하거나 제거할 수는 없지만 편집할 수는 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-116">You cannot add or remove SOA records, but you can edit them.</span></span> <span data-ttu-id="c7096-117">이 cmdlet에는 RecordSet 개체를 매개 변수로 전달 하거나 파이프라인 연산자를 사용 하 여 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-117">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="c7096-118">예제의</span><span class="sxs-lookup"><span data-stu-id="c7096-118">EXAMPLES</span></span>

### <span data-ttu-id="c7096-119">예제 1: 레코드 집합에 A 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="c7096-119">Example 1: Add an A record to a record set</span></span>
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

<span data-ttu-id="c7096-120">이 예제에서는 A 레코드를 기존 레코드 집합에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-120">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="c7096-121">예제 2: 레코드 집합에 AAAA 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="c7096-121">Example 2: Add an AAAA record to a record set</span></span>
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

<span data-ttu-id="c7096-122">이 예제에서는 기존 레코드 집합에 AAAAA 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-122">This example adds an AAAAA record to an existing record set.</span></span>

### <span data-ttu-id="c7096-123">예제 3: 레코드 집합에 CNAME 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="c7096-123">Example 3: Add a CNAME record to a record set</span></span>
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

<span data-ttu-id="c7096-124">이 예제에서는 기존 레코드 집합에 CNAME 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-124">This example adds a CNAME record to an existing record set.</span></span>

### <span data-ttu-id="c7096-125">예제 4: 레코드 집합에 MX 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="c7096-125">Example 4: Add a MX record to a record set</span></span>
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

<span data-ttu-id="c7096-126">이 예제에서는 기존 레코드 집합에 MX 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-126">This example adds a MX record to an existing record set.</span></span>

### <span data-ttu-id="c7096-127">예제 5: 레코드 집합에 PTR 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="c7096-127">Example 5: Add a PTR record to a record set</span></span>
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

<span data-ttu-id="c7096-128">이 예제에서는 기존 레코드 집합에 PTR 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-128">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="c7096-129">예제 6: 레코드 집합에 SRV 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="c7096-129">Example 6: Add a SRV record to a record set</span></span>
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

<span data-ttu-id="c7096-130">이 예제에서는 기존 레코드 집합에 SRV 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-130">This example adds a SRV record to an existing record set.</span></span>

### <span data-ttu-id="c7096-131">예제 7: 레코드 집합에 TXT 레코드 추가</span><span class="sxs-lookup"><span data-stu-id="c7096-131">Example 7: Add a TXT record to a record set</span></span>
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

<span data-ttu-id="c7096-132">이 예제에서는 기존 레코드 집합에 TXT 레코드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-132">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="c7096-133">변수</span><span class="sxs-lookup"><span data-stu-id="c7096-133">PARAMETERS</span></span>

### <span data-ttu-id="c7096-134">-Cname</span><span class="sxs-lookup"><span data-stu-id="c7096-134">-Cname</span></span>
<span data-ttu-id="c7096-135">추가할 CNAME 레코드의 정식 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-135">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="c7096-136">영역 이름을 기준으로 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-136">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="c7096-137">종료 점이 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-137">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="c7096-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7096-138">-DefaultProfile</span></span>
<span data-ttu-id="c7096-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7096-140">-Exchange</span><span class="sxs-lookup"><span data-stu-id="c7096-140">-Exchange</span></span>
<span data-ttu-id="c7096-141">추가할 MX 레코드에 대 한 메일 교환 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-141">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="c7096-142">영역 이름을 기준으로 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-142">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="c7096-143">종료 점이 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-143">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="c7096-144">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="c7096-144">-Ipv4Address</span></span>
<span data-ttu-id="c7096-145">추가할 레코드에 대 한 IPv4 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-145">The IPv4 address for the A record to add.</span></span>

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

### <span data-ttu-id="c7096-146">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="c7096-146">-Ipv6Address</span></span>
<span data-ttu-id="c7096-147">추가할 AAAA 레코드의 IPv6 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-147">The IPv6 address for the AAAA record to add.</span></span>

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

### <span data-ttu-id="c7096-148">-포트</span><span class="sxs-lookup"><span data-stu-id="c7096-148">-Port</span></span>
<span data-ttu-id="c7096-149">추가할 SRV 레코드의 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-149">The port number for the SRV record to add.</span></span>

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

### <span data-ttu-id="c7096-150">-기본 설정</span><span class="sxs-lookup"><span data-stu-id="c7096-150">-Preference</span></span>
<span data-ttu-id="c7096-151">추가할 MX 레코드의 기본 설정 값입니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-151">The preference value for the MX record to add.</span></span>

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

### <span data-ttu-id="c7096-152">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="c7096-152">-Priority</span></span>
<span data-ttu-id="c7096-153">추가할 우선 순위 값 SRV 레코드입니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-153">The priority value SRV record to add.</span></span>

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

### <span data-ttu-id="c7096-154">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="c7096-154">-Ptrdname</span></span>
<span data-ttu-id="c7096-155">추가할 PTR 레코드의 대상 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-155">The target host for the PTR record to add.</span></span>
<span data-ttu-id="c7096-156">영역 이름을 기준으로 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-156">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="c7096-157">종료 점이 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-157">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="c7096-158">-레코드 집합</span><span class="sxs-lookup"><span data-stu-id="c7096-158">-RecordSet</span></span>
<span data-ttu-id="c7096-159">레코드를 추가할 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-159">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="c7096-160">-대상</span><span class="sxs-lookup"><span data-stu-id="c7096-160">-Target</span></span>
<span data-ttu-id="c7096-161">추가할 SRV 레코드의 대상 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-161">The target host for the SRV record to add.</span></span>
<span data-ttu-id="c7096-162">영역 이름을 기준으로 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-162">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="c7096-163">종료 점이 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-163">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="c7096-164">-값</span><span class="sxs-lookup"><span data-stu-id="c7096-164">-Value</span></span>
<span data-ttu-id="c7096-165">추가할 TXT 레코드의 텍스트 값입니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-165">The text value for the TXT record to add.</span></span>

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

### <span data-ttu-id="c7096-166">-중량</span><span class="sxs-lookup"><span data-stu-id="c7096-166">-Weight</span></span>
<span data-ttu-id="c7096-167">추가할 SRV 레코드의 가중치 값입니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-167">The weight value for the SRV record to add.</span></span>

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

### <span data-ttu-id="c7096-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7096-168">CommonParameters</span></span>
<span data-ttu-id="c7096-169">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7096-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7096-170">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7096-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7096-171">입력</span><span class="sxs-lookup"><span data-stu-id="c7096-171">INPUTS</span></span>

### <span data-ttu-id="c7096-172">PrivateDns. PSPrivateDnsRecordSet/.</span><span class="sxs-lookup"><span data-stu-id="c7096-172">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="c7096-173">출력</span><span class="sxs-lookup"><span data-stu-id="c7096-173">OUTPUTS</span></span>

### <span data-ttu-id="c7096-174">PrivateDns. PSPrivateDnsRecordSet/.</span><span class="sxs-lookup"><span data-stu-id="c7096-174">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="c7096-175">상속자</span><span class="sxs-lookup"><span data-stu-id="c7096-175">NOTES</span></span>

## <span data-ttu-id="c7096-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7096-176">RELATED LINKS</span></span>
