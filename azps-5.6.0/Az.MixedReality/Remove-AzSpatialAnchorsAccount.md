---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 502b7b7c97752758003c1a7f0ad007e3e6cf67e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980368"
---
# <span data-ttu-id="7f55a-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="7f55a-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="7f55a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f55a-102">SYNOPSIS</span></span>
<span data-ttu-id="7f55a-103">공간 앵커 계정 삭제</span><span class="sxs-lookup"><span data-stu-id="7f55a-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="7f55a-104">구문</span><span class="sxs-lookup"><span data-stu-id="7f55a-104">SYNTAX</span></span>

### <span data-ttu-id="7f55a-105">DefaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7f55a-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f55a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f55a-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f55a-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f55a-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f55a-108">설명</span><span class="sxs-lookup"><span data-stu-id="7f55a-108">DESCRIPTION</span></span>
<span data-ttu-id="7f55a-109">특정 구독 및 리소스 그룹에서 지정된 공간 앵커 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7f55a-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="7f55a-110">예제</span><span class="sxs-lookup"><span data-stu-id="7f55a-110">EXAMPLES</span></span>

### <span data-ttu-id="7f55a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7f55a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="7f55a-112">현재 구독 및 리소스 그룹 "rg1"에서 공간 앵커 계정 "예제"를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7f55a-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="7f55a-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7f55a-113">PARAMETERS</span></span>

### <span data-ttu-id="7f55a-114">-확인</span><span class="sxs-lookup"><span data-stu-id="7f55a-114">-Confirm</span></span>
<span data-ttu-id="7f55a-115">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f55a-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f55a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f55a-116">-DefaultProfile</span></span>
<span data-ttu-id="7f55a-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f55a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f55a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f55a-118">-InputObject</span></span>
<span data-ttu-id="7f55a-119">사용자 지정 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7f55a-119">The custom domain object.</span></span>

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

### <span data-ttu-id="7f55a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7f55a-120">-Name</span></span>
<span data-ttu-id="7f55a-121">공간 앵커 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f55a-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="7f55a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f55a-122">-PassThru</span></span>
<span data-ttu-id="7f55a-123">지정된 경우 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7f55a-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f55a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f55a-124">-ResourceGroupName</span></span>
<span data-ttu-id="7f55a-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f55a-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="7f55a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f55a-126">-ResourceId</span></span>
<span data-ttu-id="7f55a-127">공간 앵커 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7f55a-127">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="7f55a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f55a-128">-WhatIf</span></span>
<span data-ttu-id="7f55a-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7f55a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f55a-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f55a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f55a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f55a-131">CommonParameters</span></span>
<span data-ttu-id="7f55a-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7f55a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7f55a-133">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7f55a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f55a-134">입력</span><span class="sxs-lookup"><span data-stu-id="7f55a-134">INPUTS</span></span>

### <span data-ttu-id="7f55a-135">System.String</span><span class="sxs-lookup"><span data-stu-id="7f55a-135">System.String</span></span>

### <span data-ttu-id="7f55a-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="7f55a-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="7f55a-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7f55a-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7f55a-138">출력</span><span class="sxs-lookup"><span data-stu-id="7f55a-138">OUTPUTS</span></span>

### <span data-ttu-id="7f55a-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7f55a-139">System.Boolean</span></span>

## <span data-ttu-id="7f55a-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7f55a-140">NOTES</span></span>

## <span data-ttu-id="7f55a-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f55a-141">RELATED LINKS</span></span>
