---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
ms.openlocfilehash: a0b527a0931c5c3423e5e64bad0abb7128fc3497
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699787"
---
# <span data-ttu-id="9461d-101">Get-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9461d-101">Get-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="9461d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9461d-102">SYNOPSIS</span></span>
<span data-ttu-id="9461d-103">개인 DNS 영역에서 레코드 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9461d-103">Gets a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="9461d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9461d-104">SYNTAX</span></span>

### <span data-ttu-id="9461d-105">FieldsWithNoName (기본값)</span><span class="sxs-lookup"><span data-stu-id="9461d-105">FieldsWithNoName (Default)</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9461d-106">필드인</span><span class="sxs-lookup"><span data-stu-id="9461d-106">Fields</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9461d-107">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="9461d-107">Object</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9461d-108">ObjectWithNoName</span><span class="sxs-lookup"><span data-stu-id="9461d-108">ObjectWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9461d-109">리소스</span><span class="sxs-lookup"><span data-stu-id="9461d-109">ResourceId</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9461d-110">ResourceIdWithNoName</span><span class="sxs-lookup"><span data-stu-id="9461d-110">ResourceIdWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9461d-111">설명은</span><span class="sxs-lookup"><span data-stu-id="9461d-111">DESCRIPTION</span></span>
<span data-ttu-id="9461d-112">Get-AzPrivateDnsRecordSet cmdlet은 지정 된 개인 영역에서 지정한 이름 및 형식으로 DNS (Private Domain Name System) 레코드 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9461d-112">The Get-AzPrivateDnsRecordSet cmdlet gets the Private Domain Name System (DNS) record set with the specified name and type, in the specified private zone.</span></span> <span data-ttu-id="9461d-113">Name 또는 RecordType 매개 변수를 지정 하지 않으면이 cmdlet은 개인 영역에 있는 지정 된 형식의 모든 레코드 집합을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9461d-113">If you do not specify the Name or RecordType parameters, this cmdlet returns all record sets of the specified type in the private zone.</span></span> <span data-ttu-id="9461d-114">Name 매개 변수를 제외한 RecordType 매개 변수를 지정 하면이 cmdlet은 지정 된 레코드 형식의 모든 레코드 집합을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9461d-114">If you specify the RecordType parameter but not the Name parameter, this cmdlet returns all record sets of the specified record type.</span></span> <span data-ttu-id="9461d-115">파이프라인 연산자를 사용 하 여 PSPrivateDnsZone 개체를이 cmdlet에 전달 하거나, PSPrivateDnsZone 개체를 Zone 매개 변수로 전달 하거나, 이름을 기준으로 영역과 리소스 그룹을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9461d-115">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or alternatively you can specify the zone and resource group by name.</span></span> <span data-ttu-id="9461d-116">개인 영역에 대 한 리소스 Id를 사용 하 여 개인 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9461d-116">You can also specify the private zone using the Resource Id of the private zone.</span></span>

## <span data-ttu-id="9461d-117">예제의</span><span class="sxs-lookup"><span data-stu-id="9461d-117">EXAMPLES</span></span>

