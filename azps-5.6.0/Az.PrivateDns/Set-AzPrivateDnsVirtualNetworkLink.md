---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 1e1fa3709e597d220ba8269856f562a8ad8c3bd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985726"
---
# <span data-ttu-id="ecce4-101">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ecce4-101">Set-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="ecce4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecce4-102">SYNOPSIS</span></span>
<span data-ttu-id="ecce4-103">개인 영역 및 리소스 그룹과 연결된 가상 네트워크 링크를 업데이트/설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-103">Updates/Sets a virtual network link associated with a private zone and a resource group.</span></span>

## <span data-ttu-id="ecce4-104">구문</span><span class="sxs-lookup"><span data-stu-id="ecce4-104">SYNTAX</span></span>

### <span data-ttu-id="ecce4-105">필드(기본값)</span><span class="sxs-lookup"><span data-stu-id="ecce4-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecce4-106">개체</span><span class="sxs-lookup"><span data-stu-id="ecce4-106">Object</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecce4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecce4-107">ResourceId</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecce4-108">설명</span><span class="sxs-lookup"><span data-stu-id="ecce4-108">DESCRIPTION</span></span>
<span data-ttu-id="ecce4-109">**Set-AzPrivateDnsVirtualNetworkLink** cmdlet은 지정된 리소스 그룹의 영역과 연결된 링크를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-109">The **Set-AzPrivateDnsVirtualNetworkLink** cmdlet updates a link associated with a zone from a specified resource group.</span></span>
<span data-ttu-id="ecce4-110">링크 매개 변수를 사용하여 **PSPrivateDnsVirtualNetworkLink** 개체를 전달하거나 파이프라인 연산자를 사용하여 전달하거나 이름  *영역* 이름 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다. </span><span class="sxs-lookup"><span data-stu-id="ecce4-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="ecce4-111">확인 매개 변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ecce4-112">**PSPrivateDnsVirtualNetworkLink** 개체(파이프라인 또는 링크 매개 변수를 통해  전달)를 사용하여 영역을 지정할 때 로컬 **PSPrivateDnsVirtualNetworkLink** 개체가 검색된 이후 Azure DNS에서 변경된 경우 링크가 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-112">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not updated if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="ecce4-113">그러면 동시 링크 변경에 대한 보호가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-113">This provides protection for concurrent link changes.</span></span> <span data-ttu-id="ecce4-114">이는 덮어 덮어 사용 매개 변수를 사용하여 억제할 수 있습니다. 이는 동시 변경 내용에 관계없이 링크를 업데이트합니다. </span><span class="sxs-lookup"><span data-stu-id="ecce4-114">This can be suppressed using the *Overwrite* parameter, which updates the link regardless of concurrent changes.</span></span>

## <span data-ttu-id="ecce4-115">예제</span><span class="sxs-lookup"><span data-stu-id="ecce4-115">EXAMPLES</span></span>

