---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 81bce36cb1b8cd4737141e58ad3e220199e726cf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492786"
---
# <span data-ttu-id="8fb40-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="8fb40-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="8fb40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fb40-102">SYNOPSIS</span></span>
<span data-ttu-id="8fb40-103">Spatial Anchors 계정의 키 얻기</span><span class="sxs-lookup"><span data-stu-id="8fb40-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="8fb40-104">구문</span><span class="sxs-lookup"><span data-stu-id="8fb40-104">SYNTAX</span></span>

### <span data-ttu-id="8fb40-105">DefaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8fb40-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fb40-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fb40-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fb40-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fb40-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fb40-108">설명</span><span class="sxs-lookup"><span data-stu-id="8fb40-108">DESCRIPTION</span></span>
<span data-ttu-id="8fb40-109">Spatial Anchors 계정의 개발자 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8fb40-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="8fb40-110">예제</span><span class="sxs-lookup"><span data-stu-id="8fb40-110">EXAMPLES</span></span>

### <span data-ttu-id="8fb40-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8fb40-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="8fb40-112">현재 구독 및 리소스 그룹 "rg1"에서 Spatial Anchors 계정 "example"의 개발자 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8fb40-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="8fb40-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="8fb40-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="8fb40-114">현재 구독에서 Spatial Anchors 계정 "example"의 개발자 키를, 파이핑을 사용하여 리소스 그룹 "rg1"을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8fb40-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="8fb40-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fb40-115">PARAMETERS</span></span>

### <span data-ttu-id="8fb40-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fb40-116">-DefaultProfile</span></span>
<span data-ttu-id="8fb40-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8fb40-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fb40-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fb40-118">-InputObject</span></span>
<span data-ttu-id="8fb40-119">사용자 지정 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8fb40-119">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fb40-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8fb40-120">-Name</span></span>
<span data-ttu-id="8fb40-121">Spatial Anchors 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fb40-121">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fb40-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fb40-122">-ResourceGroupName</span></span>
<span data-ttu-id="8fb40-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fb40-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fb40-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fb40-124">-ResourceId</span></span>
<span data-ttu-id="8fb40-125">Spatial Anchors 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8fb40-125">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fb40-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fb40-126">CommonParameters</span></span>
<span data-ttu-id="8fb40-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8fb40-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8fb40-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8fb40-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fb40-129">입력</span><span class="sxs-lookup"><span data-stu-id="8fb40-129">INPUTS</span></span>

### <span data-ttu-id="8fb40-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8fb40-130">System.String</span></span>

### <span data-ttu-id="8fb40-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="8fb40-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="8fb40-132">출력</span><span class="sxs-lookup"><span data-stu-id="8fb40-132">OUTPUTS</span></span>

### <span data-ttu-id="8fb40-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8fb40-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="8fb40-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8fb40-134">NOTES</span></span>

## <span data-ttu-id="8fb40-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8fb40-135">RELATED LINKS</span></span>
