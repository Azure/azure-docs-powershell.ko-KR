---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: a5c4ae9492d64bc8c84439f747031d6facd88673
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872810"
---
# <span data-ttu-id="b73e5-101">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b73e5-101">Set-AzPrivateDnsZone</span></span>

## <span data-ttu-id="b73e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b73e5-102">SYNOPSIS</span></span>
<span data-ttu-id="b73e5-103">리소스 그룹에서 개인 DNS 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-103">Updates a Private DNS zone from a resource group.</span></span>

## <span data-ttu-id="b73e5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b73e5-104">SYNTAX</span></span>

### <span data-ttu-id="b73e5-105">필드 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b73e5-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b73e5-106">리소스</span><span class="sxs-lookup"><span data-stu-id="b73e5-106">ResourceId</span></span>
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b73e5-107">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="b73e5-107">Object</span></span>
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b73e5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b73e5-108">DESCRIPTION</span></span>
<span data-ttu-id="b73e5-109">**AzPrivateDnsZone** cmdlet은 지정 된 리소스 그룹에서 DNS (개인 도메인 이름 시스템) 영역을 영구적으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-109">The **Set-AzPrivateDnsZone** cmdlet permanently updates a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="b73e5-110">*PrivateZone* 매개 변수를 사용 하거나 파이프라인 연산자를 사용 하 여 **PrivateDnsZone** 개체를 전달 하거나 *Name* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-110">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="b73e5-111">확인 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="b73e5-112">**PrivateDnsZone** 개체 (파이프라인 또는 *zone* 매개 변수를 통해 전달 됨)를 사용 하 여 영역을 지정 하는 경우, 로컬 **PrivateDnsZone** 개체를 검색 한 후에 Azure DNS에서 해당 영역이 변경 된 것이 아니라 DNS 영역 리소스에서 직접 작업을 수행 하는 경우에만 해당 영역 내의 레코드 집합에 대 한 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-112">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="b73e5-113">이는 동시 영역 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="b73e5-114">이는 *덮어쓰기* 매개 변수를 사용 하 여 억제할 수 있으며, 동시 변경 내용에 관계 없이 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-114">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="b73e5-115">예제의</span><span class="sxs-lookup"><span data-stu-id="b73e5-115">EXAMPLES</span></span>

### <span data-ttu-id="b73e5-116">예제 1: 개인 영역 업데이트</span><span class="sxs-lookup"><span data-stu-id="b73e5-116">Example 1: Updates a private zone</span></span>
```
PS C:\>Set-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup" -Tag @{tag1="value1";tag2="value2"}


This command updates the zone named myzone.com from the resource group named MyResourceGroup with the tags provided. Use Get-AzPrivateDnsZone to retrieve the updated zone. Updated zone would look something like this:

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {tag1="value1";tag2="value2"}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="b73e5-117">변수</span><span class="sxs-lookup"><span data-stu-id="b73e5-117">PARAMETERS</span></span>

### <span data-ttu-id="b73e5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b73e5-118">-DefaultProfile</span></span>
<span data-ttu-id="b73e5-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b73e5-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b73e5-120">-이름</span><span class="sxs-lookup"><span data-stu-id="b73e5-120">-Name</span></span>
<span data-ttu-id="b73e5-121">이 cmdlet이 업데이트 하는 개인 DNS 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-121">Specifies the name of the Private DNS zone that this cmdlet updates.</span></span>
<span data-ttu-id="b73e5-122">또한 *ResourceGroupName* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-122">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="b73e5-123">또는 *zone* 매개 변수를 사용 하 여 개인 DNS 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-123">Alternatively, you can specify the private DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="b73e5-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="b73e5-124">-Overwrite</span></span>
<span data-ttu-id="b73e5-125">**PrivateDnsZone** 개체 (파이프라인 또는 *zone* 매개 변수를 통해 전달 됨)를 사용 하 여 영역을 지정 하는 경우, 로컬 **DnsZone** 개체를 검색 한 후에 Azure DNS에서 해당 영역이 변경 된 것이 아니라 DNS 영역 리소스에서 직접 작업을 수행 하는 경우에만 해당 영역 내의 레코드 집합에 대 한 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-125">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="b73e5-126">이는 동시 영역 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-126">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="b73e5-127">이는 *덮어쓰기* 매개 변수를 사용 하 여 억제할 수 있으며, 동시 변경 내용에 관계 없이 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-127">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b73e5-128">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="b73e5-128">-PrivateZone</span></span>
<span data-ttu-id="b73e5-129">설정할 영역 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-129">The zone object to set.</span></span>

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

### <span data-ttu-id="b73e5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b73e5-130">-ResourceGroupName</span></span>
<span data-ttu-id="b73e5-131">업데이트 될 영역이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-131">Specifies the name of the resource group that contains the zone to be updated.</span></span>
<span data-ttu-id="b73e5-132">*ZoneName* 매개 변수도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-132">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="b73e5-133">또는 파이프라인 또는 *zone* 매개 변수를 통해 전달 되는 **DnsZone** 개체를 사용 하 여 개인 DNS 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-133">Alternatively, you can specify the private DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="b73e5-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b73e5-134">-ResourceId</span></span>
<span data-ttu-id="b73e5-135">개인 DNS 영역 ResourceID</span><span class="sxs-lookup"><span data-stu-id="b73e5-135">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="b73e5-136">태그</span><span class="sxs-lookup"><span data-stu-id="b73e5-136">-Tag</span></span>
<span data-ttu-id="b73e5-137">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="b73e5-138">-확인</span><span class="sxs-lookup"><span data-stu-id="b73e5-138">-Confirm</span></span>
<span data-ttu-id="b73e5-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b73e5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b73e5-140">-WhatIf</span></span>
<span data-ttu-id="b73e5-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b73e5-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b73e5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b73e5-143">CommonParameters</span></span>
<span data-ttu-id="b73e5-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b73e5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b73e5-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b73e5-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b73e5-146">입력</span><span class="sxs-lookup"><span data-stu-id="b73e5-146">INPUTS</span></span>

### <span data-ttu-id="b73e5-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b73e5-147">System.String</span></span>

### <span data-ttu-id="b73e5-148">PrivateDns. PSPrivateDnsZone/.</span><span class="sxs-lookup"><span data-stu-id="b73e5-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="b73e5-149">출력</span><span class="sxs-lookup"><span data-stu-id="b73e5-149">OUTPUTS</span></span>

### <span data-ttu-id="b73e5-150">PrivateDns. PSPrivateDnsZone/.</span><span class="sxs-lookup"><span data-stu-id="b73e5-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="b73e5-151">상속자</span><span class="sxs-lookup"><span data-stu-id="b73e5-151">NOTES</span></span>

## <span data-ttu-id="b73e5-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b73e5-152">RELATED LINKS</span></span>

[<span data-ttu-id="b73e5-153">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b73e5-153">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="b73e5-154">새로운 AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b73e5-154">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="b73e5-155">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b73e5-155">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
