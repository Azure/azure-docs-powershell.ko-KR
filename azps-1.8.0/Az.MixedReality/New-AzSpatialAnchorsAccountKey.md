---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 043b97a256fff50ca9831685a90f0cfb46ff7277
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867377"
---
# <span data-ttu-id="ef0f2-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="ef0f2-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="ef0f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef0f2-102">SYNOPSIS</span></span>
<span data-ttu-id="ef0f2-103">공간 앵커 계정의 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="ef0f2-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="ef0f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ef0f2-104">SYNTAX</span></span>

### <span data-ttu-id="ef0f2-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef0f2-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef0f2-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef0f2-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef0f2-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef0f2-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef0f2-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef0f2-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef0f2-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef0f2-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef0f2-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef0f2-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef0f2-111">설명은</span><span class="sxs-lookup"><span data-stu-id="ef0f2-111">DESCRIPTION</span></span>
<span data-ttu-id="ef0f2-112">Renegrate 기본 키 또는 공간 앵커 계정의 보조 키입니다.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-112">Renegrate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="ef0f2-113">예제의</span><span class="sxs-lookup"><span data-stu-id="ef0f2-113">EXAMPLES</span></span>

### <span data-ttu-id="ef0f2-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="ef0f2-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="ef0f2-115">리소스 그룹 "rg1"에서 공간 앵커 계정의 보조 키 "예제"를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="ef0f2-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="ef0f2-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="ef0f2-117">현재 구독 및 리소스 그룹 "rg1"에서 "example" 공간 앵커 계정의 보조 키를 파이프로 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="ef0f2-118">변수</span><span class="sxs-lookup"><span data-stu-id="ef0f2-118">PARAMETERS</span></span>

### <span data-ttu-id="ef0f2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef0f2-119">-DefaultProfile</span></span>
<span data-ttu-id="ef0f2-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef0f2-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ef0f2-121">-Force</span></span>
<span data-ttu-id="ef0f2-122">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ef0f2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef0f2-123">-InputObject</span></span>
<span data-ttu-id="ef0f2-124">사용자 지정 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-124">The custom domain object.</span></span>

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

### <span data-ttu-id="ef0f2-125">-이름</span><span class="sxs-lookup"><span data-stu-id="ef0f2-125">-Name</span></span>
<span data-ttu-id="ef0f2-126">공간 앵커 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-126">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="ef0f2-127">-기본</span><span class="sxs-lookup"><span data-stu-id="ef0f2-127">-Primary</span></span>
<span data-ttu-id="ef0f2-128">공간 앵커 계정의 기본 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-128">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="ef0f2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef0f2-129">-ResourceGroupName</span></span>
<span data-ttu-id="ef0f2-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="ef0f2-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef0f2-131">-ResourceId</span></span>
<span data-ttu-id="ef0f2-132">공간 앵커 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-132">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="ef0f2-133">-보조</span><span class="sxs-lookup"><span data-stu-id="ef0f2-133">-Secondary</span></span>
<span data-ttu-id="ef0f2-134">공간 앵커 계정의 기본 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-134">Regenerate primary key of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="ef0f2-135">-확인</span><span class="sxs-lookup"><span data-stu-id="ef0f2-135">-Confirm</span></span>
<span data-ttu-id="ef0f2-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef0f2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef0f2-137">-WhatIf</span></span>
<span data-ttu-id="ef0f2-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef0f2-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef0f2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef0f2-140">CommonParameters</span></span>
<span data-ttu-id="ef0f2-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0f2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ef0f2-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef0f2-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef0f2-143">입력</span><span class="sxs-lookup"><span data-stu-id="ef0f2-143">INPUTS</span></span>

### <span data-ttu-id="ef0f2-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ef0f2-144">System.String</span></span>

### <span data-ttu-id="ef0f2-145">MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="ef0f2-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="ef0f2-146">출력</span><span class="sxs-lookup"><span data-stu-id="ef0f2-146">OUTPUTS</span></span>

### <span data-ttu-id="ef0f2-147">MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ef0f2-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccountKeys</span></span>

## <span data-ttu-id="ef0f2-148">상속자</span><span class="sxs-lookup"><span data-stu-id="ef0f2-148">NOTES</span></span>

## <span data-ttu-id="ef0f2-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef0f2-149">RELATED LINKS</span></span>
