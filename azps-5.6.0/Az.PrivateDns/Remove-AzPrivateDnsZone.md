---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: 8c8e7059a6c23c928180b8d6fab3cfdbbfd9ed5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970411"
---
# <span data-ttu-id="7c072-101">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="7c072-101">Remove-AzPrivateDnsZone</span></span>

## <span data-ttu-id="7c072-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c072-102">SYNOPSIS</span></span>
<span data-ttu-id="7c072-103">리소스 그룹에서 개인 DNS 영역이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c072-103">Removes a private DNS zone from a resource group.</span></span>

## <span data-ttu-id="7c072-104">구문</span><span class="sxs-lookup"><span data-stu-id="7c072-104">SYNTAX</span></span>

### <span data-ttu-id="7c072-105">필드(기본값)</span><span class="sxs-lookup"><span data-stu-id="7c072-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c072-106">개체</span><span class="sxs-lookup"><span data-stu-id="7c072-106">Object</span></span>
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c072-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c072-107">ResourceId</span></span>
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c072-108">설명</span><span class="sxs-lookup"><span data-stu-id="7c072-108">DESCRIPTION</span></span>
<span data-ttu-id="7c072-109">**Remove-AzPrivateDnsZone cmdlet은** 지정된 리소스 그룹에서 DNS(개인 도메인 이름 시스템) 영역이 영구적으로 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c072-109">The **Remove-AzPrivateDnsZone** cmdlet permanently deletes a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="7c072-110">영역 내에 포함된 모든 레코드 집합도 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c072-110">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="7c072-111">PrivateZone 매개 변수를 사용하여  **PrivateDnsZone** 개체를 전달하거나 파이프라인 연산자를 사용하여 전달하거나 이름 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다. </span><span class="sxs-lookup"><span data-stu-id="7c072-111">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="7c072-112">확인 매개 변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c072-112">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="7c072-113">PrivateDnsZone 개체(파이프라인 또는 영역 매개 변수를 통해  전달)를 사용하여 영역을 지정하는 경우 로컬 **PrivateDnsZone** 개체가 검색된 이후 Azure DNS에서 변경된 경우 영역이 삭제되지 않습니다(DNS 영역 리소스에 직접 작업만 변경으로 수, 영역 내의 레코드 집합의 작업은 변경되지 않습니다). </span><span class="sxs-lookup"><span data-stu-id="7c072-113">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="7c072-114">그러면 동시 영역 변경에 대한 보호가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c072-114">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="7c072-115">이는 덮어 덮어 사용 매개 변수를 사용하여 억제할 수 있습니다. 이는 동시 변경 내용에 관계없이 영역이 삭제됩니다. </span><span class="sxs-lookup"><span data-stu-id="7c072-115">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="7c072-116">예제</span><span class="sxs-lookup"><span data-stu-id="7c072-116">EXAMPLES</span></span>

### <span data-ttu-id="7c072-117">예제 1: 개인 영역 제거</span><span class="sxs-lookup"><span data-stu-id="7c072-117">Example 1: Remove a private zone</span></span>
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="7c072-118">이 명령은 MyResourceGroup이라는 리소스 myzone.com 그룹에서 이라는 영역이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c072-118">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="7c072-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7c072-119">PARAMETERS</span></span>

### <span data-ttu-id="7c072-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c072-120">-DefaultProfile</span></span>
<span data-ttu-id="7c072-121">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7c072-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c072-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7c072-122">-Name</span></span>
<span data-ttu-id="7c072-123">이 cmdlet이 제거한 개인 DNS 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7c072-123">Specifies the name of the private DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="7c072-124">*ResourceGroupName 매개 변수도 지정해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c072-124">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="7c072-125">또는 영역 매개 변수를 사용하여 DNS 지역을 *지정할 수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c072-125">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="7c072-126">-덮어 덮어 덮어 덮어 덮어</span><span class="sxs-lookup"><span data-stu-id="7c072-126">-Overwrite</span></span>
<span data-ttu-id="7c072-127">PrivateDnsZone 개체(파이프라인 또는 영역 매개 변수를 통해  전달)를 사용하여 영역을 지정하는 경우 로컬 **PrivateDnsZone** 개체가 검색된 이후 Azure DNS에서 변경된 경우 영역이 삭제되지 않습니다(DNS 영역 리소스에 직접 작업만 변경으로 수, 영역 내의 레코드 집합의 작업은 변경되지 않습니다). </span><span class="sxs-lookup"><span data-stu-id="7c072-127">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="7c072-128">그러면 동시 영역 변경에 대한 보호가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c072-128">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="7c072-129">이는 덮어 덮어 사용 매개 변수를 사용하여 억제할 수 있습니다. 이는 동시 변경 내용에 관계없이 영역이 삭제됩니다. </span><span class="sxs-lookup"><span data-stu-id="7c072-129">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="7c072-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c072-130">-PassThru</span></span>
<span data-ttu-id="7c072-131">작업의 결과(부울)를 전달하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c072-131">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="7c072-132">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="7c072-132">-PrivateZone</span></span>
<span data-ttu-id="7c072-133">삭제할 개인 영역 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7c072-133">The private zone object to delete.</span></span>

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

### <span data-ttu-id="7c072-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c072-134">-ResourceGroupName</span></span>
<span data-ttu-id="7c072-135">제거할 영역이 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7c072-135">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="7c072-136">*ZoneName 매개 변수도 지정해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c072-136">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="7c072-137">또는 파이프라인 또는 영역 매개 변수를 통해 전달되는 **PrivateDnsZone** 개체를 사용하여 DNS 영역을 *지정할 수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c072-137">Alternatively, you can specify the DNS zone using a **PrivateDnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="7c072-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c072-138">-ResourceId</span></span>
<span data-ttu-id="7c072-139">개인 DNS 영역 ResourceID.</span><span class="sxs-lookup"><span data-stu-id="7c072-139">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="7c072-140">-확인</span><span class="sxs-lookup"><span data-stu-id="7c072-140">-Confirm</span></span>
<span data-ttu-id="7c072-141">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c072-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c072-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c072-142">-WhatIf</span></span>
<span data-ttu-id="7c072-143">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c072-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c072-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c072-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c072-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c072-145">CommonParameters</span></span>
<span data-ttu-id="7c072-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7c072-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c072-147">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7c072-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c072-148">입력</span><span class="sxs-lookup"><span data-stu-id="7c072-148">INPUTS</span></span>

### <span data-ttu-id="7c072-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="7c072-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="7c072-150">System.String</span><span class="sxs-lookup"><span data-stu-id="7c072-150">System.String</span></span>

## <span data-ttu-id="7c072-151">출력</span><span class="sxs-lookup"><span data-stu-id="7c072-151">OUTPUTS</span></span>

### <span data-ttu-id="7c072-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7c072-152">System.Boolean</span></span>

## <span data-ttu-id="7c072-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7c072-153">NOTES</span></span>

## <span data-ttu-id="7c072-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c072-154">RELATED LINKS</span></span>

[<span data-ttu-id="7c072-155">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="7c072-155">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="7c072-156">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="7c072-156">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="7c072-157">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="7c072-157">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
