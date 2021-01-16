---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 0b61764d358cc234f66dc8bb24249ca93a4e9919
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344877"
---
# <span data-ttu-id="42802-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="42802-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="42802-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42802-102">SYNOPSIS</span></span>
<span data-ttu-id="42802-103">Spatial Anchors 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="42802-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="42802-104">구문</span><span class="sxs-lookup"><span data-stu-id="42802-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42802-105">설명</span><span class="sxs-lookup"><span data-stu-id="42802-105">DESCRIPTION</span></span>
<span data-ttu-id="42802-106">특정 구독, 리소스 그룹 및 지역에 새 Spatial Anchors 계정을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42802-106">Create a new Spatial Anchors Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="42802-107">예제</span><span class="sxs-lookup"><span data-stu-id="42802-107">EXAMPLES</span></span>

### <span data-ttu-id="42802-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="42802-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSpatialAnchorsAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="42802-109">현재 구독, 리소스 그룹 "rg1" 및 미국 중부에서 새 Spatial Anchors 계정 "예제"를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42802-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="42802-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42802-110">PARAMETERS</span></span>

### <span data-ttu-id="42802-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42802-111">-Confirm</span></span>
<span data-ttu-id="42802-112">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="42802-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42802-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42802-113">-DefaultProfile</span></span>
<span data-ttu-id="42802-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42802-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42802-115">-Location</span><span class="sxs-lookup"><span data-stu-id="42802-115">-Location</span></span>
<span data-ttu-id="42802-116">Spatial Anchors 계정 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="42802-116">Spatial Anchors Account Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42802-117">-Name</span><span class="sxs-lookup"><span data-stu-id="42802-117">-Name</span></span>
<span data-ttu-id="42802-118">Spatial Anchors 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42802-118">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42802-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42802-119">-ResourceGroupName</span></span>
<span data-ttu-id="42802-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42802-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42802-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42802-121">-WhatIf</span></span>
<span data-ttu-id="42802-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="42802-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42802-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42802-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42802-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42802-124">CommonParameters</span></span>
<span data-ttu-id="42802-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42802-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="42802-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="42802-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42802-127">입력</span><span class="sxs-lookup"><span data-stu-id="42802-127">INPUTS</span></span>

### <span data-ttu-id="42802-128">없음</span><span class="sxs-lookup"><span data-stu-id="42802-128">None</span></span>

## <span data-ttu-id="42802-129">출력</span><span class="sxs-lookup"><span data-stu-id="42802-129">OUTPUTS</span></span>

### <span data-ttu-id="42802-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="42802-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="42802-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="42802-131">NOTES</span></span>

## <span data-ttu-id="42802-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42802-132">RELATED LINKS</span></span>
