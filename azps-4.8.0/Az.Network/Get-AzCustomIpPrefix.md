---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
ms.openlocfilehash: ce9d10726cee7aa5a7416048e2e3582c8a42fd74
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048941"
---
# <span data-ttu-id="ad083-101">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ad083-101">Get-AzCustomIpPrefix</span></span>

## <span data-ttu-id="ad083-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad083-102">SYNOPSIS</span></span>
<span data-ttu-id="ad083-103">CustomIpPrefix 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ad083-103">Gets a CustomIpPrefix resource</span></span>

## <span data-ttu-id="ad083-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad083-104">SYNTAX</span></span>

### <span data-ttu-id="ad083-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ad083-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzCustomIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad083-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad083-106">GetByResourceIdParameterSet</span></span>
```
Get-AzCustomIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad083-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ad083-107">DESCRIPTION</span></span>
<span data-ttu-id="ad083-108">**AzCustomIpPrefix** cmdlet은 입력 매개 변수 집합에 제공 되는 하나 이상의 CustomIpPrefixes를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ad083-108">The **Get-AzCustomIpPrefix** cmdlet gets one or more CustomIpPrefixes given the set of input parameters</span></span>

## <span data-ttu-id="ad083-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ad083-109">EXAMPLES</span></span>

### <span data-ttu-id="ad083-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ad083-110">Example 1</span></span>
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

<span data-ttu-id="ad083-111">이 명령은 리소스 그룹 myRg의 myCustomIpPrefix 이라는 CustomIpPrefix 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ad083-111">This command gets a CustomIpPrefix resource named myCustomIpPrefix in resource group myRg</span></span>

## <span data-ttu-id="ad083-112">변수</span><span class="sxs-lookup"><span data-stu-id="ad083-112">PARAMETERS</span></span>

### <span data-ttu-id="ad083-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad083-113">-DefaultProfile</span></span>
<span data-ttu-id="ad083-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad083-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad083-115">-이름</span><span class="sxs-lookup"><span data-stu-id="ad083-115">-Name</span></span>
<span data-ttu-id="ad083-116">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad083-116">The resource name.</span></span>

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

### <span data-ttu-id="ad083-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad083-117">-ResourceGroupName</span></span>
<span data-ttu-id="ad083-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad083-118">The resource group name.</span></span>

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

### <span data-ttu-id="ad083-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad083-119">-ResourceId</span></span>
<span data-ttu-id="ad083-120">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="ad083-120">The resource id.</span></span>

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

### <span data-ttu-id="ad083-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad083-121">CommonParameters</span></span>
<span data-ttu-id="ad083-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad083-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad083-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ad083-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad083-124">입력</span><span class="sxs-lookup"><span data-stu-id="ad083-124">INPUTS</span></span>

### <span data-ttu-id="ad083-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ad083-125">System.String</span></span>

## <span data-ttu-id="ad083-126">출력</span><span class="sxs-lookup"><span data-stu-id="ad083-126">OUTPUTS</span></span>

### <span data-ttu-id="ad083-127">PSCustomIpPrefix에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ad083-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="ad083-128">상속자</span><span class="sxs-lookup"><span data-stu-id="ad083-128">NOTES</span></span>

## <span data-ttu-id="ad083-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad083-129">RELATED LINKS</span></span>

[<span data-ttu-id="ad083-130">새로운 AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ad083-130">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="ad083-131">제거-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ad083-131">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="ad083-132">업데이트-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ad083-132">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)