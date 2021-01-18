---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
ms.openlocfilehash: ce9d10726cee7aa5a7416048e2e3582c8a42fd74
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496699"
---
# <span data-ttu-id="351cf-101">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="351cf-101">Get-AzCustomIpPrefix</span></span>

## <span data-ttu-id="351cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="351cf-102">SYNOPSIS</span></span>
<span data-ttu-id="351cf-103">CustomIpPrefix 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="351cf-103">Gets a CustomIpPrefix resource</span></span>

## <span data-ttu-id="351cf-104">구문</span><span class="sxs-lookup"><span data-stu-id="351cf-104">SYNTAX</span></span>

### <span data-ttu-id="351cf-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="351cf-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzCustomIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="351cf-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="351cf-106">GetByResourceIdParameterSet</span></span>
```
Get-AzCustomIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="351cf-107">설명</span><span class="sxs-lookup"><span data-stu-id="351cf-107">DESCRIPTION</span></span>
<span data-ttu-id="351cf-108">**Get-AzCustomIpPrefix** cmdlet은 입력 매개 변수 집합이 제공된 하나 이상의 CustomIpPrefixes를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="351cf-108">The **Get-AzCustomIpPrefix** cmdlet gets one or more CustomIpPrefixes given the set of input parameters</span></span>

## <span data-ttu-id="351cf-109">예제</span><span class="sxs-lookup"><span data-stu-id="351cf-109">EXAMPLES</span></span>

### <span data-ttu-id="351cf-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="351cf-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myCustomIpPrefix

Name                 : myCustomIpPrefix
ResourceGroupName    : myRg
Location             : westus
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/byoip-test-rg/providers/Micro
                       soft.Network/customIPPrefixes/testCustomIpPrefix
Etag                 : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid         : 00000000-0000-0000-0000-000000000000
ProvisioningState    : Succeeded
Tags                 :
Cidr                 : 111.111.111.111/24
CommissionedState    : Provisioning
PublicIpPrefixes     : []
Zones                : {}
```

<span data-ttu-id="351cf-111">이 명령은 리소스 그룹 myRg에서 myCustomIpPrefix라는 CustomIpPrefix 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="351cf-111">This command gets a CustomIpPrefix resource named myCustomIpPrefix in resource group myRg</span></span>

## <span data-ttu-id="351cf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="351cf-112">PARAMETERS</span></span>

### <span data-ttu-id="351cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="351cf-113">-DefaultProfile</span></span>
<span data-ttu-id="351cf-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="351cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="351cf-115">-Name</span><span class="sxs-lookup"><span data-stu-id="351cf-115">-Name</span></span>
<span data-ttu-id="351cf-116">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="351cf-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="351cf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="351cf-117">-ResourceGroupName</span></span>
<span data-ttu-id="351cf-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="351cf-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="351cf-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="351cf-119">-ResourceId</span></span>
<span data-ttu-id="351cf-120">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="351cf-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="351cf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="351cf-121">CommonParameters</span></span>
<span data-ttu-id="351cf-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="351cf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="351cf-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="351cf-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="351cf-124">입력</span><span class="sxs-lookup"><span data-stu-id="351cf-124">INPUTS</span></span>

### <span data-ttu-id="351cf-125">System.String</span><span class="sxs-lookup"><span data-stu-id="351cf-125">System.String</span></span>

## <span data-ttu-id="351cf-126">출력</span><span class="sxs-lookup"><span data-stu-id="351cf-126">OUTPUTS</span></span>

### <span data-ttu-id="351cf-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="351cf-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="351cf-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="351cf-128">NOTES</span></span>

## <span data-ttu-id="351cf-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="351cf-129">RELATED LINKS</span></span>

[<span data-ttu-id="351cf-130">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="351cf-130">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="351cf-131">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="351cf-131">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="351cf-132">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="351cf-132">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)