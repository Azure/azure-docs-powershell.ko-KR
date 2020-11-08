---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 3ffcc30dc0291be06c27ee53ee0ee7ea14f3e2c1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034465"
---
# <span data-ttu-id="67f6a-101">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="67f6a-101">Set-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="67f6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67f6a-102">SYNOPSIS</span></span>
<span data-ttu-id="67f6a-103">개인 영역 및 리소스 그룹과 연결 된 가상 네트워크 링크를 업데이트/설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-103">Updates/Sets a virtual network link associated with a private zone and a resource group.</span></span>

## <span data-ttu-id="67f6a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67f6a-104">SYNTAX</span></span>

### <span data-ttu-id="67f6a-105">필드 (기본값)</span><span class="sxs-lookup"><span data-stu-id="67f6a-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67f6a-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="67f6a-106">Object</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67f6a-107">리소스</span><span class="sxs-lookup"><span data-stu-id="67f6a-107">ResourceId</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67f6a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="67f6a-108">DESCRIPTION</span></span>
<span data-ttu-id="67f6a-109">**Set-AzPrivateDnsVirtualNetworkLink** cmdlet은 지정 된 리소스 그룹의 영역과 연결 된 링크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-109">The **Set-AzPrivateDnsVirtualNetworkLink** cmdlet updates a link associated with a zone from a specified resource group.</span></span>
<span data-ttu-id="67f6a-110">*Link* 매개 변수를 사용 하거나 파이프라인 연산자를 사용 하 여 **PSPrivateDnsVirtualNetworkLink** 개체를 전달 하거나 *이름* *ZoneName* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="67f6a-111">확인 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="67f6a-112">**PSPrivateDnsVirtualNetworkLink** 개체 (파이프라인 또는 *링크* 매개 변수를 통해 전달)를 사용 하 여 영역을 지정 하는 경우 로컬 **PSPrivateDnsVirtualNetworkLink** 개체가 검색 된 이후 Azure DNS에서 변경 된 링크가 업데이트 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-112">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not updated if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="67f6a-113">이는 동시 링크 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-113">This provides protection for concurrent link changes.</span></span> <span data-ttu-id="67f6a-114">이는 *덮어쓰기* 매개 변수를 사용 하 여 억제할 수 있으며, 동시 변경에 관계 없이 링크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-114">This can be suppressed using the *Overwrite* parameter, which updates the link regardless of concurrent changes.</span></span>

## <span data-ttu-id="67f6a-115">예제의</span><span class="sxs-lookup"><span data-stu-id="67f6a-115">EXAMPLES</span></span>

### <span data-ttu-id="67f6a-116">예제 1: 링크 설정</span><span class="sxs-lookup"><span data-stu-id="67f6a-116">Example 1: Set a link</span></span>
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

<span data-ttu-id="67f6a-117">이 명령은 Mylink 이라는 리소스 그룹의 myzone.com 이라는 영역에 연결 된 mylink 링크에 대해 IsRegistrationEnabled를 True로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-117">This command sets IsRegistrationEnabled to True for the link named mylink, linked to zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="67f6a-118">변수</span><span class="sxs-lookup"><span data-stu-id="67f6a-118">PARAMETERS</span></span>

### <span data-ttu-id="67f6a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f6a-119">-DefaultProfile</span></span>
<span data-ttu-id="67f6a-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="67f6a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67f6a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67f6a-121">-InputObject</span></span>
<span data-ttu-id="67f6a-122">설정할 가상 네트워크 링크 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-122">The virtual network link object to set.</span></span>

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

### <span data-ttu-id="67f6a-123">-IsRegistrationEnabled</span><span class="sxs-lookup"><span data-stu-id="67f6a-123">-IsRegistrationEnabled</span></span>
<span data-ttu-id="67f6a-124">가상 네트워크 링크에서 등록을 사용할 수 있는지 여부를 나타내는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-124">Boolean that represents if registration is enabled on the virtual network link.</span></span>

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

