---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 1a7042c94457f23302aa8d2899475d7b117e65b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358142"
---
# <span data-ttu-id="378e2-101">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="378e2-101">New-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="378e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="378e2-102">SYNOPSIS</span></span>
<span data-ttu-id="378e2-103">사설 DNS 영역의 레코드 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-103">Creates a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="378e2-104">구문</span><span class="sxs-lookup"><span data-stu-id="378e2-104">SYNTAX</span></span>

### <span data-ttu-id="378e2-105">필드(기본값)</span><span class="sxs-lookup"><span data-stu-id="378e2-105">Fields (Default)</span></span>
```
New-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> -Ttl <UInt32> [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="378e2-106">개체</span><span class="sxs-lookup"><span data-stu-id="378e2-106">Object</span></span>
```
New-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="378e2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="378e2-107">ResourceId</span></span>
```
New-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="378e2-108">설명</span><span class="sxs-lookup"><span data-stu-id="378e2-108">DESCRIPTION</span></span>
<span data-ttu-id="378e2-109">New-AzPrivateDnsRecordSet cmdlet은 지정된 이름 및 형식을 사용하여 새 DNS(개인 도메인 이름 시스템) 레코드 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-109">The New-AzPrivateDnsRecordSet cmdlet creates a new Private Domain Name System (DNS) record set with the specified name and type in the specified private zone.</span></span> <span data-ttu-id="378e2-110">RecordSet 개체는 이름과 형식이 같은 개인 DNS 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-110">A RecordSet object is a set of Private DNS records with the same name and type.</span></span> <span data-ttu-id="378e2-111">이 이름은 개인 영역과 상대적이며, 정식 이름이 아니라는 점에 유의합니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-111">Note that the name is relative to the private zone and not the fully qualified name.</span></span> <span data-ttu-id="378e2-112">PrivateDnsRecord 매개 변수는 레코드 집합의 레코드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-112">The PrivateDnsRecord parameter specifies the records in the record set.</span></span> <span data-ttu-id="378e2-113">이 매개 변수는 New-AzPrivateDnsRecordConfig를 사용하여 생성된 개인 DNS 레코드의 배열을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-113">This parameter takes an array of Private DNS records, constructed using New-AzPrivateDnsRecordConfig.</span></span> <span data-ttu-id="378e2-114">파이프라인 연산자를 사용하여 PSPrivateDnsZone 개체를 이 cmdlet에 전달하거나 PSPrivateDnsZone 개체를 영역 매개 변수로 전달하거나 ResourceId에 의해 해당 영역 또는 이름으로 영역 지정을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-114">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or you can specify the zone by its ResourceId, or alternatively you can specify the zone by name.</span></span> <span data-ttu-id="378e2-115">Confirm 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-115">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="378e2-116">일치하는 RecordSet이 이미 있는 경우(동일한 이름 및 레코드 형식) 덮어써서 매개 변수를 지정해야 합니다. 그렇지 않으면 cmdlet에서 새 RecordSet을 만들지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-116">If a matching RecordSet already exists (same name and record type), you must specify the Overwrite parameter, otherwise the cmdlet will not create a new RecordSet .</span></span>

## <span data-ttu-id="378e2-117">예제</span><span class="sxs-lookup"><span data-stu-id="378e2-117">EXAMPLES</span></span>

### <span data-ttu-id="378e2-118">예제 1: A 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="378e2-118">Example 1: Create a RecordSet of type A</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4)

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :


# To create a record set containing multiple records, use New-AzPrivateDnsRecordConfig to add each record to the $Records array,
# then call New-AzPrivateDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 5.6.7.8}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="378e2-119">이 예제에서는 개인 영역 집합에 www라는 RecordSet을 myzone.com.</span><span class="sxs-lookup"><span data-stu-id="378e2-119">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="378e2-120">레코드 집합은 형식 A로, TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="378e2-121">단일 개인 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-121">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="378e2-122">예제 2: AAAA 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="378e2-122">Example 2: Create a RecordSet of type AAAA</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:db8::1}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="378e2-123">이 예제에서는 개인 영역 집합에 www라는 RecordSet을 myzone.com.</span><span class="sxs-lookup"><span data-stu-id="378e2-123">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="378e2-124">레코드 집합은 AAAA 형식의 TTL(1시간)(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="378e2-125">단일 개인 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-125">It contains a single Private DNS record.</span></span> <span data-ttu-id="378e2-126">한 줄의 레코드만 사용하여 RecordSet을 만들거나 pn_PowerShell_short 레코드 집합을 만들거나 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-126">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="378e2-127">예제 3: CNAME 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="378e2-127">Example 3: Create a RecordSet of type CNAME</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="378e2-128">이 예제에서는 개인 영역 집합에 www라는 RecordSet을 myzone.com.</span><span class="sxs-lookup"><span data-stu-id="378e2-128">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="378e2-129">레코드 집합은 CNAME 형식이고 TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="378e2-130">단일 개인 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-130">It contains a single Private DNS record.</span></span> <span data-ttu-id="378e2-131">한 줄의 레코드만 사용하여 RecordSet을 만들거나 pn_PowerShell_short 레코드 집합을 만들거나 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-131">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="378e2-132">예제 4: MX 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="378e2-132">Example 4: Create a RecordSet of type MX</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="378e2-133">이 명령은 개인 영역 집합에 www라는 RecordSet을 myzone.com.</span><span class="sxs-lookup"><span data-stu-id="378e2-133">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="378e2-134">레코드 집합은 MX 형식이고 TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="378e2-135">단일 개인 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-135">It contains a single Private DNS record.</span></span> <span data-ttu-id="378e2-136">한 줄의 레코드만 사용하여 RecordSet을 만들거나 pn_PowerShell_short 레코드 집합을 만들거나 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-136">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="378e2-137">예제 5: PTR 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="378e2-137">Example 5: Create a RecordSet of type PTR</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -PrivateDnsRecords $Records

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

<span data-ttu-id="378e2-138">이 명령은 private zone 3.2.1.in-addr.arpa에 4라는 RecordSet을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-138">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="378e2-139">레코드 집합은 PTR 형식으로, TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-139">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="378e2-140">단일 개인 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-140">It contains a single Private DNS record.</span></span> <span data-ttu-id="378e2-141">한 줄의 레코드만 사용하여 RecordSet을 만들거나 pn_PowerShell_short 레코드 집합을 만들거나 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-141">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="378e2-142">예제 6: SRV 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="378e2-142">Example 6: Create a RecordSet of type SRV</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="378e2-143">이 명령은 개인 영역 _sip._tcp라는 RecordSet을 myzone.com.</span><span class="sxs-lookup"><span data-stu-id="378e2-143">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="378e2-144">레코드 집합은 SRV 형식이고 TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-144">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="378e2-145">IP 주소 2001.2.3.4를 지점으로 하는 단일 개인 DNS 레코드가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-145">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="378e2-146">서비스(sip) 및 프로토콜(tcp)은 레코드 데이터의 일부가 아닌 레코드 집합 이름의 일부로 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-146">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="378e2-147">한 줄의 레코드만 사용하여 RecordSet을 만들거나 pn_PowerShell_short 레코드 집합을 만들거나 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-147">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="378e2-148">예제 7: TXT 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="378e2-148">Example 7: Create a RecordSet of type TXT</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="378e2-149">이 명령은 개인 영역 이름의 레코드 집합을 myzone.com.</span><span class="sxs-lookup"><span data-stu-id="378e2-149">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="378e2-150">레코드 집합은 TXT 형식으로, TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-150">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="378e2-151">단일 개인 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-151">It contains a single Private DNS record.</span></span> <span data-ttu-id="378e2-152">한 줄의 레코드만 사용하여 RecordSet을 만들거나 pn_PowerShell_short 레코드 집합을 만들거나 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-152">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="378e2-153">예제 8: 영역 apex에서 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="378e2-153">Example 8:  Create a RecordSet at the zone apex</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="378e2-154">이 명령은 개인 영역의 루트 또는 루트에 RecordSet을 myzone.com.</span><span class="sxs-lookup"><span data-stu-id="378e2-154">This command creates a RecordSet at the apex (or root) of the private zone myzone.com.</span></span> <span data-ttu-id="378e2-155">이를 위해 레코드 집합 이름은 "@"(따옴표 포함)로 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-155">To do this, the record set name is specified as "@" (including the double-quotes).</span></span> <span data-ttu-id="378e2-156">영역의 apex에서 CNAME 레코드를 만들 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-156">You cannot create CNAME records at the apex of a zone.</span></span> <span data-ttu-id="378e2-157">DNS 표준의 제약 조건입니다. Azure 사설 DNS의 제한 사항이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-157">This is a constraint of the DNS standards; it is not a limitation of Azure Private DNS.</span></span> <span data-ttu-id="378e2-158">한 줄의 레코드만 사용하여 RecordSet을 만들거나 pn_PowerShell_short 레코드 집합을 만들거나 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-158">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="378e2-159">예제 9: 와일드카드 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="378e2-159">Example 9:  Create a wildcard Record Set</span></span>

```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="378e2-160">이 명령은 개인 영역 집합에 \*라는 RecordSet을 myzone.com.</span><span class="sxs-lookup"><span data-stu-id="378e2-160">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="378e2-161">와일드카드 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-161">This is a wildcard record set.</span></span> <span data-ttu-id="378e2-162">한 줄의 레코드만 사용하여 RecordSet을 만들거나 pn_PowerShell_short 레코드 집합을 만들거나 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-162">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="378e2-163">예제 10: 빈 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="378e2-163">Example 10:  Create an empty Record Set</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords @()

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="378e2-164">이 명령은 개인 영역 집합에 \*라는 RecordSet을 myzone.com.</span><span class="sxs-lookup"><span data-stu-id="378e2-164">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="378e2-165">레코드 집합은 형식 A로, TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-165">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="378e2-166">빈 레코드 집합으로, 나중에 레코드를 추가할 수 있는 자리 홀더 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-166">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="378e2-167">예제 11: 레코드 집합 만들기 및 모든 확인 표시 안</span><span class="sxs-lookup"><span data-stu-id="378e2-167">Example 11:  Create a record set and suppress all confirmation</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="378e2-168">이 명령은 RecordSet을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-168">This command creates a RecordSet.</span></span> <span data-ttu-id="378e2-169">덮어덮어 사용 매개 변수는 이 레코드 집합이 이름과 형식이 같은 기존 레코드 집합을 덮어들이게 합니다(해당 레코드 집합의 기존 레코드가 손실).</span><span class="sxs-lookup"><span data-stu-id="378e2-169">The Overwrite parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span> <span data-ttu-id="378e2-170">값이 $False Confirm 매개 변수는 확인 프롬프트를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-170">The Confirm parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="378e2-171">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="378e2-171">PARAMETERS</span></span>

