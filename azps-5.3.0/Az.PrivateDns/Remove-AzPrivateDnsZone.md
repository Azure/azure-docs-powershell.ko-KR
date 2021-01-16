---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d381af8de23b5eb781882f10670e6ba69afbc571
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490835"
---
# <span data-ttu-id="a2a2b-101">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="a2a2b-101">Remove-AzPrivateDnsZone</span></span>

## <span data-ttu-id="a2a2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2a2b-102">SYNOPSIS</span></span>
<span data-ttu-id="a2a2b-103">리소스 그룹에서 사설 DNS 영역이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-103">Removes a private DNS zone from a resource group.</span></span>

## <span data-ttu-id="a2a2b-104">구문</span><span class="sxs-lookup"><span data-stu-id="a2a2b-104">SYNTAX</span></span>

### <span data-ttu-id="a2a2b-105">필드(기본값)</span><span class="sxs-lookup"><span data-stu-id="a2a2b-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2a2b-106">개체</span><span class="sxs-lookup"><span data-stu-id="a2a2b-106">Object</span></span>
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2a2b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2a2b-107">ResourceId</span></span>
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2a2b-108">설명</span><span class="sxs-lookup"><span data-stu-id="a2a2b-108">DESCRIPTION</span></span>
<span data-ttu-id="a2a2b-109">**Remove-AzPrivateDnsZone** cmdlet은 지정된 리소스 그룹에서 사설 DNS(도메인 이름 시스템) 영역이 영구적으로 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-109">The **Remove-AzPrivateDnsZone** cmdlet permanently deletes a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="a2a2b-110">영역 내에 포함된 모든 레코드 집합도 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-110">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="a2a2b-111">*PrivateZone* 매개 변수를 사용하거나 파이프라인 연산자를 사용하여 **PrivateDnsZone** 개체를 전달하거나 *Name* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-111">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="a2a2b-112">Confirm 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-112">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="a2a2b-113">PrivateDnsZone 개체(파이프라인 또는 영역 매개 변수를 통해  전달)를 사용하여 영역을 지정할 때 로컬 **PrivateDnsZone** 개체가 검색된 이후 Azure DNS에서 변경된 경우 영역이 삭제되지 않습니다(DNS 영역 리소스에 대한 직접 작업만 변경으로 계산, 영역 내의 레코드 집합에 대한 작업은 수행되지 않습니다). </span><span class="sxs-lookup"><span data-stu-id="a2a2b-113">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="a2a2b-114">이렇게 하면 동시 영역 변경에 대한 보호를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-114">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="a2a2b-115">이는 동시 변경  내용에 관계없이 영역이 삭제되는 덮어 사용 매개 변수를 사용하여 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-115">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="a2a2b-116">예제</span><span class="sxs-lookup"><span data-stu-id="a2a2b-116">EXAMPLES</span></span>

### <span data-ttu-id="a2a2b-117">예제 1: 개인 영역 제거</span><span class="sxs-lookup"><span data-stu-id="a2a2b-117">Example 1: Remove a private zone</span></span>
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a2a2b-118">이 명령은 MyResourceGroup이라는 myzone.com 그룹에서 이름이 지정되는 영역이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-118">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="a2a2b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2a2b-119">PARAMETERS</span></span>

### <span data-ttu-id="a2a2b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2a2b-120">-DefaultProfile</span></span>
<span data-ttu-id="a2a2b-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a2a2b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2a2b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a2a2b-122">-Name</span></span>
<span data-ttu-id="a2a2b-123">이 cmdlet이 제거하는 개인 DNS 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-123">Specifies the name of the private DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="a2a2b-124">*ResourceGroupName 매개 변수도 지정해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-124">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="a2a2b-125">또는 영역 매개 변수를 사용하여 DNS 지역을 지정할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-125">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="a2a2b-126">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="a2a2b-126">-Overwrite</span></span>
<span data-ttu-id="a2a2b-127">PrivateDnsZone 개체(파이프라인 또는 영역 매개 변수를 통해  전달)를 사용하여 영역을 지정할 때 로컬 **PrivateDnsZone** 개체가 검색된 이후 Azure DNS에서 변경된 경우 영역이 삭제되지 않습니다(DNS 영역 리소스에 대한 직접 작업만 변경으로 계산, 영역 내의 레코드 집합에 대한 작업은 수행되지 않습니다). </span><span class="sxs-lookup"><span data-stu-id="a2a2b-127">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="a2a2b-128">이렇게 하면 동시 영역 변경에 대한 보호를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-128">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="a2a2b-129">이는 동시 변경  내용에 관계없이 영역이 삭제되는 덮어 사용 매개 변수를 사용하여 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-129">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="a2a2b-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2a2b-130">-PassThru</span></span>
<span data-ttu-id="a2a2b-131">작업의 결과(부울)를 전달하는 데 사용됩니다. 사설 영역은 파이프라인을 더 아래로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-131">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="a2a2b-132">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="a2a2b-132">-PrivateZone</span></span>
<span data-ttu-id="a2a2b-133">삭제할 개인 영역 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-133">The private zone object to delete.</span></span>

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

### <span data-ttu-id="a2a2b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2a2b-134">-ResourceGroupName</span></span>
<span data-ttu-id="a2a2b-135">제거할 영역이 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-135">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="a2a2b-136">*ZoneName 매개 변수도 지정해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-136">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="a2a2b-137">또는 파이프라인 또는 영역 매개 변수를 통해 전달된 **PrivateDnsZone** 개체를 사용하여 DNS 지역을 지정할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-137">Alternatively, you can specify the DNS zone using a **PrivateDnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="a2a2b-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2a2b-138">-ResourceId</span></span>
<span data-ttu-id="a2a2b-139">사설 DNS 영역 ResourceID.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-139">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="a2a2b-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2a2b-140">-Confirm</span></span>
<span data-ttu-id="a2a2b-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2a2b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2a2b-142">-WhatIf</span></span>
<span data-ttu-id="a2a2b-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a2a2b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2a2b-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2a2b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2a2b-145">CommonParameters</span></span>
<span data-ttu-id="a2a2b-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2a2b-147">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a2a2b-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2a2b-148">입력</span><span class="sxs-lookup"><span data-stu-id="a2a2b-148">INPUTS</span></span>

### <span data-ttu-id="a2a2b-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="a2a2b-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="a2a2b-150">System.String</span><span class="sxs-lookup"><span data-stu-id="a2a2b-150">System.String</span></span>

## <span data-ttu-id="a2a2b-151">출력</span><span class="sxs-lookup"><span data-stu-id="a2a2b-151">OUTPUTS</span></span>

### <span data-ttu-id="a2a2b-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a2a2b-152">System.Boolean</span></span>

## <span data-ttu-id="a2a2b-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a2a2b-153">NOTES</span></span>

## <span data-ttu-id="a2a2b-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2a2b-154">RELATED LINKS</span></span>

[<span data-ttu-id="a2a2b-155">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="a2a2b-155">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="a2a2b-156">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="a2a2b-156">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="a2a2b-157">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="a2a2b-157">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
