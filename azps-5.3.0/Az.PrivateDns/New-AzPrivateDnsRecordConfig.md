---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: f828c422447768ff59aea413eeca036a60877b09
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384497"
---
# <span data-ttu-id="dd733-101">New-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="dd733-101">New-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="dd733-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd733-102">SYNOPSIS</span></span>
<span data-ttu-id="dd733-103">새 개인 DNS 레코드 로컬 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-103">Creates a new Private DNS record local object.</span></span>

## <span data-ttu-id="dd733-104">구문</span><span class="sxs-lookup"><span data-stu-id="dd733-104">SYNTAX</span></span>

### <span data-ttu-id="dd733-105">A(기본값)</span><span class="sxs-lookup"><span data-stu-id="dd733-105">A (Default)</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd733-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="dd733-106">AAAA</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd733-107">MX</span><span class="sxs-lookup"><span data-stu-id="dd733-107">MX</span></span>
```
New-AzPrivateDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd733-108">PTR</span><span class="sxs-lookup"><span data-stu-id="dd733-108">PTR</span></span>
```
New-AzPrivateDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd733-109">TXT</span><span class="sxs-lookup"><span data-stu-id="dd733-109">TXT</span></span>
```
New-AzPrivateDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd733-110">SRV</span><span class="sxs-lookup"><span data-stu-id="dd733-110">SRV</span></span>
```
New-AzPrivateDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd733-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="dd733-111">CNAME</span></span>
```
New-AzPrivateDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd733-112">설명</span><span class="sxs-lookup"><span data-stu-id="dd733-112">DESCRIPTION</span></span>
<span data-ttu-id="dd733-113">New-AzPrivateDnsRecordConfig cmdlet은 로컬 PSPrivateDnsRecord 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-113">The New-AzPrivateDnsRecordConfig cmdlet creates a local PSPrivateDnsRecord object.</span></span> <span data-ttu-id="dd733-114">이러한 개체의 배열은 PrivateDnsRecord 매개 변수를 사용하여 New-AzPrivateDnsRecordSet cmdlet에 전달되어 레코드 집합에 만들 레코드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-114">An array of these objects is passed to the New-AzPrivateDnsRecordSet cmdlet using the PrivateDnsRecord parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="dd733-115">예제</span><span class="sxs-lookup"><span data-stu-id="dd733-115">EXAMPLES</span></span>

### <span data-ttu-id="dd733-116">예제 1: A 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="dd733-116">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="dd733-117">이 예제에서는 개인 영역 집합에 www라는 RecordSet을 myzone.com.</span><span class="sxs-lookup"><span data-stu-id="dd733-117">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="dd733-118">레코드 집합은 형식 A로, TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-118">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="dd733-119">단일 개인 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-119">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="dd733-120">예제 2: AAAA 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="dd733-120">Example 2: Create a RecordSet of type AAAA</span></span>
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

<span data-ttu-id="dd733-121">이 예제에서는 개인 영역 집합에 www라는 RecordSet을 myzone.com.</span><span class="sxs-lookup"><span data-stu-id="dd733-121">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="dd733-122">레코드 집합은 AAAA 형식의 TTL(1시간)(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-122">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="dd733-123">단일 개인 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-123">It contains a single Private DNS record.</span></span> <span data-ttu-id="dd733-124">한 줄의 레코드만 사용하여 RecordSet을 만들거나 pn_PowerShell_short 레코드 집합을 만들거나 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-124">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="dd733-125">예제 3: CNAME 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="dd733-125">Example 3: Create a RecordSet of type CNAME</span></span>
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

<span data-ttu-id="dd733-126">이 예제에서는 개인 영역 집합에 www라는 RecordSet을 myzone.com.</span><span class="sxs-lookup"><span data-stu-id="dd733-126">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="dd733-127">레코드 집합은 CNAME 형식이고 TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-127">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="dd733-128">단일 개인 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-128">It contains a single Private DNS record.</span></span> <span data-ttu-id="dd733-129">한 줄의 레코드만 사용하여 RecordSet을 만들거나 pn_PowerShell_short 레코드 집합을 만들거나 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-129">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="dd733-130">예제 4: MX 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="dd733-130">Example 4: Create a RecordSet of type MX</span></span>
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

<span data-ttu-id="dd733-131">이 명령은 개인 영역 집합에 www라는 RecordSet을 myzone.com.</span><span class="sxs-lookup"><span data-stu-id="dd733-131">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="dd733-132">레코드 집합은 MX 형식이고 TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-132">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="dd733-133">단일 개인 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-133">It contains a single Private DNS record.</span></span> <span data-ttu-id="dd733-134">한 줄의 레코드만 사용하여 RecordSet을 만들거나 pn_PowerShell_short 레코드 집합을 만들거나 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-134">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="dd733-135">예제 5: PTR 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="dd733-135">Example 5: Create a RecordSet of type PTR</span></span>
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

<span data-ttu-id="dd733-136">이 명령은 private zone 3.2.1.in-addr.arpa에 4라는 RecordSet을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-136">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="dd733-137">레코드 집합은 PTR 형식으로, TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-137">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="dd733-138">단일 개인 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-138">It contains a single Private DNS record.</span></span> <span data-ttu-id="dd733-139">한 줄의 레코드만 사용하여 RecordSet을 만들거나 pn_PowerShell_short 레코드 집합을 만들거나 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-139">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="dd733-140">예제 6: SRV 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="dd733-140">Example 6: Create a RecordSet of type SRV</span></span>
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

<span data-ttu-id="dd733-141">이 명령은 개인 영역 _sip._tcp라는 RecordSet을 myzone.com.</span><span class="sxs-lookup"><span data-stu-id="dd733-141">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="dd733-142">레코드 집합은 SRV 형식이고 TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-142">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="dd733-143">IP 주소 2001.2.3.4를 지점으로 하는 단일 개인 DNS 레코드가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-143">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="dd733-144">서비스(sip) 및 프로토콜(tcp)은 레코드 데이터의 일부가 아닌 레코드 집합 이름의 일부로 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-144">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="dd733-145">한 줄의 레코드만 사용하여 RecordSet을 만들거나 pn_PowerShell_short 레코드 집합을 만들거나 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-145">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="dd733-146">예제 7: TXT 형식의 RecordSet 만들기</span><span class="sxs-lookup"><span data-stu-id="dd733-146">Example 7: Create a RecordSet of type TXT</span></span>
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

<span data-ttu-id="dd733-147">이 명령은 개인 영역 이름의 레코드 집합을 myzone.com.</span><span class="sxs-lookup"><span data-stu-id="dd733-147">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="dd733-148">레코드 집합은 TXT 형식으로, TTL은 1시간(3600초)입니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-148">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="dd733-149">단일 개인 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-149">It contains a single Private DNS record.</span></span> <span data-ttu-id="dd733-150">한 줄의 레코드만 사용하여 RecordSet을 만들거나 pn_PowerShell_short 레코드 집합을 만들거나 예제 1을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-150">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="dd733-151">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd733-151">PARAMETERS</span></span>

### <span data-ttu-id="dd733-152">-Cname</span><span class="sxs-lookup"><span data-stu-id="dd733-152">-Cname</span></span>
<span data-ttu-id="dd733-153">추가할 CNAME 레코드의 정형 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-153">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="dd733-154">영역의 이름에 상대적이지 말아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-154">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="dd733-155">종료 점이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-155">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="dd733-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd733-156">-DefaultProfile</span></span>
<span data-ttu-id="dd733-157">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd733-158">-Exchange</span><span class="sxs-lookup"><span data-stu-id="dd733-158">-Exchange</span></span>
<span data-ttu-id="dd733-159">추가할 MX 레코드의 메일 교환 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-159">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="dd733-160">영역의 이름에 상대적이지 말아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-160">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="dd733-161">종료 점이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-161">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="dd733-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="dd733-162">-Ipv4Address</span></span>
<span data-ttu-id="dd733-163">추가할 A 레코드의 IPv4 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-163">The IPv4 address for the A record to add.</span></span>

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

### <span data-ttu-id="dd733-164">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="dd733-164">-Ipv6Address</span></span>
<span data-ttu-id="dd733-165">추가할 AAAA 레코드의 IPv6 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-165">The IPv6 address for the AAAA record to add.</span></span>

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

### <span data-ttu-id="dd733-166">-Port</span><span class="sxs-lookup"><span data-stu-id="dd733-166">-Port</span></span>
<span data-ttu-id="dd733-167">추가할 SRV 레코드의 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-167">The port number for the SRV record to add.</span></span>

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

### <span data-ttu-id="dd733-168">-Preference</span><span class="sxs-lookup"><span data-stu-id="dd733-168">-Preference</span></span>
<span data-ttu-id="dd733-169">추가할 MX 레코드의 기본 설정 값입니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-169">The preference value for the MX record to add.</span></span>

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

### <span data-ttu-id="dd733-170">-Priority</span><span class="sxs-lookup"><span data-stu-id="dd733-170">-Priority</span></span>
<span data-ttu-id="dd733-171">추가할 우선 순위 값 SRV 레코드입니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-171">The priority value SRV record to add.</span></span>

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

### <span data-ttu-id="dd733-172">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="dd733-172">-Ptrdname</span></span>
<span data-ttu-id="dd733-173">추가할 PTR 레코드의 대상 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-173">The target host for the PTR record to add.</span></span>
<span data-ttu-id="dd733-174">영역의 이름에 상대적이지 말아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-174">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="dd733-175">종료 점이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-175">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="dd733-176">-Target</span><span class="sxs-lookup"><span data-stu-id="dd733-176">-Target</span></span>
<span data-ttu-id="dd733-177">추가할 SRV 레코드의 대상 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-177">The target host for the SRV record to add.</span></span>
<span data-ttu-id="dd733-178">영역의 이름에 상대적이지 말아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-178">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="dd733-179">종료 점이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-179">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="dd733-180">-Value</span><span class="sxs-lookup"><span data-stu-id="dd733-180">-Value</span></span>
<span data-ttu-id="dd733-181">추가할 TXT 레코드의 텍스트 값입니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-181">The text value for the TXT record to add.</span></span>

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

### <span data-ttu-id="dd733-182">-Weight</span><span class="sxs-lookup"><span data-stu-id="dd733-182">-Weight</span></span>
<span data-ttu-id="dd733-183">추가할 SRV 레코드의 가중치 값입니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-183">The weight value for the SRV record to add.</span></span>

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

### <span data-ttu-id="dd733-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd733-184">CommonParameters</span></span>
<span data-ttu-id="dd733-185">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dd733-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd733-186">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dd733-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd733-187">입력</span><span class="sxs-lookup"><span data-stu-id="dd733-187">INPUTS</span></span>

### <span data-ttu-id="dd733-188">없음</span><span class="sxs-lookup"><span data-stu-id="dd733-188">None</span></span>

## <span data-ttu-id="dd733-189">출력</span><span class="sxs-lookup"><span data-stu-id="dd733-189">OUTPUTS</span></span>

### <span data-ttu-id="dd733-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="dd733-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="dd733-191">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dd733-191">NOTES</span></span>

## <span data-ttu-id="dd733-192">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dd733-192">RELATED LINKS</span></span>
