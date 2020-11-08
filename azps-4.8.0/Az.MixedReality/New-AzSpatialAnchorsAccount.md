---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 0b61764d358cc234f66dc8bb24249ca93a4e9919
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213495"
---
# <span data-ttu-id="f0a82-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="f0a82-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="f0a82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0a82-102">SYNOPSIS</span></span>
<span data-ttu-id="f0a82-103">공간 앵커 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="f0a82-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="f0a82-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f0a82-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0a82-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f0a82-105">DESCRIPTION</span></span>
<span data-ttu-id="f0a82-106">특정 구독, 리소스 그룹 및 영역에서 새 공간 앵커 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0a82-106">Create a new Spatial Anchors Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="f0a82-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f0a82-107">EXAMPLES</span></span>

### <span data-ttu-id="f0a82-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f0a82-108">Example 1</span></span>
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

<span data-ttu-id="f0a82-109">현재 구독, 리소스 그룹 "rg1" 및 중부 US에 새 공간 앵커 계정 "예제"를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0a82-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="f0a82-110">변수</span><span class="sxs-lookup"><span data-stu-id="f0a82-110">PARAMETERS</span></span>

### <span data-ttu-id="f0a82-111">-확인</span><span class="sxs-lookup"><span data-stu-id="f0a82-111">-Confirm</span></span>
<span data-ttu-id="f0a82-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0a82-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0a82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0a82-113">-DefaultProfile</span></span>
<span data-ttu-id="f0a82-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f0a82-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0a82-115">-위치</span><span class="sxs-lookup"><span data-stu-id="f0a82-115">-Location</span></span>
<span data-ttu-id="f0a82-116">공간 앵커 계정 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f0a82-116">Spatial Anchors Account Location.</span></span>

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

### <span data-ttu-id="f0a82-117">-이름</span><span class="sxs-lookup"><span data-stu-id="f0a82-117">-Name</span></span>
<span data-ttu-id="f0a82-118">공간 앵커 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0a82-118">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="f0a82-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0a82-119">-ResourceGroupName</span></span>
<span data-ttu-id="f0a82-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0a82-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="f0a82-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0a82-121">-WhatIf</span></span>
<span data-ttu-id="f0a82-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f0a82-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0a82-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0a82-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0a82-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0a82-124">CommonParameters</span></span>
<span data-ttu-id="f0a82-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0a82-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f0a82-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0a82-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0a82-127">입력</span><span class="sxs-lookup"><span data-stu-id="f0a82-127">INPUTS</span></span>

### <span data-ttu-id="f0a82-128">않아야</span><span class="sxs-lookup"><span data-stu-id="f0a82-128">None</span></span>

## <span data-ttu-id="f0a82-129">출력</span><span class="sxs-lookup"><span data-stu-id="f0a82-129">OUTPUTS</span></span>

### <span data-ttu-id="f0a82-130">MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="f0a82-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="f0a82-131">상속자</span><span class="sxs-lookup"><span data-stu-id="f0a82-131">NOTES</span></span>

## <span data-ttu-id="f0a82-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0a82-132">RELATED LINKS</span></span>
