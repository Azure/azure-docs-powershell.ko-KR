---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/powershell/module/az.privatedns/New-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 18a5f55f458bf1c16ac090237d876dd2e8f7d3ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965568"
---
# <span data-ttu-id="85835-101">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="85835-101">New-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="85835-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85835-102">SYNOPSIS</span></span>
<span data-ttu-id="85835-103">새 개인 DNS 가상 네트워크 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="85835-103">Creates a new private DNS virtual network link.</span></span>

## <span data-ttu-id="85835-104">구문</span><span class="sxs-lookup"><span data-stu-id="85835-104">SYNTAX</span></span>

### <span data-ttu-id="85835-105">VirtualNetworkId(기본값)</span><span class="sxs-lookup"><span data-stu-id="85835-105">VirtualNetworkId (Default)</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85835-106">VirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="85835-106">VirtualNetworkObject</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetwork <VirtualNetwork> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85835-107">RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="85835-107">RemoteVirtualNetworkId</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85835-108">설명</span><span class="sxs-lookup"><span data-stu-id="85835-108">DESCRIPTION</span></span>
<span data-ttu-id="85835-109">**New-AzPrivateDnsVirtualNetworkLink** cmdlet은 지정된 리소스 그룹 및 개인 영역의 새 DNS(개인 도메인 이름 시스템) 가상 네트워크 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="85835-109">The **New-AzPrivateDnsVirtualNetworkLink** cmdlet creates a new private Domain Name System (DNS) virtual network link in the specified resource group and private zone.</span></span> <span data-ttu-id="85835-110">이름 매개 변수에 대한  고유한 링크 이름을 지정해야 합니다. 또는 cmdlet에서 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="85835-110">You must specify a unique link name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="85835-111">확인 매개  변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85835-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="85835-112">예제</span><span class="sxs-lookup"><span data-stu-id="85835-112">EXAMPLES</span></span>

### <span data-ttu-id="85835-113">예제 1: 개인 DNS 가상 네트워크 링크 만들기</span><span class="sxs-lookup"><span data-stu-id="85835-113">Example 1: Create a Private DNS virtual network link</span></span>
```
PS C:\>$Link = New-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -VirtualNetworkId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork" -EnableRegistration

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

<span data-ttu-id="85835-114">이 명령은 지정된 리소스 그룹에서 myzone.com "myvirtualnetwork"(리소스 그룹에 이미 만들어진)라는 개인 DNS 영역과 연결된 새 가상 네트워크 $Link 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="85835-114">This command creates a new virtual network link associated with the private DNS zone named myzone.com and virtual network "myvirtualnetwork" (which has already been created in the resource group) in the specified resource group, and then stores it in the $Link variable.</span></span>

## <span data-ttu-id="85835-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="85835-115">PARAMETERS</span></span>

### <span data-ttu-id="85835-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85835-116">-DefaultProfile</span></span>
<span data-ttu-id="85835-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="85835-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85835-118">-EnableRegistration</span><span class="sxs-lookup"><span data-stu-id="85835-118">-EnableRegistration</span></span>
<span data-ttu-id="85835-119">링크가 등록을 사용하도록 설정되어 있는 경우를 나타내는 스위치 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="85835-119">Switch parameter that represents if the link is registration enabled or not.</span></span>

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

### <span data-ttu-id="85835-120">-Name</span><span class="sxs-lookup"><span data-stu-id="85835-120">-Name</span></span>
<span data-ttu-id="85835-121">만들 가상 네트워크 링크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="85835-121">Specifies the name of the virtual network link to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85835-122">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="85835-122">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="85835-123">다른 테넌트의 가상 네트워크의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="85835-123">The resource id of the virtual network in another tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoteVirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85835-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85835-124">-ResourceGroupName</span></span>
<span data-ttu-id="85835-125">링크를 만들 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="85835-125">Specifies the resource group in which to create the link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85835-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="85835-126">-Tag</span></span>
<span data-ttu-id="85835-127">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="85835-127">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="85835-128">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="85835-128">-VirtualNetwork</span></span>
<span data-ttu-id="85835-129">링크와 연결된 가상 네트워크 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="85835-129">The virtual network object associated with the link.</span></span>

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IVirtualNetwork
Parameter Sets: VirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85835-130">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="85835-130">-VirtualNetworkId</span></span>
<span data-ttu-id="85835-131">링크와 연결된 가상 네트워크의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="85835-131">The resource id of the virtual network associated with the link.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85835-132">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="85835-132">-ZoneName</span></span>
<span data-ttu-id="85835-133">가상 네트워크 링크에 연결된 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="85835-133">Specifies the name of the zone which will be linked to the virtual network link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85835-134">-확인</span><span class="sxs-lookup"><span data-stu-id="85835-134">-Confirm</span></span>
<span data-ttu-id="85835-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="85835-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85835-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85835-136">-WhatIf</span></span>
<span data-ttu-id="85835-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="85835-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85835-138">cmdlet이 실행되지 않습니다. cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="85835-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85835-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85835-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85835-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85835-140">CommonParameters</span></span>
<span data-ttu-id="85835-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="85835-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85835-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85835-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85835-143">입력</span><span class="sxs-lookup"><span data-stu-id="85835-143">INPUTS</span></span>

### <span data-ttu-id="85835-144">없음</span><span class="sxs-lookup"><span data-stu-id="85835-144">None</span></span>

## <span data-ttu-id="85835-145">출력</span><span class="sxs-lookup"><span data-stu-id="85835-145">OUTPUTS</span></span>

### <span data-ttu-id="85835-146">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="85835-146">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="85835-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="85835-147">NOTES</span></span>

## <span data-ttu-id="85835-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85835-148">RELATED LINKS</span></span>

[<span data-ttu-id="85835-149">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="85835-149">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="85835-150">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="85835-150">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="85835-151">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="85835-151">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)