### <span data-ttu-id="378e2-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="378e2-172">-DefaultProfile</span></span>
<span data-ttu-id="378e2-173">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="378e2-174">-Metadata</span><span class="sxs-lookup"><span data-stu-id="378e2-174">-Metadata</span></span>
<span data-ttu-id="378e2-175">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-175">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e2-176">-Name</span><span class="sxs-lookup"><span data-stu-id="378e2-176">-Name</span></span>
<span data-ttu-id="378e2-177">이 레코드 집합의 레코드 이름입니다(영역 이름과 종료 점이 없는 상대적).</span><span class="sxs-lookup"><span data-stu-id="378e2-177">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e2-178">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="378e2-178">-Overwrite</span></span>
<span data-ttu-id="378e2-179">레코드 집합이 이미 있는 경우 실패하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-179">Do not fail if the record set already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e2-180">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="378e2-180">-ParentResourceId</span></span>
<span data-ttu-id="378e2-181">사설 DNS 영역 ResourceID.</span><span class="sxs-lookup"><span data-stu-id="378e2-181">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="378e2-182">-PrivateDnsRecord</span><span class="sxs-lookup"><span data-stu-id="378e2-182">-PrivateDnsRecord</span></span>
<span data-ttu-id="378e2-183">이 레코드 집합의 일부인 개인 DNS 레코드입니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-183">The private dns records that are part of this record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordBase[]
Parameter Sets: (All)
Aliases: PrivateDnsRecords

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e2-184">-RecordType</span><span class="sxs-lookup"><span data-stu-id="378e2-184">-RecordType</span></span>
<span data-ttu-id="378e2-185">이 레코드 집합의 개인 DNS 레코드 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-185">The type of Private DNS records in this record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e2-186">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="378e2-186">-ResourceGroupName</span></span>
<span data-ttu-id="378e2-187">영역이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-187">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e2-188">-Ttl</span><span class="sxs-lookup"><span data-stu-id="378e2-188">-Ttl</span></span>
<span data-ttu-id="378e2-189">이 레코드 집합에 있는 모든 레코드의 TTL 값입니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-189">The TTL value of all the records in this record set.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e2-190">-Zone</span><span class="sxs-lookup"><span data-stu-id="378e2-190">-Zone</span></span>
<span data-ttu-id="378e2-191">레코드 집합을 만들 영역의 PrivateDnsZone 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-191">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="378e2-192">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="378e2-192">-ZoneName</span></span>
<span data-ttu-id="378e2-193">레코드 집합을 만들 영역입니다(종료점 없이).</span><span class="sxs-lookup"><span data-stu-id="378e2-193">The zone in which to create the record set (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e2-194">-Confirm</span><span class="sxs-lookup"><span data-stu-id="378e2-194">-Confirm</span></span>
<span data-ttu-id="378e2-195">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-195">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e2-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="378e2-196">-WhatIf</span></span>
<span data-ttu-id="378e2-197">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="378e2-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="378e2-198">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-198">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378e2-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="378e2-199">CommonParameters</span></span>
<span data-ttu-id="378e2-200">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="378e2-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="378e2-201">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="378e2-201">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="378e2-202">입력</span><span class="sxs-lookup"><span data-stu-id="378e2-202">INPUTS</span></span>

### <span data-ttu-id="378e2-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="378e2-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="378e2-204">System.String</span><span class="sxs-lookup"><span data-stu-id="378e2-204">System.String</span></span>

## <span data-ttu-id="378e2-205">출력</span><span class="sxs-lookup"><span data-stu-id="378e2-205">OUTPUTS</span></span>

### <span data-ttu-id="378e2-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="378e2-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="378e2-207">참고 사항</span><span class="sxs-lookup"><span data-stu-id="378e2-207">NOTES</span></span>

## <span data-ttu-id="378e2-208">관련 링크</span><span class="sxs-lookup"><span data-stu-id="378e2-208">RELATED LINKS</span></span>