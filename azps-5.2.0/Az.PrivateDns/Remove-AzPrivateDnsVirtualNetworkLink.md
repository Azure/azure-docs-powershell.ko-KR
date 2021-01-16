---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 63fbe26fa0a9ac7ca5eb985a3806886adeb2a2f8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348722"
---
# <span data-ttu-id="dc5e3-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="dc5e3-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="dc5e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc5e3-102">SYNOPSIS</span></span>
<span data-ttu-id="dc5e3-103">리소스 그룹에서 가상 네트워크 링크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="dc5e3-104">구문</span><span class="sxs-lookup"><span data-stu-id="dc5e3-104">SYNTAX</span></span>

### <span data-ttu-id="dc5e3-105">필드(기본값)</span><span class="sxs-lookup"><span data-stu-id="dc5e3-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc5e3-106">개체</span><span class="sxs-lookup"><span data-stu-id="dc5e3-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc5e3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc5e3-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc5e3-108">설명</span><span class="sxs-lookup"><span data-stu-id="dc5e3-108">DESCRIPTION</span></span>
<span data-ttu-id="dc5e3-109">**Remove-AzPrivateDnsVirtualNetworkLink** cmdlet은 지정된 리소스 그룹에서 개인 DNS(도메인 이름 시스템) 링크를 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="dc5e3-110">Link 매개 변수를 사용하여 또는 파이프라인 연산자를 사용하여 **PSPrivateDnsVirtualNetworkLink** 개체를 전달하거나  Name *ZoneName* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다. </span><span class="sxs-lookup"><span data-stu-id="dc5e3-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="dc5e3-111">Confirm 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="dc5e3-112">**PSPrivateDnsVirtualNetworkLink** 개체를 사용하여 링크를 지정할 때(파이프라인 또는  링크 매개 변수를 통해 전달) 로컬 **PSPrivateDnsVirtualNetworkLink** 개체가 검색된 이후 Azure 개인 DNS에서 변경된 경우 링크가 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="dc5e3-113">이렇게 하면 동시 영역 변경에 대한 보호를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="dc5e3-114">이는 동시 변경  내용에 관계없이 영역이 삭제되는 덮어 사용 매개 변수를 사용하여 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="dc5e3-115">예제</span><span class="sxs-lookup"><span data-stu-id="dc5e3-115">EXAMPLES</span></span>

### <span data-ttu-id="dc5e3-116">예제 1: 링크 제거</span><span class="sxs-lookup"><span data-stu-id="dc5e3-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="dc5e3-117">이 명령은 MyResourceGroup이라는 리소스 그룹에서 myzone.com 연결된 mylink 링크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="dc5e3-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc5e3-118">PARAMETERS</span></span>

### <span data-ttu-id="dc5e3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc5e3-119">-DefaultProfile</span></span>
<span data-ttu-id="dc5e3-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dc5e3-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc5e3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc5e3-121">-InputObject</span></span>
<span data-ttu-id="dc5e3-122">제거할 가상 네트워크 링크 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-122">The virtual network link object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc5e3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="dc5e3-123">-Name</span></span>
<span data-ttu-id="dc5e3-124">삭제할 링크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="dc5e3-125">*ResourceGroupName* 및 *ZoneName 매개 변수도 지정해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="dc5e3-126">또는 Link 매개 변수를 사용하여 링크를 지정할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="dc5e3-127">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="dc5e3-127">-Overwrite</span></span>
<span data-ttu-id="dc5e3-128">**PSPrivateDnsVirtualNetworkLink** 개체를 사용하여 지역을 지정할 때(파이프라인 또는  링크 매개 변수를 통해 전달) 로컬 **PSPrivateDnsVirtualNetworkLink** 개체가 검색된 이후 Azure DNS에서 변경된 경우 영역이 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="dc5e3-129">이렇게 하면 동시 영역 변경에 대한 보호를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="dc5e3-130">이는 동시 변경  내용에 관계없이 영역이 삭제되는 덮어 사용 매개 변수를 사용하여 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="dc5e3-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc5e3-131">-PassThru</span></span>
<span data-ttu-id="dc5e3-132">작업의 결과(부울)를 전달하는 데 사용됩니다. 파이프라인에서 가상 네트워크 링크를 추가로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="dc5e3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc5e3-133">-ResourceGroupName</span></span>
<span data-ttu-id="dc5e3-134">제거할 링크가 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="dc5e3-135">*ZoneName* 및 Name 매개 변수도 *지정해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="dc5e3-136">또는 파이프라인 또는 Link 매개 변수를 통해 전달된 **PSPrivateDnsVirtualNetworkLink** 개체를 사용하여 DNS 영역을 지정할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="dc5e3-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc5e3-137">-ResourceId</span></span>
<span data-ttu-id="dc5e3-138">링크의 ARM 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-138">Specifies the ARM resource ID of the link.</span></span>

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

### <span data-ttu-id="dc5e3-139">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="dc5e3-139">-ZoneName</span></span>
<span data-ttu-id="dc5e3-140">링크가 연결된 개인 DNS 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="dc5e3-141">*ResourceGroupName* 및 Name 매개 변수도 *지정해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="dc5e3-142">또는 Link 매개 변수를 사용하여 링크를 지정할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="dc5e3-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc5e3-143">-Confirm</span></span>
<span data-ttu-id="dc5e3-144">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc5e3-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc5e3-145">-WhatIf</span></span>
<span data-ttu-id="dc5e3-146">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="dc5e3-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc5e3-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc5e3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc5e3-148">CommonParameters</span></span>
<span data-ttu-id="dc5e3-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc5e3-150">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dc5e3-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc5e3-151">입력</span><span class="sxs-lookup"><span data-stu-id="dc5e3-151">INPUTS</span></span>

### <span data-ttu-id="dc5e3-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="dc5e3-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="dc5e3-153">System.String</span><span class="sxs-lookup"><span data-stu-id="dc5e3-153">System.String</span></span>

## <span data-ttu-id="dc5e3-154">출력</span><span class="sxs-lookup"><span data-stu-id="dc5e3-154">OUTPUTS</span></span>

### <span data-ttu-id="dc5e3-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dc5e3-155">System.Boolean</span></span>

## <span data-ttu-id="dc5e3-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dc5e3-156">NOTES</span></span>

## <span data-ttu-id="dc5e3-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc5e3-157">RELATED LINKS</span></span>

[<span data-ttu-id="dc5e3-158">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="dc5e3-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="dc5e3-159">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="dc5e3-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="dc5e3-160">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="dc5e3-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