### <span data-ttu-id="ecce4-116">예제 1: 링크 설정</span><span class="sxs-lookup"><span data-stu-id="ecce4-116">Example 1: Set a link</span></span>
```
PS C:\>Set-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -Tag @{} -IsRegistrationEnabled $true

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="ecce4-117">이 명령은 MyResourceGroup이라는 리소스 그룹에서 myzone.com 명명된 영역과 연결된 mylink라는 링크에 대해 IsRegistrationEnabled를 True로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-117">This command sets IsRegistrationEnabled to True for the link named mylink, linked to zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="ecce4-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ecce4-118">PARAMETERS</span></span>

### <span data-ttu-id="ecce4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecce4-119">-DefaultProfile</span></span>
<span data-ttu-id="ecce4-120">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ecce4-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecce4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecce4-121">-InputObject</span></span>
<span data-ttu-id="ecce4-122">설정할 가상 네트워크 링크 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-122">The virtual network link object to set.</span></span>

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

### <span data-ttu-id="ecce4-123">-IsRegistrationEnabled</span><span class="sxs-lookup"><span data-stu-id="ecce4-123">-IsRegistrationEnabled</span></span>
<span data-ttu-id="ecce4-124">가상 네트워크 링크에서 등록이 활성화되어 있는 경우를 나타내는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-124">Boolean that represents if registration is enabled on the virtual network link.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecce4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ecce4-125">-Name</span></span>
<span data-ttu-id="ecce4-126">이 cmdlet이 제거한 링크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-126">Specifies the name of the link that this cmdlet removes.</span></span>
<span data-ttu-id="ecce4-127">*ResourceGroupName* 및 *ZoneName 매개 변수도 지정해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-127">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="ecce4-128">또는 링크 매개 변수를 사용하여 개인 DNS 링크를 지정할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-128">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="ecce4-129">-덮어 덮어 덮어 덮어 덮어</span><span class="sxs-lookup"><span data-stu-id="ecce4-129">-Overwrite</span></span>
<span data-ttu-id="ecce4-130">**PSPrivateDnsVirtualNetworkLink** 개체를 사용하여 링크를 지정할 때(파이프라인 또는  링크 매개 변수를 통해 전달) 로컬 **PSPrivateDnsVirtualNetworkLink** 개체가 검색된 이후 Azure DNS에서 변경된 경우 링크가 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-130">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="ecce4-131">그러면 동시 링크 변경에 대한 보호가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-131">This provides protection for concurrent link changes.</span></span>
<span data-ttu-id="ecce4-132">이는 덮어 덮어 사용 매개 변수를 사용하여 억제될 수 있습니다. 이는 동시 변경 내용에 관계없이 링크를 삭제합니다. </span><span class="sxs-lookup"><span data-stu-id="ecce4-132">This can be suppressed using the *Overwrite* parameter, which deletes the link regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="ecce4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecce4-133">-ResourceGroupName</span></span>
<span data-ttu-id="ecce4-134">제거할 링크가 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="ecce4-135">*ZoneName* 및 Name 매개 변수도 *지정해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="ecce4-136">또는 파이프라인 또는 링크 매개 변수를 통해 전달된 **PSPrivateDnsVirtualNetworkLink** 개체를 사용하여 가상 네트워크 링크를 지정할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-136">Alternatively, you can specify the virtual network link using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="ecce4-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecce4-137">-ResourceId</span></span>
<span data-ttu-id="ecce4-138">개인 DNS 영역 ResourceID.</span><span class="sxs-lookup"><span data-stu-id="ecce4-138">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="ecce4-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="ecce4-139">-Tag</span></span>
<span data-ttu-id="ecce4-140">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="ecce4-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="ecce4-141">-ZoneName</span></span>
<span data-ttu-id="ecce4-142">이 cmdlet이 제거한 DNS 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-142">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="ecce4-143">이름 및 *ResourceGroupName 매개 변수도 지정해야* 합니다. </span><span class="sxs-lookup"><span data-stu-id="ecce4-143">You must also specify the *Name* and *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="ecce4-144">또는 링크 매개 변수를 사용하여 개인 DNS 링크를 지정할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-144">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="ecce4-145">-확인</span><span class="sxs-lookup"><span data-stu-id="ecce4-145">-Confirm</span></span>
<span data-ttu-id="ecce4-146">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecce4-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecce4-147">-WhatIf</span></span>
<span data-ttu-id="ecce4-148">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecce4-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecce4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecce4-150">CommonParameters</span></span>
<span data-ttu-id="ecce4-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ecce4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecce4-152">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ecce4-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecce4-153">입력</span><span class="sxs-lookup"><span data-stu-id="ecce4-153">INPUTS</span></span>

### <span data-ttu-id="ecce4-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ecce4-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="ecce4-155">System.String</span><span class="sxs-lookup"><span data-stu-id="ecce4-155">System.String</span></span>

## <span data-ttu-id="ecce4-156">출력</span><span class="sxs-lookup"><span data-stu-id="ecce4-156">OUTPUTS</span></span>

### <span data-ttu-id="ecce4-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ecce4-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="ecce4-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ecce4-158">NOTES</span></span>

## <span data-ttu-id="ecce4-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecce4-159">RELATED LINKS</span></span>

[<span data-ttu-id="ecce4-160">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ecce4-160">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="ecce4-161">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ecce4-161">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="ecce4-162">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="ecce4-162">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
