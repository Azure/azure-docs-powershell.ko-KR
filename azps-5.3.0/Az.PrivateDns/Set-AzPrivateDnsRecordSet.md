---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 04c8153bae884a074a8db10e8f4330f26c4c5502
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490832"
---
# <span data-ttu-id="f61a9-101">Set-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f61a9-101">Set-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="f61a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f61a9-102">SYNOPSIS</span></span>
<span data-ttu-id="f61a9-103">사설 DNS 영역의 레코드 집합을 업데이트/설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f61a9-103">Updates/Sets a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="f61a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="f61a9-104">SYNTAX</span></span>

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f61a9-105">설명</span><span class="sxs-lookup"><span data-stu-id="f61a9-105">DESCRIPTION</span></span>
<span data-ttu-id="f61a9-106">이 Set-AzPrivateDnsRecordSet cmdlet은 로컬 RecordSet 개체에서 Azure 개인 DNS 서비스의 레코드 집합을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f61a9-106">The Set-AzPrivateDnsRecordSet cmdlet updates a record set in the Azure Private DNS service from a local RecordSet object.</span></span> <span data-ttu-id="f61a9-107">RecordSet 개체를 매개 변수로 전달하거나 파이프라인 연산자를 사용하여 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f61a9-107">You can pass a RecordSet object as a parameter or by using the pipeline operator.</span></span> <span data-ttu-id="f61a9-108">Confirm 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f61a9-108">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="f61a9-109">로컬 RecordSet 개체를 검색한 후 Azure 개인 DNS에서 변경된 레코드 집합은 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f61a9-109">The record set is not updated if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="f61a9-110">이렇게 하면 동시 변경에 대한 보호를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f61a9-110">This provides protection for concurrent changes.</span></span> <span data-ttu-id="f61a9-111">동시 변경 내용에 관계없이 레코드 집합을 업데이트하는 덮어 사용 매개 변수를 사용하여 이 동작을 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f61a9-111">You can suppress this behavior using the Overwrite parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="f61a9-112">예제</span><span class="sxs-lookup"><span data-stu-id="f61a9-112">EXAMPLES</span></span>

### <span data-ttu-id="f61a9-113">예제 1: 레코드 집합 업데이트</span><span class="sxs-lookup"><span data-stu-id="f61a9-113">Example 1: Update a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 172.16.0.0, 172.31.255.255}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f61a9-114">첫 번째 명령은 Get-AzPrivateDnsRecordSet cmdlet을 사용하여 지정된 레코드 집합을 구한 다음, $RecordSet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f61a9-114">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="f61a9-115">두 번째 및 세 번째 명령은 레코드 집합에 두 개의 A 레코드를 추가하는 오프 라인 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="f61a9-115">The second and third commands are off-line operations to add two A records to the record set.</span></span> <span data-ttu-id="f61a9-116">마지막 명령은 Set-AzPrivateDnsRecordSet cmdlet을 사용하여 업데이트를 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="f61a9-116">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to commit the update.</span></span>

### <span data-ttu-id="f61a9-117">예제 2: SOA 레코드 업데이트</span><span class="sxs-lookup"><span data-stu-id="f61a9-117">Example 2: Update an SOA record</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SOA/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : Myresourcegroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SOA
Records           : {[internal.cloudapp.net,admin.myzone.com,3600,300,2419200,300]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f61a9-118">첫 번째 명령은 Get-AzPrivateDnsRecordSet cmdlet을 사용하여 지정된 레코드 집합을 구한 다음, $RecordSet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f61a9-118">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="f61a9-119">두 번째 명령은 지정된 SOA 레코드를 $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="f61a9-119">The second command updates the specified SOA record in $RecordSet.</span></span> <span data-ttu-id="f61a9-120">마지막 명령은 Set-AzPrivateDnsRecordSet cmdlet을 사용하여 $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="f61a9-120">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="f61a9-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f61a9-121">PARAMETERS</span></span>

### <span data-ttu-id="f61a9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f61a9-122">-DefaultProfile</span></span>
<span data-ttu-id="f61a9-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f61a9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f61a9-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="f61a9-124">-Overwrite</span></span>
<span data-ttu-id="f61a9-125">낙관적 동시성 검사에는 RecordSet 매개 변수의 ETag 필드를 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f61a9-125">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="f61a9-126">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="f61a9-126">-RecordSet</span></span>
<span data-ttu-id="f61a9-127">레코드를 추가할 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="f61a9-127">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="f61a9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f61a9-128">-Confirm</span></span>
<span data-ttu-id="f61a9-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f61a9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f61a9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f61a9-130">-WhatIf</span></span>
<span data-ttu-id="f61a9-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f61a9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f61a9-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f61a9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f61a9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f61a9-133">CommonParameters</span></span>
<span data-ttu-id="f61a9-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f61a9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f61a9-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f61a9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f61a9-136">입력</span><span class="sxs-lookup"><span data-stu-id="f61a9-136">INPUTS</span></span>

### <span data-ttu-id="f61a9-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f61a9-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="f61a9-138">출력</span><span class="sxs-lookup"><span data-stu-id="f61a9-138">OUTPUTS</span></span>

### <span data-ttu-id="f61a9-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f61a9-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="f61a9-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f61a9-140">NOTES</span></span>

## <span data-ttu-id="f61a9-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f61a9-141">RELATED LINKS</span></span>
