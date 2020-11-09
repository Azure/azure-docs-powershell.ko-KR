---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 63fbe26fa0a9ac7ca5eb985a3806886adeb2a2f8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311153"
---
# <span data-ttu-id="3a874-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="3a874-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="3a874-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a874-102">SYNOPSIS</span></span>
<span data-ttu-id="3a874-103">리소스 그룹에서 가상 네트워크 링크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="3a874-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3a874-104">SYNTAX</span></span>

### <span data-ttu-id="3a874-105">필드 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3a874-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a874-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="3a874-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a874-107">리소스</span><span class="sxs-lookup"><span data-stu-id="3a874-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a874-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3a874-108">DESCRIPTION</span></span>
<span data-ttu-id="3a874-109">**AzPrivateDnsVirtualNetworkLink** cmdlet은 지정 된 리소스 그룹에서 DNS (사설 Domain Name System) 링크를 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="3a874-110">*Link* 매개 변수를 사용 하거나 파이프라인 연산자를 사용 하 여 **PSPrivateDnsVirtualNetworkLink** 개체를 전달 하거나 *이름* *ZoneName* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="3a874-111">확인 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="3a874-112">**PSPrivateDnsVirtualNetworkLink** 개체 (파이프라인 또는 *링크* 매개 변수를 통해 전달)를 사용 하 여 링크를 지정 하는 경우 로컬 **PSPrivateDnsVirtualNetworkLink** 개체를 검색 한 후에 해당 링크가 Azure Private DNS에서 변경 된 경우에는 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="3a874-113">이는 동시 영역 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="3a874-114">이는 *덮어쓰기* 매개 변수를 사용 하 여 억제할 수 있으며, 동시 변경 내용에 관계 없이 영역이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="3a874-115">예제의</span><span class="sxs-lookup"><span data-stu-id="3a874-115">EXAMPLES</span></span>

### <span data-ttu-id="3a874-116">예제 1: 링크 제거</span><span class="sxs-lookup"><span data-stu-id="3a874-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="3a874-117">이 명령은 Mylink 이라는 리소스 그룹에서 myzone.com 영역에 연결 된 mylink 링크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="3a874-118">변수</span><span class="sxs-lookup"><span data-stu-id="3a874-118">PARAMETERS</span></span>

### <span data-ttu-id="3a874-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a874-119">-DefaultProfile</span></span>
<span data-ttu-id="3a874-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3a874-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a874-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a874-121">-InputObject</span></span>
<span data-ttu-id="3a874-122">제거할 가상 네트워크 링크 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-122">The virtual network link object to remove.</span></span>

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

### <span data-ttu-id="3a874-123">-이름</span><span class="sxs-lookup"><span data-stu-id="3a874-123">-Name</span></span>
<span data-ttu-id="3a874-124">삭제할 링크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="3a874-125">또한 *ResourceGroupName* 및 *ZoneName* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="3a874-126">또는 *link* 매개 변수를 사용 하 여 링크를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="3a874-127">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="3a874-127">-Overwrite</span></span>
<span data-ttu-id="3a874-128">**PSPrivateDnsVirtualNetworkLink** 개체 (파이프라인 또는 *링크* 매개 변수를 통해 전달)를 사용 하 여 영역을 지정 하는 경우 로컬 **PSPrivateDnsVirtualNetworkLink** 개체를 검색 한 후 Azure DNS에서 해당 영역이 변경 되 면 해당 영역은 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="3a874-129">이는 동시 영역 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="3a874-130">이는 *덮어쓰기* 매개 변수를 사용 하 여 억제할 수 있으며, 동시 변경 내용에 관계 없이 영역이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="3a874-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a874-131">-PassThru</span></span>
<span data-ttu-id="3a874-132">작업의 결과를 전달 하는 데 사용 됩니다 (부울). 파이프라인의 가상 네트워크 링크 삭제</span><span class="sxs-lookup"><span data-stu-id="3a874-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="3a874-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a874-133">-ResourceGroupName</span></span>
<span data-ttu-id="3a874-134">제거할 링크가 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="3a874-135">*ZoneName* 및 *Name* 매개 변수도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="3a874-136">또는 파이프라인 또는 *링크* 매개 변수를 통해 전달 되는 **PSPrivateDnsVirtualNetworkLink** 개체를 사용 하 여 DNS 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="3a874-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a874-137">-ResourceId</span></span>
<span data-ttu-id="3a874-138">링크의 ARM 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-138">Specifies the ARM resource ID of the link.</span></span>

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

### <span data-ttu-id="3a874-139">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="3a874-139">-ZoneName</span></span>
<span data-ttu-id="3a874-140">링크가 연결 된 개인 DNS 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="3a874-141">또한 *ResourceGroupName* 및 *Name* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="3a874-142">또는 *link* 매개 변수를 사용 하 여 링크를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="3a874-143">-확인</span><span class="sxs-lookup"><span data-stu-id="3a874-143">-Confirm</span></span>
<span data-ttu-id="3a874-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a874-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a874-145">-WhatIf</span></span>
<span data-ttu-id="3a874-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a874-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a874-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a874-148">CommonParameters</span></span>
<span data-ttu-id="3a874-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a874-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a874-150">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a874-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a874-151">입력</span><span class="sxs-lookup"><span data-stu-id="3a874-151">INPUTS</span></span>

### <span data-ttu-id="3a874-152">PrivateDns. PSPrivateDnsVirtualNetworkLink/.</span><span class="sxs-lookup"><span data-stu-id="3a874-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="3a874-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3a874-153">System.String</span></span>

## <span data-ttu-id="3a874-154">출력</span><span class="sxs-lookup"><span data-stu-id="3a874-154">OUTPUTS</span></span>

### <span data-ttu-id="3a874-155">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="3a874-155">System.Boolean</span></span>

## <span data-ttu-id="3a874-156">상속자</span><span class="sxs-lookup"><span data-stu-id="3a874-156">NOTES</span></span>

## <span data-ttu-id="3a874-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a874-157">RELATED LINKS</span></span>

[<span data-ttu-id="3a874-158">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="3a874-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="3a874-159">새로운 AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="3a874-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="3a874-160">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="3a874-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
