---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 60da913ea7743be288e58eee9e4840c15e4818b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202129"
---
# <span data-ttu-id="f60ec-101">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f60ec-101">Get-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="f60ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f60ec-102">SYNOPSIS</span></span>
<span data-ttu-id="f60ec-103">지정된 개인 DNS 영역과 연결된 가상 네트워크 링크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f60ec-103">Gets a virtual network link associated with the specified Private DNS zone.</span></span>

## <span data-ttu-id="f60ec-104">구문</span><span class="sxs-lookup"><span data-stu-id="f60ec-104">SYNTAX</span></span>

```
Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f60ec-105">설명</span><span class="sxs-lookup"><span data-stu-id="f60ec-105">DESCRIPTION</span></span>
<span data-ttu-id="f60ec-106">**Get-AzPrivateDnsVirtualNetworkLink** cmdlet은 지정된 리소스 그룹에서 특정 개인 DNS 영역과 연결된 가상 네트워크 링크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f60ec-106">The **Get-AzPrivateDnsVirtualNetworkLink** cmdlet gets virtual network links associated with a particular Private DNS zone from the specified resource group.</span></span>
<span data-ttu-id="f60ec-107">Name 매개 *변수를 지정하면* 단일 **PSPrivateDnsVirtualNetworkLink 개체가** 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="f60ec-107">If you specify the *Name* parameter, a single **PSPrivateDnsVirtualNetworkLink** object is returned.</span></span>
<span data-ttu-id="f60ec-108">이름 매개 변수를  지정하지 않으면 지정된 리소스 그룹의 영역과 연결된 모든 링크를 포함하는 배열이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="f60ec-108">If you do not specify the *Name* parameter, an array containing all of the links associated with the zone in the specified resource group is returned.</span></span>
<span data-ttu-id="f60ec-109">**PSPrivateDnsVirtualNetworkLink** 개체를 사용하여 링크를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f60ec-109">You can use the **PSPrivateDnsVirtualNetworkLink** object to update the link.</span></span>

## <span data-ttu-id="f60ec-110">예제</span><span class="sxs-lookup"><span data-stu-id="f60ec-110">EXAMPLES</span></span>

### <span data-ttu-id="f60ec-111">예제 1: 가상 네트워크 링크 다운로드</span><span class="sxs-lookup"><span data-stu-id="f60ec-111">Example 1: Get a virtual network link.</span></span>
```
PS C:\> $Link = Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"

The link object returned looks like the following:

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="f60ec-112">이 예제에서는 지정된 리소스 그룹에서 myzone.com 개인 DNS 영역과 연결된 가상 네트워크 링크 mylink를 $Link 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f60ec-112">This example gets the virtual network link mylink associated with the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Link variable.</span></span>

### <span data-ttu-id="f60ec-113">예제 2: 리소스 그룹의 영역과 연결된 모든 링크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f60ec-113">Example 2: Get all of the links associated with a zone in a resource group.</span></span>
```
PS C:\> $Links = Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"

Name                    : mylink1
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink1
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded

Name                    : mylink2
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink2
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="f60ec-114">이 예제에서는 지정된 리소스 그룹의 개인 DNS 영역 "myzone.com"와 연결된 모든 가상 네트워크 링크를 찾은 다음 $Links 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f60ec-114">This example gets all of the virtual network links associated with the Private DNS zone "myzone.com" in the specified resource group, and then stores it in the $Links variable.</span></span>

## <span data-ttu-id="f60ec-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f60ec-115">PARAMETERS</span></span>

### <span data-ttu-id="f60ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f60ec-116">-DefaultProfile</span></span>
<span data-ttu-id="f60ec-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f60ec-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f60ec-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f60ec-118">-Name</span></span>
<span data-ttu-id="f60ec-119">얻을 가상 네트워크 링크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f60ec-119">Specifies the name of the virtual network link to get.</span></span>
<span data-ttu-id="f60ec-120">Name 매개 변수에 대한  값을 지정하지 않으면 이 cmdlet은 지정된 리소스 그룹의 지정된 개인 DNS 영역과 연결된 모든 링크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f60ec-120">If you do not specify a value for the *Name* parameter, this cmdlet gets all links associated with the specified Private DNS zone in the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f60ec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f60ec-121">-ResourceGroupName</span></span>
<span data-ttu-id="f60ec-122">얻을 가상 네트워크 링크가 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f60ec-122">Specifies the name of the resource group that contains the virtual network link to get.</span></span>

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

### <span data-ttu-id="f60ec-123">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="f60ec-123">-ZoneName</span></span>
<span data-ttu-id="f60ec-124">가상 네트워크 링크가 연결된 개인 DNS 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f60ec-124">Specifies the name of the Private DNS zone that the virtual network link is linked to.</span></span>


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

### <span data-ttu-id="f60ec-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f60ec-125">CommonParameters</span></span>
<span data-ttu-id="f60ec-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f60ec-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f60ec-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f60ec-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f60ec-128">입력</span><span class="sxs-lookup"><span data-stu-id="f60ec-128">INPUTS</span></span>

### <span data-ttu-id="f60ec-129">없음</span><span class="sxs-lookup"><span data-stu-id="f60ec-129">None</span></span>

## <span data-ttu-id="f60ec-130">출력</span><span class="sxs-lookup"><span data-stu-id="f60ec-130">OUTPUTS</span></span>

### <span data-ttu-id="f60ec-131">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f60ec-131">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="f60ec-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f60ec-132">NOTES</span></span>

## <span data-ttu-id="f60ec-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f60ec-133">RELATED LINKS</span></span>

[<span data-ttu-id="f60ec-134">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f60ec-134">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="f60ec-135">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f60ec-135">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="f60ec-136">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="f60ec-136">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
