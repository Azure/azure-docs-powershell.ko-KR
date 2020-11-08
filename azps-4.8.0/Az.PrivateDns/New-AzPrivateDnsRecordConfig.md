---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: 6653491e7ee4a60b6ad9b392895454e5ee6dc3ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212907"
---
# <span data-ttu-id="9f786-101">New-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="9f786-101">New-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="9f786-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f786-102">SYNOPSIS</span></span>
<span data-ttu-id="9f786-103">새 개인 DNS 레코드 로컬 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-103">Creates a new Private DNS record local object.</span></span>

## <span data-ttu-id="9f786-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9f786-104">SYNTAX</span></span>

### <span data-ttu-id="9f786-105">A (기본값)</span><span class="sxs-lookup"><span data-stu-id="9f786-105">A (Default)</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f786-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="9f786-106">AAAA</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f786-107">멕시코</span><span class="sxs-lookup"><span data-stu-id="9f786-107">MX</span></span>
```
New-AzPrivateDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f786-108">PTR 레코드로</span><span class="sxs-lookup"><span data-stu-id="9f786-108">PTR</span></span>
```
New-AzPrivateDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f786-109">라는</span><span class="sxs-lookup"><span data-stu-id="9f786-109">TXT</span></span>
```
New-AzPrivateDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f786-110">SRV</span><span class="sxs-lookup"><span data-stu-id="9f786-110">SRV</span></span>
```
New-AzPrivateDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f786-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="9f786-111">CNAME</span></span>
```
New-AzPrivateDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f786-112">설명은</span><span class="sxs-lookup"><span data-stu-id="9f786-112">DESCRIPTION</span></span>
<span data-ttu-id="9f786-113">New-AzPrivateDnsRecordConfig cmdlet은 로컬 PSPrivateDnsRecord 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-113">The New-AzPrivateDnsRecordConfig cmdlet creates a local PSPrivateDnsRecord object.</span></span> <span data-ttu-id="9f786-114">이러한 개체의 배열은 PrivateDnsRecord 매개 변수를 사용 하 여 New-AzPrivateDnsRecordSet cmdlet에 전달 되며, 레코드 집합에서 만들 레코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-114">An array of these objects is passed to the New-AzPrivateDnsRecordSet cmdlet using the PrivateDnsRecord parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="9f786-115">예제의</span><span class="sxs-lookup"><span data-stu-id="9f786-115">EXAMPLES</span></span>

### <span data-ttu-id="9f786-116">예제 1: 형식 A의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="9f786-116">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="9f786-117">이 예제에서는 개인 영역 myzone.com에서 www 라는 레코드 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-117">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="9f786-118">레코드 집합은 A 형식이 고 TTL은 1 시간 (3600 초)입니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-118">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="9f786-119">단일 개인 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-119">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="9f786-120">예제 2: AAAA 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="9f786-120">Example 2: Create a RecordSet of type AAAA</span></span>
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

<span data-ttu-id="9f786-121">이 예제에서는 개인 영역 myzone.com에서 www 라는 레코드 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-121">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="9f786-122">레코드 집합은 AAAA 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-122">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="9f786-123">단일 개인 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-123">It contains a single Private DNS record.</span></span> <span data-ttu-id="9f786-124">Pn_PowerShell_short 한 줄만 사용 하 여 레코드 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9f786-124">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9f786-125">예제 3: CNAME 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="9f786-125">Example 3: Create a RecordSet of type CNAME</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="9f786-126">이 예제에서는 개인 영역 myzone.com에서 www 라는 레코드 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-126">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="9f786-127">레코드 집합은 CNAME 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-127">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="9f786-128">단일 개인 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-128">It contains a single Private DNS record.</span></span> <span data-ttu-id="9f786-129">Pn_PowerShell_short 한 줄만 사용 하 여 레코드 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9f786-129">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9f786-130">예제 4: MX 유형의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="9f786-130">Example 4: Create a RecordSet of type MX</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="9f786-131">이 명령은 개인 영역 myzone.com에서 www 라는 레코드 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-131">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="9f786-132">레코드 집합은 MX 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-132">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="9f786-133">단일 개인 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-133">It contains a single Private DNS record.</span></span> <span data-ttu-id="9f786-134">Pn_PowerShell_short 한 줄만 사용 하 여 레코드 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9f786-134">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9f786-135">예제 5: PTR 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="9f786-135">Example 5: Create a RecordSet of type PTR</span></span>
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

<span data-ttu-id="9f786-136">이 명령은 개인 영역 3.2.1.in-in-addr.arpa에 4 라는 레코드 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-136">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="9f786-137">레코드 집합은 PTR 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-137">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="9f786-138">단일 개인 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-138">It contains a single Private DNS record.</span></span> <span data-ttu-id="9f786-139">Pn_PowerShell_short 한 줄만 사용 하 여 레코드 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9f786-139">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9f786-140">예제 6: SRV 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="9f786-140">Example 6: Create a RecordSet of type SRV</span></span>
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

<span data-ttu-id="9f786-141">이 명령은 개인 영역 myzone.com에서 _tcp 이라는 레코드 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-141">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="9f786-142">레코드 집합은 SRV 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-142">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="9f786-143">IP 주소 2001.2.3.4를 가리키는 단일 개인 DNS 레코드가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-143">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="9f786-144">서비스 (sip) 및 프로토콜 (tcp)은 레코드 데이터의 일부가 아닌 레코드 집합 이름의 일부로 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-144">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="9f786-145">Pn_PowerShell_short 한 줄만 사용 하 여 레코드 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9f786-145">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="9f786-146">예제 7: TXT 형식의 레코드 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="9f786-146">Example 7: Create a RecordSet of type TXT</span></span>
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

<span data-ttu-id="9f786-147">이 명령은 개인 영역 myzone.com에 텍스트 라는 레코드 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-147">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="9f786-148">레코드 집합은 TXT 형식이 며 1 시간 (3600 초) TTL을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-148">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="9f786-149">단일 개인 DNS 레코드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-149">It contains a single Private DNS record.</span></span> <span data-ttu-id="9f786-150">Pn_PowerShell_short 한 줄만 사용 하 여 레코드 집합을 만들거나 여러 레코드가 있는 레코드 집합을 만들려면 예제 1을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9f786-150">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="9f786-151">변수</span><span class="sxs-lookup"><span data-stu-id="9f786-151">PARAMETERS</span></span>

### <span data-ttu-id="9f786-152">-Cname</span><span class="sxs-lookup"><span data-stu-id="9f786-152">-Cname</span></span>
<span data-ttu-id="9f786-153">추가할 CNAME 레코드의 정식 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-153">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="9f786-154">영역 이름을 기준으로 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-154">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="9f786-155">종료 점이 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-155">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="9f786-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f786-156">-DefaultProfile</span></span>
<span data-ttu-id="9f786-157">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f786-158">-Exchange</span><span class="sxs-lookup"><span data-stu-id="9f786-158">-Exchange</span></span>
<span data-ttu-id="9f786-159">추가할 MX 레코드에 대 한 메일 교환 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-159">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="9f786-160">영역 이름을 기준으로 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-160">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="9f786-161">종료 점이 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-161">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="9f786-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="9f786-162">-Ipv4Address</span></span>
<span data-ttu-id="9f786-163">추가할 레코드에 대 한 IPv4 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-163">The IPv4 address for the A record to add.</span></span>

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

### <span data-ttu-id="9f786-164">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="9f786-164">-Ipv6Address</span></span>
<span data-ttu-id="9f786-165">추가할 AAAA 레코드의 IPv6 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-165">The IPv6 address for the AAAA record to add.</span></span>

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

### <span data-ttu-id="9f786-166">-포트</span><span class="sxs-lookup"><span data-stu-id="9f786-166">-Port</span></span>
<span data-ttu-id="9f786-167">추가할 SRV 레코드의 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-167">The port number for the SRV record to add.</span></span>

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

### <span data-ttu-id="9f786-168">-기본 설정</span><span class="sxs-lookup"><span data-stu-id="9f786-168">-Preference</span></span>
<span data-ttu-id="9f786-169">추가할 MX 레코드의 기본 설정 값입니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-169">The preference value for the MX record to add.</span></span>

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

### <span data-ttu-id="9f786-170">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="9f786-170">-Priority</span></span>
<span data-ttu-id="9f786-171">추가할 우선 순위 값 SRV 레코드입니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-171">The priority value SRV record to add.</span></span>

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

### <span data-ttu-id="9f786-172">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="9f786-172">-Ptrdname</span></span>
<span data-ttu-id="9f786-173">추가할 PTR 레코드의 대상 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-173">The target host for the PTR record to add.</span></span>
<span data-ttu-id="9f786-174">영역 이름을 기준으로 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-174">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="9f786-175">종료 점이 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-175">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="9f786-176">-대상</span><span class="sxs-lookup"><span data-stu-id="9f786-176">-Target</span></span>
<span data-ttu-id="9f786-177">추가할 SRV 레코드의 대상 호스트입니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-177">The target host for the SRV record to add.</span></span>
<span data-ttu-id="9f786-178">영역 이름을 기준으로 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-178">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="9f786-179">종료 점이 없어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-179">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="9f786-180">-값</span><span class="sxs-lookup"><span data-stu-id="9f786-180">-Value</span></span>
<span data-ttu-id="9f786-181">추가할 TXT 레코드의 텍스트 값입니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-181">The text value for the TXT record to add.</span></span>

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

### <span data-ttu-id="9f786-182">-중량</span><span class="sxs-lookup"><span data-stu-id="9f786-182">-Weight</span></span>
<span data-ttu-id="9f786-183">추가할 SRV 레코드의 가중치 값입니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-183">The weight value for the SRV record to add.</span></span>

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

### <span data-ttu-id="9f786-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f786-184">CommonParameters</span></span>
<span data-ttu-id="9f786-185">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f786-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f786-186">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f786-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f786-187">입력</span><span class="sxs-lookup"><span data-stu-id="9f786-187">INPUTS</span></span>

### <span data-ttu-id="9f786-188">않아야</span><span class="sxs-lookup"><span data-stu-id="9f786-188">None</span></span>

## <span data-ttu-id="9f786-189">출력</span><span class="sxs-lookup"><span data-stu-id="9f786-189">OUTPUTS</span></span>

### <span data-ttu-id="9f786-190">PrivateDns. PSPrivateDnsRecordSet/.</span><span class="sxs-lookup"><span data-stu-id="9f786-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="9f786-191">상속자</span><span class="sxs-lookup"><span data-stu-id="9f786-191">NOTES</span></span>

## <span data-ttu-id="9f786-192">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f786-192">RELATED LINKS</span></span>
