---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: 1e3362850880f02c648fb3318db226515fc95eef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490848"
---
# <span data-ttu-id="16720-101">Remove-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="16720-101">Remove-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="16720-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16720-102">SYNOPSIS</span></span>
<span data-ttu-id="16720-103">로컬 레코드 집합 개체에서 개인 DNS 레코드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-103">Removes a Private DNS record from a local record set object.</span></span>

## <span data-ttu-id="16720-104">구문</span><span class="sxs-lookup"><span data-stu-id="16720-104">SYNTAX</span></span>

### <span data-ttu-id="16720-105">A(기본값)</span><span class="sxs-lookup"><span data-stu-id="16720-105">A (Default)</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16720-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="16720-106">AAAA</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16720-107">MX</span><span class="sxs-lookup"><span data-stu-id="16720-107">MX</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16720-108">PTR</span><span class="sxs-lookup"><span data-stu-id="16720-108">PTR</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16720-109">TXT</span><span class="sxs-lookup"><span data-stu-id="16720-109">TXT</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16720-110">SRV</span><span class="sxs-lookup"><span data-stu-id="16720-110">SRV</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16720-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="16720-111">CNAME</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16720-112">설명</span><span class="sxs-lookup"><span data-stu-id="16720-112">DESCRIPTION</span></span>
<span data-ttu-id="16720-113">이 Remove-AzPrivateDnsRecordConfig cmdlet은 레코드 집합에서 DNS(개인 도메인 이름 시스템) 레코드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-113">The Remove-AzPrivateDnsRecordConfig cmdlet removes a Private Domain Name System (DNS) record from a record set.</span></span> <span data-ttu-id="16720-114">RecordSet 개체는 오프라인 개체로, Microsoft Azure 개인 DNS 서비스에 대한 변경 내용을 유지하기 위해 Set-AzPrivateDnsRecordSet cmdlet을 실행한 후에만 개인 DNS 응답을 변경하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16720-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="16720-115">레코드를 제거하려면 해당 레코드 형식의 모든 필드가 정확히 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-115">To remove a record, all the fields for that record type must match exactly.</span></span> <span data-ttu-id="16720-116">SOA 레코드를 추가하거나 제거할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="16720-116">You cannot add or remove SOA records.</span></span> <span data-ttu-id="16720-117">SOA 레코드는 사설 DNS 영역이 만들어지면 자동으로 생성되고 사설 DNS 영역이 삭제될 때 자동으로 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="16720-117">SOA records are automatically created when a Private DNS zone is created and automatically deleted when the Private DNS zone is deleted.</span></span> <span data-ttu-id="16720-118">RecordSet 개체를 매개 변수로 또는 파이프라인 연산자를 사용하여 이 cmdlet에 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16720-118">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="16720-119">예제</span><span class="sxs-lookup"><span data-stu-id="16720-119">EXAMPLES</span></span>

### <span data-ttu-id="16720-120">예제 1: 레코드 집합에서 A 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="16720-120">Example 1: Remove an A record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="16720-121">이 예제에서는 기존 레코드 집합에서 A 레코드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-121">This example removes an A record from an existing record set.</span></span> <span data-ttu-id="16720-122">레코드 집합에서 유일한 레코드인 경우 결과는 빈 레코드 집합이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16720-122">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="16720-123">레코드 집합을 완전히 제거하려면 Remove-AzPrivateDnsRecordSet을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-123">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="16720-124">예제 2: 레코드 집합에서 AAAA 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="16720-124">Example 2: Remove an AAAA record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="16720-125">이 예제에서는 기존 레코드 집합에서 AAAA 레코드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-125">This example removes an AAAA record from an existing record set.</span></span> <span data-ttu-id="16720-126">레코드 집합에서 유일한 레코드인 경우 결과는 빈 레코드 집합이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16720-126">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="16720-127">레코드 집합을 완전히 제거하려면 Remove-AzPrivateDnsRecordSet을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-127">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="16720-128">예제 3: 레코드 집합에서 CNAME 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="16720-128">Example 3: Remove a CNAME record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="16720-129">이 예제에서는 기존 레코드 집합에서 CNAME 레코드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-129">This example removes a CNAME record from an existing record set.</span></span> <span data-ttu-id="16720-130">CNAME 레코드 집합은 최대 하나의 레코드를 포함할 수 있기 때문에 결과는 빈 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="16720-130">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="16720-131">예제 4: 레코드 집합에서 MX 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="16720-131">Example 4: Remove a MX record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="16720-132">이 예제에서는 기존 레코드 집합에서 MX 레코드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-132">This example removes an MX record from an existing record set.</span></span> <span data-ttu-id="16720-133">레코드 이름 "@"은 영역 apex에 있는 레코드 집합을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="16720-133">The record name "@" indicates a record set at the zone apex.</span></span> <span data-ttu-id="16720-134">레코드 집합에서 유일한 레코드인 경우 결과는 빈 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="16720-134">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="16720-135">레코드 집합을 완전히 제거하려면 Remove-AzPrivateDnsRecordSet을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-135">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="16720-136">예제 5: 레코드 집합에서 PTR 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="16720-136">Example 5: Remove a PTR record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="16720-137">이 예제에서는 기존 레코드 집합에서 PTR 레코드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-137">This example removes a PTR record from an existing record set.</span></span> <span data-ttu-id="16720-138">레코드 집합에서 유일한 레코드인 경우 결과는 빈 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="16720-138">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="16720-139">레코드 집합을 완전히 제거하려면 Remove-AzPrivateDnsRecordSet을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-139">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="16720-140">예제 6: 레코드 집합에서 SRV 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="16720-140">Example 6: Remove a SRV record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="16720-141">이 예제에서는 기존 레코드 집합에서 SRV 레코드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-141">This example removes an SRV record from an existing record set.</span></span> <span data-ttu-id="16720-142">레코드 집합에서 유일한 레코드인 경우 결과는 빈 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="16720-142">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="16720-143">레코드 집합을 완전히 제거하려면 Remove-AzPrivateDnsRecordSet을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-143">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="16720-144">예제 7: 레코드 집합에서 TXT 레코드 제거</span><span class="sxs-lookup"><span data-stu-id="16720-144">Example 7: Remove a TXT record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Value "This is a TXT Record"  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="16720-145">이 예제에서는 기존 레코드 집합에서 TXT 레코드를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-145">This example removes a TXT record from an existing record set.</span></span> <span data-ttu-id="16720-146">레코드 집합에서 유일한 레코드인 경우 결과는 빈 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="16720-146">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="16720-147">레코드 집합을 완전히 제거하려면 Remove-AzPrivateDnsRecordSet을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-147">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