### <span data-ttu-id="9461d-118">예제 1: 지정 된 이름 및 형식으로 레코드 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="9461d-118">Example 1: Get record sets with a specified name and type</span></span>
```powershell
PS C:\>$RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
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

<span data-ttu-id="9461d-119">이 명령은 지정 된 리소스 그룹 및 개인 영역에 있는 www 라는 레코드 종류의 레코드 집합을 가져온 다음 $RecordSet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9461d-119">This command gets the record set of record type A named www in the specified resource group and private zone, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="9461d-120">Name 및 RecordType 매개 변수는 지정 되어 있으므로 하나의 레코드 집합 개체만 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9461d-120">Because the Name and RecordType parameters are specified, only one RecordSet object is returned.</span></span>

### <span data-ttu-id="9461d-121">예제 2: 지정 된 형식의 레코드 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="9461d-121">Example 2: Get record sets of a specified type</span></span>
```powershell
PS C:\>$RecordSets = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www2
Name              : www2
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {2.3.4.5}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="9461d-122">이 명령은 MyResourceGroup 이라는 리소스 그룹의 myzone.com 이라는 개인 영역에 있는 레코드 종류 A의 모든 레코드 집합의 배열을 가져온 다음이를 $RecordSets 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9461d-122">This command gets an array of all record sets of record type A in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="9461d-123">예제 3: 개인 영역에서 모든 레코드 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="9461d-123">Example 3: Get all record sets in a private zone</span></span>
```powershell
PS C:\>$RecordSets = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="9461d-124">이 명령은 MyResourceGroup 이라는 리소스 그룹의 myzone.com 이라는 개인 영역에 있는 모든 레코드 집합의 배열을 가져온 다음이를 $RecordSets 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9461d-124">This command gets an array of all record sets in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="9461d-125">예제 4: PSPrivateDnsZone 개체를 사용 하 여 개인 영역에서 모든 레코드 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="9461d-125">Example 4: Get all record sets in a private zone, using a PSPrivateDnsZone object</span></span>
```powershell
PS C:\> $Zone = Get-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzPrivateDnsRecordSet -Zone $Zone

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="9461d-126">이 예제는 위의 예제 3과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="9461d-126">This example is equivalent to Example 3 above.</span></span> <span data-ttu-id="9461d-127">이번에는 개인 영역이 전용 영역 개체를 사용 하 여 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9461d-127">This time, the private zone is specified using a private zone object.</span></span>

## <span data-ttu-id="9461d-128">변수</span><span class="sxs-lookup"><span data-stu-id="9461d-128">PARAMETERS</span></span>

### <span data-ttu-id="9461d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9461d-129">-DefaultProfile</span></span>
<span data-ttu-id="9461d-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9461d-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9461d-131">-이름</span><span class="sxs-lookup"><span data-stu-id="9461d-131">-Name</span></span>
<span data-ttu-id="9461d-132">이 레코드 집합의 레코드 이름 (영역의 이름과 종료 점이 없는 위치)을 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="9461d-132">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Object, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9461d-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9461d-133">-ParentResourceId</span></span>
<span data-ttu-id="9461d-134">개인 DNS 영역 ResourceID</span><span class="sxs-lookup"><span data-stu-id="9461d-134">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId, ResourceIdWithNoName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9461d-135">-RecordType</span><span class="sxs-lookup"><span data-stu-id="9461d-135">-RecordType</span></span>
<span data-ttu-id="9461d-136">이 레코드 집합의 DNS 레코드 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="9461d-136">The type of DNS records in this record set.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.PrivateDns.Models.RecordType]
Parameter Sets: FieldsWithNoName, ObjectWithNoName, ResourceIdWithNoName
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.PrivateDns.Models.RecordType]
Parameter Sets: Fields, Object, ResourceId
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9461d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9461d-137">-ResourceGroupName</span></span>
<span data-ttu-id="9461d-138">영역이 속해 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="9461d-138">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: FieldsWithNoName, Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9461d-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="9461d-139">-Zone</span></span>
<span data-ttu-id="9461d-140">레코드 집합을 만들 영역을 나타내는 DnsZone 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9461d-140">The DnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object, ObjectWithNoName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9461d-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="9461d-141">-ZoneName</span></span>
<span data-ttu-id="9461d-142">레코드 집합을 만들 영역으로, 종료 점 없이 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9461d-142">The zone in which to create the record set (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: FieldsWithNoName, Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9461d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9461d-143">CommonParameters</span></span>
<span data-ttu-id="9461d-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9461d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9461d-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9461d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9461d-146">입력</span><span class="sxs-lookup"><span data-stu-id="9461d-146">INPUTS</span></span>

### <span data-ttu-id="9461d-147">PrivateDns. PSPrivateDnsZone/.</span><span class="sxs-lookup"><span data-stu-id="9461d-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="9461d-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9461d-148">System.String</span></span>

## <span data-ttu-id="9461d-149">출력</span><span class="sxs-lookup"><span data-stu-id="9461d-149">OUTPUTS</span></span>

### <span data-ttu-id="9461d-150">PrivateDns. PSPrivateDnsRecordSet/.</span><span class="sxs-lookup"><span data-stu-id="9461d-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="9461d-151">상속자</span><span class="sxs-lookup"><span data-stu-id="9461d-151">NOTES</span></span>

## <span data-ttu-id="9461d-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9461d-152">RELATED LINKS</span></span>
