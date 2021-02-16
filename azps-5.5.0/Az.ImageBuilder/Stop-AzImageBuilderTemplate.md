---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/stop-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
ms.openlocfilehash: 01fd95dd41a7ee76c06f0423d33c4aba34329c18
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194329"
---
# <span data-ttu-id="a80be-101">Stop-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="a80be-101">Stop-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="a80be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a80be-102">SYNOPSIS</span></span>
<span data-ttu-id="a80be-103">이미지 템플릿을 기반으로 장기 실행 이미지 빌드 취소</span><span class="sxs-lookup"><span data-stu-id="a80be-103">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="a80be-104">구문</span><span class="sxs-lookup"><span data-stu-id="a80be-104">SYNTAX</span></span>

### <span data-ttu-id="a80be-105">취소(기본값)</span><span class="sxs-lookup"><span data-stu-id="a80be-105">Cancel (Default)</span></span>
```
Stop-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a80be-106">CancelViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a80be-106">CancelViaIdentity</span></span>
```
Stop-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a80be-107">설명</span><span class="sxs-lookup"><span data-stu-id="a80be-107">DESCRIPTION</span></span>
<span data-ttu-id="a80be-108">이미지 템플릿을 기반으로 장기 실행 이미지 빌드 취소</span><span class="sxs-lookup"><span data-stu-id="a80be-108">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="a80be-109">예제</span><span class="sxs-lookup"><span data-stu-id="a80be-109">EXAMPLES</span></span>

### <span data-ttu-id="a80be-110">예제 1: 이미지 템플릿 만들기 중지</span><span class="sxs-lookup"><span data-stu-id="a80be-110">Example 1: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> Stop-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="a80be-111">이 명령은 이미지 템플릿 만들기를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="a80be-111">This command stops image template creation.</span></span>

### <span data-ttu-id="a80be-112">예제 2: 이미지 템플릿 만들기 중지</span><span class="sxs-lookup"><span data-stu-id="a80be-112">Example 2: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Stop-AzImageBuilderTemplate -InputObject $template 

```

<span data-ttu-id="a80be-113">이 명령은 이미지 템플릿 만들기를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="a80be-113">This command stops image template creation.</span></span>

## <span data-ttu-id="a80be-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a80be-114">PARAMETERS</span></span>

### <span data-ttu-id="a80be-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a80be-115">-AsJob</span></span>
<span data-ttu-id="a80be-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="a80be-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a80be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a80be-117">-DefaultProfile</span></span>
<span data-ttu-id="a80be-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a80be-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a80be-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="a80be-119">-ImageTemplateName</span></span>
<span data-ttu-id="a80be-120">이미지 템플릿의 이름</span><span class="sxs-lookup"><span data-stu-id="a80be-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a80be-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a80be-121">-InputObject</span></span>
<span data-ttu-id="a80be-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="a80be-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: CancelViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a80be-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a80be-123">-NoWait</span></span>
<span data-ttu-id="a80be-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="a80be-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a80be-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a80be-125">-PassThru</span></span>
<span data-ttu-id="a80be-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a80be-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a80be-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a80be-127">-ResourceGroupName</span></span>
<span data-ttu-id="a80be-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a80be-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a80be-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a80be-129">-SubscriptionId</span></span>
<span data-ttu-id="a80be-130">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="a80be-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a80be-131">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="a80be-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a80be-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a80be-132">-Confirm</span></span>
<span data-ttu-id="a80be-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a80be-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a80be-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a80be-134">-WhatIf</span></span>
<span data-ttu-id="a80be-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a80be-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a80be-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a80be-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a80be-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a80be-137">CommonParameters</span></span>
<span data-ttu-id="a80be-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a80be-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a80be-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a80be-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a80be-140">입력</span><span class="sxs-lookup"><span data-stu-id="a80be-140">INPUTS</span></span>

### <span data-ttu-id="a80be-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="a80be-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="a80be-142">출력</span><span class="sxs-lookup"><span data-stu-id="a80be-142">OUTPUTS</span></span>

### <span data-ttu-id="a80be-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a80be-143">System.Boolean</span></span>

## <span data-ttu-id="a80be-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a80be-144">NOTES</span></span>

<span data-ttu-id="a80be-145">별칭</span><span class="sxs-lookup"><span data-stu-id="a80be-145">ALIASES</span></span>

<span data-ttu-id="a80be-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a80be-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a80be-147">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a80be-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a80be-148">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a80be-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a80be-149">INPUTOBJECT: <IImageBuilderIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a80be-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a80be-150">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="a80be-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a80be-151">`[ImageTemplateName <String>]`: 이미지 템플릿의 이름</span><span class="sxs-lookup"><span data-stu-id="a80be-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="a80be-152">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a80be-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="a80be-153">`[RunOutputName <String>]`: 실행 출력의 이름</span><span class="sxs-lookup"><span data-stu-id="a80be-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="a80be-154">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="a80be-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a80be-155">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="a80be-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a80be-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a80be-156">RELATED LINKS</span></span>

