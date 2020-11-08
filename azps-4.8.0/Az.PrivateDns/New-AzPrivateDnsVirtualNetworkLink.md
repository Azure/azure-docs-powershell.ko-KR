---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/New-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: be1480b68c4b0fd66328a7ff417517ee86cb88df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214266"
---
# <span data-ttu-id="0f680-101">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="0f680-101">New-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="0f680-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f680-102">SYNOPSIS</span></span>
<span data-ttu-id="0f680-103">새 개인 DNS 가상 네트워크 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0f680-103">Creates a new private DNS virtual network link.</span></span>

## <span data-ttu-id="0f680-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0f680-104">SYNTAX</span></span>

### <span data-ttu-id="0f680-105">VirtualNetworkId (기본값)</span><span class="sxs-lookup"><span data-stu-id="0f680-105">VirtualNetworkId (Default)</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f680-106">VirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="0f680-106">VirtualNetworkObject</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetwork <VirtualNetwork> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f680-107">RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="0f680-107">RemoteVirtualNetworkId</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f680-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0f680-108">DESCRIPTION</span></span>
<span data-ttu-id="0f680-109">**AzPrivateDnsVirtualNetworkLink** cmdlet은 지정 된 리소스 그룹 및 개인 영역에 새 DNS (개인 도메인 이름 시스템) 가상 네트워크 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0f680-109">The **New-AzPrivateDnsVirtualNetworkLink** cmdlet creates a new private Domain Name System (DNS) virtual network link in the specified resource group and private zone.</span></span> <span data-ttu-id="0f680-110">*Name* 매개 변수에 대해 고유한 링크 이름을 지정 해야 하며, cmdlet에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f680-110">You must specify a unique link name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="0f680-111">*확인* 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0f680-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="0f680-112">예제의</span><span class="sxs-lookup"><span data-stu-id="0f680-112">EXAMPLES</span></span>

### <span data-ttu-id="0f680-113">예제 1: 개인 DNS 가상 네트워크 링크 만들기</span><span class="sxs-lookup"><span data-stu-id="0f680-113">Example 1: Create a Private DNS virtual network link</span></span>
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

<span data-ttu-id="0f680-114">이 명령은 지정 된 리소스 그룹에서 myzone.com 및 가상 네트워크 "myvirtualnetwork" (리소스 그룹에 이미 생성 된) 이라는 개인 DNS 영역과 연결 된 새 가상 네트워크 링크를 만든 다음이를 $Link 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f680-114">This command creates a new virtual network link associated with the private DNS zone named myzone.com and virtual network "myvirtualnetwork" (which has already been created in the resource group) in the specified resource group, and then stores it in the $Link variable.</span></span>

## <span data-ttu-id="0f680-115">변수</span><span class="sxs-lookup"><span data-stu-id="0f680-115">PARAMETERS</span></span>

### <span data-ttu-id="0f680-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f680-116">-DefaultProfile</span></span>
<span data-ttu-id="0f680-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0f680-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f680-118">-EnableRegistration</span><span class="sxs-lookup"><span data-stu-id="0f680-118">-EnableRegistration</span></span>
<span data-ttu-id="0f680-119">링크가 등록 되었는지 여부를 나타내는 Switch 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="0f680-119">Switch parameter that represents if the link is registration enabled or not.</span></span>

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

### <span data-ttu-id="0f680-120">-이름</span><span class="sxs-lookup"><span data-stu-id="0f680-120">-Name</span></span>
<span data-ttu-id="0f680-121">만들 가상 네트워크 링크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f680-121">Specifies the name of the virtual network link to create.</span></span>

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

### <span data-ttu-id="0f680-122">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="0f680-122">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="0f680-123">다른 테 넌 트에 있는 가상 네트워크의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="0f680-123">The resource id of the virtual network in another tenant.</span></span>

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

### <span data-ttu-id="0f680-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f680-124">-ResourceGroupName</span></span>
<span data-ttu-id="0f680-125">링크를 만들 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f680-125">Specifies the resource group in which to create the link.</span></span>

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

### <span data-ttu-id="0f680-126">태그</span><span class="sxs-lookup"><span data-stu-id="0f680-126">-Tag</span></span>
<span data-ttu-id="0f680-127">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="0f680-127">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="0f680-128">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0f680-128">-VirtualNetwork</span></span>
<span data-ttu-id="0f680-129">링크와 연결 된 가상 네트워크 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0f680-129">The virtual network object associated with the link.</span></span>

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

### <span data-ttu-id="0f680-130">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="0f680-130">-VirtualNetworkId</span></span>
<span data-ttu-id="0f680-131">링크와 연결 된 가상 네트워크의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="0f680-131">The resource id of the virtual network associated with the link.</span></span>

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

### <span data-ttu-id="0f680-132">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="0f680-132">-ZoneName</span></span>
<span data-ttu-id="0f680-133">가상 네트워크 링크에 연결 될 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f680-133">Specifies the name of the zone which will be linked to the virtual network link.</span></span>

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

### <span data-ttu-id="0f680-134">-확인</span><span class="sxs-lookup"><span data-stu-id="0f680-134">-Confirm</span></span>
<span data-ttu-id="0f680-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f680-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f680-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f680-136">-WhatIf</span></span>
<span data-ttu-id="0f680-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0f680-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f680-138">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0f680-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f680-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f680-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f680-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f680-140">CommonParameters</span></span>
<span data-ttu-id="0f680-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f680-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f680-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0f680-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f680-143">입력</span><span class="sxs-lookup"><span data-stu-id="0f680-143">INPUTS</span></span>

### <span data-ttu-id="0f680-144">않아야</span><span class="sxs-lookup"><span data-stu-id="0f680-144">None</span></span>

## <span data-ttu-id="0f680-145">출력</span><span class="sxs-lookup"><span data-stu-id="0f680-145">OUTPUTS</span></span>

### <span data-ttu-id="0f680-146">PrivateDns. PSPrivateDnsVirtualNetworkLink/.</span><span class="sxs-lookup"><span data-stu-id="0f680-146">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="0f680-147">상속자</span><span class="sxs-lookup"><span data-stu-id="0f680-147">NOTES</span></span>

## <span data-ttu-id="0f680-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f680-148">RELATED LINKS</span></span>

[<span data-ttu-id="0f680-149">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="0f680-149">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="0f680-150">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="0f680-150">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="0f680-151">제거-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="0f680-151">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)
