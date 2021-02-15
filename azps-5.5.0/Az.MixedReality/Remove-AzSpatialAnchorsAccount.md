---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 5ba079a17dcfb0a263766237adbbec9beb4cc64c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203576"
---
# <span data-ttu-id="f1527-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="f1527-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="f1527-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1527-102">SYNOPSIS</span></span>
<span data-ttu-id="f1527-103">Spatial Anchors 계정 삭제</span><span class="sxs-lookup"><span data-stu-id="f1527-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="f1527-104">구문</span><span class="sxs-lookup"><span data-stu-id="f1527-104">SYNTAX</span></span>

### <span data-ttu-id="f1527-105">DefaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f1527-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1527-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1527-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1527-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1527-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1527-108">설명</span><span class="sxs-lookup"><span data-stu-id="f1527-108">DESCRIPTION</span></span>
<span data-ttu-id="f1527-109">특정 구독 및 리소스 그룹에서 지정된 Spatial Anchors 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f1527-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="f1527-110">예제</span><span class="sxs-lookup"><span data-stu-id="f1527-110">EXAMPLES</span></span>

### <span data-ttu-id="f1527-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f1527-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="f1527-112">현재 구독 및 리소스 그룹 "rg1"에서 Spatial Anchors 계정 "example"을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f1527-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="f1527-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1527-113">PARAMETERS</span></span>

### <span data-ttu-id="f1527-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1527-114">-Confirm</span></span>
<span data-ttu-id="f1527-115">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1527-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1527-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1527-116">-DefaultProfile</span></span>
<span data-ttu-id="f1527-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1527-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1527-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1527-118">-InputObject</span></span>
<span data-ttu-id="f1527-119">사용자 지정 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f1527-119">The custom domain object.</span></span>

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

### <span data-ttu-id="f1527-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f1527-120">-Name</span></span>
<span data-ttu-id="f1527-121">Spatial Anchors 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1527-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="f1527-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1527-122">-PassThru</span></span>
<span data-ttu-id="f1527-123">지정된 경우 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f1527-123">Return object if specified.</span></span>

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

### <span data-ttu-id="f1527-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1527-124">-ResourceGroupName</span></span>
<span data-ttu-id="f1527-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1527-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="f1527-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1527-126">-ResourceId</span></span>
<span data-ttu-id="f1527-127">Spatial Anchors 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f1527-127">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="f1527-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1527-128">-WhatIf</span></span>
<span data-ttu-id="f1527-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f1527-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1527-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1527-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1527-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1527-131">CommonParameters</span></span>
<span data-ttu-id="f1527-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f1527-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f1527-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f1527-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1527-134">입력</span><span class="sxs-lookup"><span data-stu-id="f1527-134">INPUTS</span></span>

### <span data-ttu-id="f1527-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f1527-135">System.String</span></span>

### <span data-ttu-id="f1527-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="f1527-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="f1527-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f1527-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f1527-138">출력</span><span class="sxs-lookup"><span data-stu-id="f1527-138">OUTPUTS</span></span>

### <span data-ttu-id="f1527-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f1527-139">System.Boolean</span></span>

## <span data-ttu-id="f1527-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f1527-140">NOTES</span></span>

## <span data-ttu-id="f1527-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1527-141">RELATED LINKS</span></span>
