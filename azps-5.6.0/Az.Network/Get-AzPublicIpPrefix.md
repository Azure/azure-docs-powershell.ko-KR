---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: 6083c87ddf0bd7b2306fdacc6d109ccebc144faa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954107"
---
# <span data-ttu-id="82bd3-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="82bd3-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="82bd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="82bd3-103">공용 IP 연결부를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82bd3-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="82bd3-104">구문</span><span class="sxs-lookup"><span data-stu-id="82bd3-104">SYNTAX</span></span>

### <span data-ttu-id="82bd3-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="82bd3-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82bd3-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82bd3-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82bd3-107">설명</span><span class="sxs-lookup"><span data-stu-id="82bd3-107">DESCRIPTION</span></span>
<span data-ttu-id="82bd3-108">**Get-AzPublicIpPrefix** cmdlet은 리소스 그룹에서 하나 이상의 공용 IP 프리픽스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82bd3-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="82bd3-109">예제</span><span class="sxs-lookup"><span data-stu-id="82bd3-109">EXAMPLES</span></span>

### <span data-ttu-id="82bd3-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="82bd3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myPublicIpPrefix1

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard",
                           "Tier":"Regional"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="82bd3-111">이 명령은 리소스 그룹 myRg에서 myPublicIpPrefix1을 사용하여 공용 IP 강두사 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82bd3-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="82bd3-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="82bd3-112">Example 2</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -Name myPublicIpPrefix*

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard",
                           "Tier": "Regional"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="82bd3-113">이 명령은 myPublicIpPrefix로 시작하는 모든 공용 IP 프리픽스 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="82bd3-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="82bd3-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="82bd3-114">PARAMETERS</span></span>

### <span data-ttu-id="82bd3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82bd3-115">-DefaultProfile</span></span>
<span data-ttu-id="82bd3-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82bd3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82bd3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="82bd3-117">-Name</span></span>
<span data-ttu-id="82bd3-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82bd3-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="82bd3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82bd3-119">-ResourceGroupName</span></span>
<span data-ttu-id="82bd3-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82bd3-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="82bd3-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82bd3-121">-ResourceId</span></span>
<span data-ttu-id="82bd3-122">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="82bd3-122">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82bd3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82bd3-123">CommonParameters</span></span>
<span data-ttu-id="82bd3-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82bd3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82bd3-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82bd3-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82bd3-126">입력</span><span class="sxs-lookup"><span data-stu-id="82bd3-126">INPUTS</span></span>

### <span data-ttu-id="82bd3-127">System.String</span><span class="sxs-lookup"><span data-stu-id="82bd3-127">System.String</span></span>

## <span data-ttu-id="82bd3-128">출력</span><span class="sxs-lookup"><span data-stu-id="82bd3-128">OUTPUTS</span></span>

### <span data-ttu-id="82bd3-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="82bd3-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="82bd3-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82bd3-130">NOTES</span></span>

## <span data-ttu-id="82bd3-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82bd3-131">RELATED LINKS</span></span>

[<span data-ttu-id="82bd3-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="82bd3-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="82bd3-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="82bd3-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="82bd3-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="82bd3-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