### <span data-ttu-id="67f6a-125">-이름</span><span class="sxs-lookup"><span data-stu-id="67f6a-125">-Name</span></span>
<span data-ttu-id="67f6a-126">이 cmdlet이 제거 하는 링크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-126">Specifies the name of the link that this cmdlet removes.</span></span>
<span data-ttu-id="67f6a-127">또한 *ResourceGroupName* 및 *ZoneName* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-127">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="67f6a-128">또는 *링크* 매개 변수를 사용 하 여 개인 DNS 링크를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-128">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="67f6a-129">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="67f6a-129">-Overwrite</span></span>
<span data-ttu-id="67f6a-130">**PSPrivateDnsVirtualNetworkLink** 개체 (파이프라인 또는 *링크* 매개 변수를 통해 전달)를 사용 하 여 링크를 지정 하는 경우 로컬 **PSPrivateDnsVirtualNetworkLink** 개체가 검색 된 이후 Azure DNS에서 변경 된 링크가 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-130">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="67f6a-131">이는 동시 링크 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-131">This provides protection for concurrent link changes.</span></span>
<span data-ttu-id="67f6a-132">이는 *덮어쓰기* 매개 변수를 사용 하 여 억제할 수 있으며,이는 동시 변경에 관계 없이 링크를 삭제 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-132">This can be suppressed using the *Overwrite* parameter, which deletes the link regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="67f6a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67f6a-133">-ResourceGroupName</span></span>
<span data-ttu-id="67f6a-134">제거할 링크가 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="67f6a-135">*ZoneName* 및 *Name* 매개 변수도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="67f6a-136">또는 파이프라인 또는 *링크* 매개 변수를 통해 전달 되는 **PSPrivateDnsVirtualNetworkLink** 개체를 사용 하 여 가상 네트워크 링크를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-136">Alternatively, you can specify the virtual network link using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="67f6a-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67f6a-137">-ResourceId</span></span>
<span data-ttu-id="67f6a-138">개인 DNS 영역 ResourceID</span><span class="sxs-lookup"><span data-stu-id="67f6a-138">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="67f6a-139">태그</span><span class="sxs-lookup"><span data-stu-id="67f6a-139">-Tag</span></span>
<span data-ttu-id="67f6a-140">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="67f6a-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="67f6a-141">-ZoneName</span></span>
<span data-ttu-id="67f6a-142">이 cmdlet이 제거 하는 DNS 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-142">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="67f6a-143">또한 *Name* 및 *ResourceGroupName* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-143">You must also specify the *Name* and *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="67f6a-144">또는 *링크* 매개 변수를 사용 하 여 개인 DNS 링크를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-144">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="67f6a-145">-확인</span><span class="sxs-lookup"><span data-stu-id="67f6a-145">-Confirm</span></span>
<span data-ttu-id="67f6a-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67f6a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67f6a-147">-WhatIf</span></span>
<span data-ttu-id="67f6a-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67f6a-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67f6a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f6a-150">CommonParameters</span></span>
<span data-ttu-id="67f6a-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67f6a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f6a-152">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67f6a-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f6a-153">입력</span><span class="sxs-lookup"><span data-stu-id="67f6a-153">INPUTS</span></span>

### <span data-ttu-id="67f6a-154">PrivateDns. PSPrivateDnsVirtualNetworkLink/.</span><span class="sxs-lookup"><span data-stu-id="67f6a-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="67f6a-155">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="67f6a-155">System.String</span></span>

## <span data-ttu-id="67f6a-156">출력</span><span class="sxs-lookup"><span data-stu-id="67f6a-156">OUTPUTS</span></span>

### <span data-ttu-id="67f6a-157">PrivateDns. PSPrivateDnsVirtualNetworkLink/.</span><span class="sxs-lookup"><span data-stu-id="67f6a-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="67f6a-158">상속자</span><span class="sxs-lookup"><span data-stu-id="67f6a-158">NOTES</span></span>

## <span data-ttu-id="67f6a-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67f6a-159">RELATED LINKS</span></span>

[<span data-ttu-id="67f6a-160">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="67f6a-160">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="67f6a-161">새로운 AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="67f6a-161">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="67f6a-162">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="67f6a-162">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)