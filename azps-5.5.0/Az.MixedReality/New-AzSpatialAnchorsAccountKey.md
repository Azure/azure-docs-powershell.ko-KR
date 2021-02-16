---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 35c00fca10223a22d586efba8961dd9cab6b0faf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185017"
---
# <span data-ttu-id="82ab7-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="82ab7-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="82ab7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="82ab7-103">Spatial Anchors 계정의 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="82ab7-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="82ab7-104">구문</span><span class="sxs-lookup"><span data-stu-id="82ab7-104">SYNTAX</span></span>

### <span data-ttu-id="82ab7-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="82ab7-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82ab7-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="82ab7-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82ab7-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="82ab7-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82ab7-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="82ab7-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82ab7-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="82ab7-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82ab7-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="82ab7-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82ab7-111">설명</span><span class="sxs-lookup"><span data-stu-id="82ab7-111">DESCRIPTION</span></span>
<span data-ttu-id="82ab7-112">Spatial Anchors 계정의 기본 키 또는 보조 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="82ab7-112">Regenerate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="82ab7-113">예제</span><span class="sxs-lookup"><span data-stu-id="82ab7-113">EXAMPLES</span></span>

### <span data-ttu-id="82ab7-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="82ab7-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="82ab7-115">리소스 그룹 "rg1"에서 Spatial Anchors 계정 "example"의 보조 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="82ab7-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="82ab7-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="82ab7-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="82ab7-117">현재 구독에서 Spatial Anchors 계정 "example"의 보조 키를 다시 생성하고 파이핑을 통해 리소스 그룹 "rg1"을 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="82ab7-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="82ab7-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82ab7-118">PARAMETERS</span></span>

### <span data-ttu-id="82ab7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ab7-119">-DefaultProfile</span></span>
<span data-ttu-id="82ab7-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82ab7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82ab7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="82ab7-121">-Force</span></span>
<span data-ttu-id="82ab7-122">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="82ab7-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="82ab7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82ab7-123">-InputObject</span></span>
<span data-ttu-id="82ab7-124">사용자 지정 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="82ab7-124">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82ab7-125">-Name</span><span class="sxs-lookup"><span data-stu-id="82ab7-125">-Name</span></span>
<span data-ttu-id="82ab7-126">Spatial Anchors 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82ab7-126">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ab7-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="82ab7-127">-Primary</span></span>
<span data-ttu-id="82ab7-128">Spatial Anchors 계정의 기본 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="82ab7-128">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ab7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82ab7-129">-ResourceGroupName</span></span>
<span data-ttu-id="82ab7-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82ab7-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ab7-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82ab7-131">-ResourceId</span></span>
<span data-ttu-id="82ab7-132">Spatial Anchors 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="82ab7-132">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ab7-133">-Secondary</span><span class="sxs-lookup"><span data-stu-id="82ab7-133">-Secondary</span></span>
<span data-ttu-id="82ab7-134">Spatial Anchors 계정의 기본 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="82ab7-134">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ab7-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82ab7-135">-Confirm</span></span>
<span data-ttu-id="82ab7-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="82ab7-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ab7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82ab7-137">-WhatIf</span></span>
<span data-ttu-id="82ab7-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="82ab7-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82ab7-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82ab7-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ab7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ab7-140">CommonParameters</span></span>
<span data-ttu-id="82ab7-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82ab7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="82ab7-142">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="82ab7-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ab7-143">입력</span><span class="sxs-lookup"><span data-stu-id="82ab7-143">INPUTS</span></span>

### <span data-ttu-id="82ab7-144">System.String</span><span class="sxs-lookup"><span data-stu-id="82ab7-144">System.String</span></span>

### <span data-ttu-id="82ab7-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="82ab7-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="82ab7-146">출력</span><span class="sxs-lookup"><span data-stu-id="82ab7-146">OUTPUTS</span></span>

### <span data-ttu-id="82ab7-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="82ab7-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="82ab7-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82ab7-148">NOTES</span></span>

## <span data-ttu-id="82ab7-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82ab7-149">RELATED LINKS</span></span>
