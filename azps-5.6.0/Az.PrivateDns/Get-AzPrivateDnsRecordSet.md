---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/get-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 7ddc6b9621bbf156b386a0f67337edcc32e0363c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014971"
---
# <span data-ttu-id="ca730-101">Get-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ca730-101">Get-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="ca730-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca730-102">SYNOPSIS</span></span>
<span data-ttu-id="ca730-103">개인 DNS 영역에서 레코드 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-103">Gets a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="ca730-104">구문</span><span class="sxs-lookup"><span data-stu-id="ca730-104">SYNTAX</span></span>

### <span data-ttu-id="ca730-105">FieldsWithNoName(기본값)</span><span class="sxs-lookup"><span data-stu-id="ca730-105">FieldsWithNoName (Default)</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca730-106">필드</span><span class="sxs-lookup"><span data-stu-id="ca730-106">Fields</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca730-107">개체</span><span class="sxs-lookup"><span data-stu-id="ca730-107">Object</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca730-108">ObjectWithNoName</span><span class="sxs-lookup"><span data-stu-id="ca730-108">ObjectWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca730-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca730-109">ResourceId</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca730-110">ResourceIdWithNoName</span><span class="sxs-lookup"><span data-stu-id="ca730-110">ResourceIdWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca730-111">설명</span><span class="sxs-lookup"><span data-stu-id="ca730-111">DESCRIPTION</span></span>
<span data-ttu-id="ca730-112">Get-AzPrivateDnsRecordSet cmdlet은 지정된 이름과 형식이 지정된 개인 영역의 DNS(개인 도메인 이름 시스템) 레코드 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-112">The Get-AzPrivateDnsRecordSet cmdlet gets the Private Domain Name System (DNS) record set with the specified name and type, in the specified private zone.</span></span> <span data-ttu-id="ca730-113">Name 또는 RecordType 매개 변수를 지정하지 않으면 이 cmdlet은 개인 영역의 지정된 형식의 모든 레코드 집합을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-113">If you do not specify the Name or RecordType parameters, this cmdlet returns all record sets of the specified type in the private zone.</span></span> <span data-ttu-id="ca730-114">RecordType 매개 변수를 지정하지만 이름 매개 변수가 아닌 경우 이 cmdlet은 지정된 레코드 형식의 모든 레코드 집합을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-114">If you specify the RecordType parameter but not the Name parameter, this cmdlet returns all record sets of the specified record type.</span></span> <span data-ttu-id="ca730-115">파이프라인 연산자를 사용하여 PSPrivateDnsZone 개체를 이 cmdlet에 전달하거나 PSPrivateDnsZone 개체를 영역 매개 변수로 전달하거나 또는 이름으로 영역 및 리소스 그룹을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-115">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or alternatively you can specify the zone and resource group by name.</span></span> <span data-ttu-id="ca730-116">개인 영역의 리소스 ID를 사용하여 개인 영역도 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-116">You can also specify the private zone using the Resource Id of the private zone.</span></span>

## <span data-ttu-id="ca730-117">예제</span><span class="sxs-lookup"><span data-stu-id="ca730-117">EXAMPLES</span></span>

### <span data-ttu-id="ca730-118">예제 1: 지정된 이름 및 형식이 있는 레코드 집합을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-118">Example 1: Get record sets with a specified name and type</span></span>
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

<span data-ttu-id="ca730-119">이 명령은 지정된 리소스 그룹 및 개인 영역의 www라는 레코드 형식 A의 레코드 집합을 구한 다음, $RecordSet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-119">This command gets the record set of record type A named www in the specified resource group and private zone, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="ca730-120">Name 및 RecordType 매개 변수가 지정되어 있기 때문에 RecordSet 개체 하나만 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-120">Because the Name and RecordType parameters are specified, only one RecordSet object is returned.</span></span>

### <span data-ttu-id="ca730-121">예제 2: 지정된 형식의 레코드 집합을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-121">Example 2: Get record sets of a specified type</span></span>
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

<span data-ttu-id="ca730-122">이 명령은 MyResourceGroup이라는 리소스 그룹에 myzone.com 라는 개인 영역의 모든 레코드 형식 A 레코드 집합의 배열을 얻은 다음, 해당 레코드 $RecordSets 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-122">This command gets an array of all record sets of record type A in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="ca730-123">예제 3: 개인 영역의 모든 레코드 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-123">Example 3: Get all record sets in a private zone</span></span>
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

<span data-ttu-id="ca730-124">이 명령은 MyResourceGroup이라는 리소스 그룹에 myzone.com 라는 개인 영역의 모든 레코드 집합의 배열을 구한 다음, 해당 레코드 집합을 $RecordSets 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-124">This command gets an array of all record sets in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="ca730-125">예제 4: PSPrivateDnsZone 개체를 사용하여 개인 영역의 모든 레코드 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-125">Example 4: Get all record sets in a private zone, using a PSPrivateDnsZone object</span></span>
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

<span data-ttu-id="ca730-126">이 예제는 위의 예제 3과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-126">This example is equivalent to Example 3 above.</span></span> <span data-ttu-id="ca730-127">이번에는 개인 영역 개체를 사용하여 개인 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-127">This time, the private zone is specified using a private zone object.</span></span>

## <span data-ttu-id="ca730-128">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ca730-128">PARAMETERS</span></span>

### <span data-ttu-id="ca730-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca730-129">-DefaultProfile</span></span>
<span data-ttu-id="ca730-130">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca730-131">-Name</span><span class="sxs-lookup"><span data-stu-id="ca730-131">-Name</span></span>
<span data-ttu-id="ca730-132">이 레코드 집합의 레코드 이름(영역의 이름과 종료점 없이)입니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-132">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="ca730-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ca730-133">-ParentResourceId</span></span>
<span data-ttu-id="ca730-134">개인 DNS 영역 ResourceID.</span><span class="sxs-lookup"><span data-stu-id="ca730-134">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="ca730-135">-RecordType</span><span class="sxs-lookup"><span data-stu-id="ca730-135">-RecordType</span></span>
<span data-ttu-id="ca730-136">이 레코드 집합의 DNS 레코드 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-136">The type of DNS records in this record set.</span></span>

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

### <span data-ttu-id="ca730-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca730-137">-ResourceGroupName</span></span>
<span data-ttu-id="ca730-138">영역이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-138">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="ca730-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="ca730-139">-Zone</span></span>
<span data-ttu-id="ca730-140">레코드 집합을 만들 영역의 DnsZone 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-140">The DnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="ca730-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="ca730-141">-ZoneName</span></span>
<span data-ttu-id="ca730-142">레코드 집합을 만들 영역(종료점 없이).</span><span class="sxs-lookup"><span data-stu-id="ca730-142">The zone in which to create the record set (without a terminating dot).</span></span>

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

### <span data-ttu-id="ca730-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca730-143">CommonParameters</span></span>
<span data-ttu-id="ca730-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ca730-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca730-145">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ca730-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca730-146">입력</span><span class="sxs-lookup"><span data-stu-id="ca730-146">INPUTS</span></span>

### <span data-ttu-id="ca730-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="ca730-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="ca730-148">System.String</span><span class="sxs-lookup"><span data-stu-id="ca730-148">System.String</span></span>

## <span data-ttu-id="ca730-149">출력</span><span class="sxs-lookup"><span data-stu-id="ca730-149">OUTPUTS</span></span>

### <span data-ttu-id="ca730-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ca730-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="ca730-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ca730-151">NOTES</span></span>

## <span data-ttu-id="ca730-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca730-152">RELATED LINKS</span></span>