## <span data-ttu-id="16720-148">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16720-148">PARAMETERS</span></span>

### <span data-ttu-id="16720-149">-Cname</span><span class="sxs-lookup"><span data-stu-id="16720-149">-Cname</span></span>
<span data-ttu-id="16720-150">제거할 CNAME 레코드의 정형 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16720-150">The canonical name of the CNAME record to remove.</span></span>
<span data-ttu-id="16720-151">영역의 이름에 상대적이지 말아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-151">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="16720-152">종료 점이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-152">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="16720-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16720-153">-DefaultProfile</span></span>
<span data-ttu-id="16720-154">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16720-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16720-155">-Exchange</span><span class="sxs-lookup"><span data-stu-id="16720-155">-Exchange</span></span>
<span data-ttu-id="16720-156">제거할 MX 레코드의 메일 교환 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="16720-156">The mail exchange host of the MX record to remove.</span></span>
<span data-ttu-id="16720-157">영역의 이름에 상대적이지 말아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-157">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="16720-158">종료 점이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-158">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="16720-159">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="16720-159">-Ipv4Address</span></span>
<span data-ttu-id="16720-160">제거할 A 레코드의 IPv4 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="16720-160">The IPv4 address of the A record to remove.</span></span>

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

### <span data-ttu-id="16720-161">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="16720-161">-Ipv6Address</span></span>
<span data-ttu-id="16720-162">제거할 AAAA 레코드의 IPv6 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="16720-162">The IPv6 address of the AAAA record to remove.</span></span>

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

### <span data-ttu-id="16720-163">-Port</span><span class="sxs-lookup"><span data-stu-id="16720-163">-Port</span></span>
<span data-ttu-id="16720-164">제거할 SRV 레코드의 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="16720-164">The port number of the SRV record to remove.</span></span>

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

### <span data-ttu-id="16720-165">-Preference</span><span class="sxs-lookup"><span data-stu-id="16720-165">-Preference</span></span>
<span data-ttu-id="16720-166">제거할 MX 레코드의 기본 설정 값입니다.</span><span class="sxs-lookup"><span data-stu-id="16720-166">The preference value of the MX record to remove.</span></span>

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

### <span data-ttu-id="16720-167">-Priority</span><span class="sxs-lookup"><span data-stu-id="16720-167">-Priority</span></span>
<span data-ttu-id="16720-168">제거할 SRV 레코드의 우선 순위 값입니다.</span><span class="sxs-lookup"><span data-stu-id="16720-168">The priority value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="16720-169">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="16720-169">-Ptrdname</span></span>
<span data-ttu-id="16720-170">제거할 PTR 레코드의 대상 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="16720-170">The target host of the PTR record to remove.</span></span>
<span data-ttu-id="16720-171">영역의 이름에 상대적이지 말아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-171">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="16720-172">종료 점이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-172">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="16720-173">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="16720-173">-RecordSet</span></span>
<span data-ttu-id="16720-174">레코드를 제거할 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="16720-174">The record set from which to remove the record.</span></span>

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

### <span data-ttu-id="16720-175">-Target</span><span class="sxs-lookup"><span data-stu-id="16720-175">-Target</span></span>
<span data-ttu-id="16720-176">제거할 SRV 레코드의 대상 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="16720-176">The target host of the SRV record to remove.</span></span>
<span data-ttu-id="16720-177">영역의 이름에 상대적이지 말아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-177">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="16720-178">종료 점이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-178">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="16720-179">-Value</span><span class="sxs-lookup"><span data-stu-id="16720-179">-Value</span></span>
<span data-ttu-id="16720-180">제거할 TXT 레코드의 텍스트 값입니다.</span><span class="sxs-lookup"><span data-stu-id="16720-180">The text value of the TXT record to remove.</span></span>

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

### <span data-ttu-id="16720-181">-Weight</span><span class="sxs-lookup"><span data-stu-id="16720-181">-Weight</span></span>
<span data-ttu-id="16720-182">제거할 SRV 레코드의 가중치 값입니다.</span><span class="sxs-lookup"><span data-stu-id="16720-182">The weight value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="16720-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16720-183">CommonParameters</span></span>
<span data-ttu-id="16720-184">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="16720-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16720-185">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="16720-185">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16720-186">입력</span><span class="sxs-lookup"><span data-stu-id="16720-186">INPUTS</span></span>

### <span data-ttu-id="16720-187">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="16720-187">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="16720-188">출력</span><span class="sxs-lookup"><span data-stu-id="16720-188">OUTPUTS</span></span>

### <span data-ttu-id="16720-189">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="16720-189">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="16720-190">참고 사항</span><span class="sxs-lookup"><span data-stu-id="16720-190">NOTES</span></span>

## <span data-ttu-id="16720-191">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16720-191">RELATED LINKS</span></span>
