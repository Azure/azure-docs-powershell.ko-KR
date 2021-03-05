---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 8de4922b5d71902fe22a17a6c02f21a40e35ddc7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965552"
---
# <span data-ttu-id="4dbf0-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4dbf0-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="4dbf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dbf0-102">SYNOPSIS</span></span>
<span data-ttu-id="4dbf0-103">리소스 그룹에서 가상 네트워크 링크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="4dbf0-104">구문</span><span class="sxs-lookup"><span data-stu-id="4dbf0-104">SYNTAX</span></span>

### <span data-ttu-id="4dbf0-105">필드(기본값)</span><span class="sxs-lookup"><span data-stu-id="4dbf0-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dbf0-106">개체</span><span class="sxs-lookup"><span data-stu-id="4dbf0-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dbf0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4dbf0-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dbf0-108">설명</span><span class="sxs-lookup"><span data-stu-id="4dbf0-108">DESCRIPTION</span></span>
<span data-ttu-id="4dbf0-109">**Remove-AzPrivateDnsVirtualNetworkLink** cmdlet은 지정된 리소스 그룹에서 DNS(개인 도메인 이름 시스템) 링크를 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="4dbf0-110">링크 매개 변수를 사용하여 **PSPrivateDnsVirtualNetworkLink** 개체를 전달하거나 파이프라인 연산자를 사용하여 전달하거나 이름  *영역* 이름 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다. </span><span class="sxs-lookup"><span data-stu-id="4dbf0-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="4dbf0-111">확인 매개 변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="4dbf0-112">**PSPrivateDnsVirtualNetworkLink** 개체를 사용하여 링크를 지정할 때(파이프라인 또는  링크 매개 변수를 통해 전달) 로컬 **PSPrivateDnsVirtualNetworkLink** 개체가 검색된 이후 Azure Private DNS에서 변경된 경우 링크가 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="4dbf0-113">그러면 동시 영역 변경에 대한 보호가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="4dbf0-114">이는 덮어 덮어 사용 매개 변수를 사용하여 억제할 수 있습니다. 이는 동시 변경 내용에 관계없이 영역이 삭제됩니다. </span><span class="sxs-lookup"><span data-stu-id="4dbf0-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="4dbf0-115">예제</span><span class="sxs-lookup"><span data-stu-id="4dbf0-115">EXAMPLES</span></span>

### <span data-ttu-id="4dbf0-116">예제 1: 링크 제거</span><span class="sxs-lookup"><span data-stu-id="4dbf0-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="4dbf0-117">이 명령은 MyResourceGroup이라는 리소스 myzone.com 영역과 연결된 mylink라는 링크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="4dbf0-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4dbf0-118">PARAMETERS</span></span>

### <span data-ttu-id="4dbf0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dbf0-119">-DefaultProfile</span></span>
<span data-ttu-id="4dbf0-120">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4dbf0-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4dbf0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4dbf0-121">-InputObject</span></span>
<span data-ttu-id="4dbf0-122">제거할 가상 네트워크 링크 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-122">The virtual network link object to remove.</span></span>

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

### <span data-ttu-id="4dbf0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4dbf0-123">-Name</span></span>
<span data-ttu-id="4dbf0-124">삭제할 링크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="4dbf0-125">*ResourceGroupName* 및 *ZoneName 매개 변수도 지정해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="4dbf0-126">또는 링크 매개 변수를 사용하여 링크를 지정할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="4dbf0-127">-덮어 덮어 덮어 덮어 덮어</span><span class="sxs-lookup"><span data-stu-id="4dbf0-127">-Overwrite</span></span>
<span data-ttu-id="4dbf0-128">**PSPrivateDnsVirtualNetworkLink** 개체(파이프라인 또는 링크 매개 변수를 통해  전달)를 사용하여 영역을 지정할 때 로컬 **PSPrivateDnsVirtualNetworkLink** 개체가 검색된 이후 Azure DNS에서 영역이 변경된 경우 해당 영역은 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="4dbf0-129">그러면 동시 영역 변경에 대한 보호가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="4dbf0-130">이는 덮어 덮어 사용 매개 변수를 사용하여 억제할 수 있습니다. 이는 동시 변경 내용에 관계없이 영역이 삭제됩니다. </span><span class="sxs-lookup"><span data-stu-id="4dbf0-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="4dbf0-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4dbf0-131">-PassThru</span></span>
<span data-ttu-id="4dbf0-132">작업 삭제 가상 네트워크 링크의 결과(부울)를 파이프라인 아래로 전달하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="4dbf0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dbf0-133">-ResourceGroupName</span></span>
<span data-ttu-id="4dbf0-134">제거할 링크가 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="4dbf0-135">*ZoneName* 및 Name 매개 변수도 *지정해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="4dbf0-136">또는 파이프라인 또는 링크 매개 변수를 통해 전달된 **PSPrivateDnsVirtualNetworkLink** 개체를 사용하여 DNS 지역을 지정할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="4dbf0-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4dbf0-137">-ResourceId</span></span>
<span data-ttu-id="4dbf0-138">링크의 ARM 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-138">Specifies the ARM resource ID of the link.</span></span>

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

### <span data-ttu-id="4dbf0-139">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="4dbf0-139">-ZoneName</span></span>
<span data-ttu-id="4dbf0-140">링크가 연결된 개인 DNS 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="4dbf0-141">*ResourceGroupName 및 Name* 매개 변수도 *지정해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="4dbf0-142">또는 링크 매개 변수를 사용하여 링크를 지정할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="4dbf0-143">-확인</span><span class="sxs-lookup"><span data-stu-id="4dbf0-143">-Confirm</span></span>
<span data-ttu-id="4dbf0-144">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dbf0-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dbf0-145">-WhatIf</span></span>
<span data-ttu-id="4dbf0-146">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dbf0-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dbf0-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dbf0-148">CommonParameters</span></span>
<span data-ttu-id="4dbf0-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dbf0-150">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4dbf0-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dbf0-151">입력</span><span class="sxs-lookup"><span data-stu-id="4dbf0-151">INPUTS</span></span>

### <span data-ttu-id="4dbf0-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4dbf0-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="4dbf0-153">System.String</span><span class="sxs-lookup"><span data-stu-id="4dbf0-153">System.String</span></span>

## <span data-ttu-id="4dbf0-154">출력</span><span class="sxs-lookup"><span data-stu-id="4dbf0-154">OUTPUTS</span></span>

### <span data-ttu-id="4dbf0-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4dbf0-155">System.Boolean</span></span>

## <span data-ttu-id="4dbf0-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4dbf0-156">NOTES</span></span>

## <span data-ttu-id="4dbf0-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4dbf0-157">RELATED LINKS</span></span>

[<span data-ttu-id="4dbf0-158">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4dbf0-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="4dbf0-159">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4dbf0-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="4dbf0-160">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="4dbf0-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
