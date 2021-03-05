---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: b28153176fdc591bc7298b45f75e8befa59e8554
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987639"
---
# <span data-ttu-id="12e9c-101">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="12e9c-101">Set-AzPrivateDnsZone</span></span>

## <span data-ttu-id="12e9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12e9c-102">SYNOPSIS</span></span>
<span data-ttu-id="12e9c-103">리소스 그룹에서 개인 DNS 지역을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="12e9c-103">Updates a Private DNS zone from a resource group.</span></span>

## <span data-ttu-id="12e9c-104">구문</span><span class="sxs-lookup"><span data-stu-id="12e9c-104">SYNTAX</span></span>

### <span data-ttu-id="12e9c-105">필드(기본값)</span><span class="sxs-lookup"><span data-stu-id="12e9c-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12e9c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="12e9c-106">ResourceId</span></span>
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12e9c-107">개체</span><span class="sxs-lookup"><span data-stu-id="12e9c-107">Object</span></span>
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12e9c-108">설명</span><span class="sxs-lookup"><span data-stu-id="12e9c-108">DESCRIPTION</span></span>
<span data-ttu-id="12e9c-109">**Set-AzPrivateDnsZone cmdlet은** 지정된 리소스 그룹에서 DNS(개인 도메인 이름 시스템) 지역을 영구적으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="12e9c-109">The **Set-AzPrivateDnsZone** cmdlet permanently updates a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="12e9c-110">PrivateZone 매개 변수를 사용하여  **PrivateDnsZone** 개체를 전달하거나 파이프라인 연산자를 사용하여 전달하거나 이름 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다. </span><span class="sxs-lookup"><span data-stu-id="12e9c-110">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="12e9c-111">확인 매개 변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="12e9c-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="12e9c-112">PrivateDnsZone 개체(파이프라인 또는 영역 매개 변수를 통해  전달)를 사용하여 영역을 지정하는 경우 로컬 **PrivateDnsZone** 개체가 검색된 이후 Azure DNS에서 변경된 경우 영역이 업데이트되지 않습니다(DNS 영역 리소스에 직접 작업만 변경으로 수, 영역 내의 레코드 집합에 대한 작업은 변경되지 않습니다). </span><span class="sxs-lookup"><span data-stu-id="12e9c-112">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="12e9c-113">그러면 동시 영역 변경에 대한 보호가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="12e9c-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="12e9c-114">이는 덮어 덮어 사용 매개 변수를 사용하여 억제될 수 있습니다. 이는 동시 변경 내용에 관계없이 영역이 업데이트됩니다. </span><span class="sxs-lookup"><span data-stu-id="12e9c-114">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="12e9c-115">예제</span><span class="sxs-lookup"><span data-stu-id="12e9c-115">EXAMPLES</span></span>

### <span data-ttu-id="12e9c-116">예제 1: 개인 영역 업데이트</span><span class="sxs-lookup"><span data-stu-id="12e9c-116">Example 1: Updates a private zone</span></span>
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

## <span data-ttu-id="12e9c-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="12e9c-117">PARAMETERS</span></span>

### <span data-ttu-id="12e9c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e9c-118">-DefaultProfile</span></span>
<span data-ttu-id="12e9c-119">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="12e9c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12e9c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="12e9c-120">-Name</span></span>
<span data-ttu-id="12e9c-121">이 cmdlet이 업데이트하는 개인 DNS 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="12e9c-121">Specifies the name of the Private DNS zone that this cmdlet updates.</span></span>
<span data-ttu-id="12e9c-122">*ResourceGroupName 매개 변수도 지정해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="12e9c-122">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="12e9c-123">또는 영역 매개 변수를 사용하여 개인 DNS 지역을 지정할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="12e9c-123">Alternatively, you can specify the private DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="12e9c-124">-덮어 덮어 덮어 덮어 덮어</span><span class="sxs-lookup"><span data-stu-id="12e9c-124">-Overwrite</span></span>
<span data-ttu-id="12e9c-125">**PrivateDnsZone** 개체(파이프라인 또는 영역 매개 변수를 통해  전달)를 사용하여 영역을 지정할 때 로컬 **DnsZone** 개체가 검색된 이후 Azure DNS에서 변경된 경우 영역이 업데이트되지 않습니다(DNS 영역 리소스에 직접 작업만 변경으로, 영역 내의 레코드 집합에 대한 작업은 변경되지 않습니다).</span><span class="sxs-lookup"><span data-stu-id="12e9c-125">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="12e9c-126">그러면 동시 영역 변경에 대한 보호가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="12e9c-126">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="12e9c-127">이는 덮어 덮어 사용 매개 변수를 사용하여 억제될 수 있습니다. 이는 동시 변경 내용에 관계없이 영역이 업데이트됩니다. </span><span class="sxs-lookup"><span data-stu-id="12e9c-127">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="12e9c-128">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="12e9c-128">-PrivateZone</span></span>
<span data-ttu-id="12e9c-129">설정할 영역 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="12e9c-129">The zone object to set.</span></span>

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

### <span data-ttu-id="12e9c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12e9c-130">-ResourceGroupName</span></span>
<span data-ttu-id="12e9c-131">업데이트할 영역이 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="12e9c-131">Specifies the name of the resource group that contains the zone to be updated.</span></span>
<span data-ttu-id="12e9c-132">*ZoneName 매개 변수도 지정해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="12e9c-132">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="12e9c-133">또는 파이프라인 또는 영역 매개 변수를 통해 전달된 **DnsZone** 개체를 사용하여 개인 DNS 지역을 *지정할 수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="12e9c-133">Alternatively, you can specify the private DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="12e9c-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12e9c-134">-ResourceId</span></span>
<span data-ttu-id="12e9c-135">개인 DNS 영역 ResourceID.</span><span class="sxs-lookup"><span data-stu-id="12e9c-135">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="12e9c-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="12e9c-136">-Tag</span></span>
<span data-ttu-id="12e9c-137">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="12e9c-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="12e9c-138">-확인</span><span class="sxs-lookup"><span data-stu-id="12e9c-138">-Confirm</span></span>
<span data-ttu-id="12e9c-139">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="12e9c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12e9c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12e9c-140">-WhatIf</span></span>
<span data-ttu-id="12e9c-141">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="12e9c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12e9c-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="12e9c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12e9c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e9c-143">CommonParameters</span></span>
<span data-ttu-id="12e9c-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="12e9c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e9c-145">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="12e9c-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e9c-146">입력</span><span class="sxs-lookup"><span data-stu-id="12e9c-146">INPUTS</span></span>

### <span data-ttu-id="12e9c-147">System.String</span><span class="sxs-lookup"><span data-stu-id="12e9c-147">System.String</span></span>

### <span data-ttu-id="12e9c-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="12e9c-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="12e9c-149">출력</span><span class="sxs-lookup"><span data-stu-id="12e9c-149">OUTPUTS</span></span>

### <span data-ttu-id="12e9c-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="12e9c-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="12e9c-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="12e9c-151">NOTES</span></span>

## <span data-ttu-id="12e9c-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12e9c-152">RELATED LINKS</span></span>

[<span data-ttu-id="12e9c-153">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="12e9c-153">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="12e9c-154">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="12e9c-154">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="12e9c-155">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="12e9c-155">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
