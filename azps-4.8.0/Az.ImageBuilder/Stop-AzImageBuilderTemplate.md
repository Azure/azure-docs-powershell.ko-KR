---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/stop-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
ms.openlocfilehash: 01fd95dd41a7ee76c06f0423d33c4aba34329c18
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212754"
---
# <span data-ttu-id="e2ac1-101">Stop-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="e2ac1-101">Stop-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="e2ac1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="e2ac1-103">이미지 템플릿을 기반으로 장기 실행 이미지 빌드 취소</span><span class="sxs-lookup"><span data-stu-id="e2ac1-103">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="e2ac1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2ac1-104">SYNTAX</span></span>

### <span data-ttu-id="e2ac1-105">취소 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e2ac1-105">Cancel (Default)</span></span>
```
Stop-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e2ac1-106">CancelViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e2ac1-106">CancelViaIdentity</span></span>
```
Stop-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e2ac1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e2ac1-107">DESCRIPTION</span></span>
<span data-ttu-id="e2ac1-108">이미지 템플릿을 기반으로 장기 실행 이미지 빌드 취소</span><span class="sxs-lookup"><span data-stu-id="e2ac1-108">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="e2ac1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e2ac1-109">EXAMPLES</span></span>

### <span data-ttu-id="e2ac1-110">예제 1: 이미지 서식 파일 만들기 중지</span><span class="sxs-lookup"><span data-stu-id="e2ac1-110">Example 1: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> Stop-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="e2ac1-111">이 명령은 이미지 서식 파일 만들기를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-111">This command stops image template creation.</span></span>

### <span data-ttu-id="e2ac1-112">예제 2: 이미지 서식 파일 만들기 중지</span><span class="sxs-lookup"><span data-stu-id="e2ac1-112">Example 2: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Stop-AzImageBuilderTemplate -InputObject $template 

```

<span data-ttu-id="e2ac1-113">이 명령은 이미지 서식 파일 만들기를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-113">This command stops image template creation.</span></span>

## <span data-ttu-id="e2ac1-114">변수</span><span class="sxs-lookup"><span data-stu-id="e2ac1-114">PARAMETERS</span></span>

### <span data-ttu-id="e2ac1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2ac1-115">-AsJob</span></span>
<span data-ttu-id="e2ac1-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="e2ac1-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e2ac1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2ac1-117">-DefaultProfile</span></span>
<span data-ttu-id="e2ac1-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2ac1-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="e2ac1-119">-ImageTemplateName</span></span>
<span data-ttu-id="e2ac1-120">이미지 서식 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-120">The name of the image Template</span></span>

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

### <span data-ttu-id="e2ac1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2ac1-121">-InputObject</span></span>
<span data-ttu-id="e2ac1-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e2ac1-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e2ac1-123">-NoWait</span></span>
<span data-ttu-id="e2ac1-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="e2ac1-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e2ac1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2ac1-125">-PassThru</span></span>
<span data-ttu-id="e2ac1-126">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e2ac1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2ac1-127">-ResourceGroupName</span></span>
<span data-ttu-id="e2ac1-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="e2ac1-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2ac1-129">-SubscriptionId</span></span>
<span data-ttu-id="e2ac1-130">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e2ac1-131">구독 Id는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e2ac1-132">-확인</span><span class="sxs-lookup"><span data-stu-id="e2ac1-132">-Confirm</span></span>
<span data-ttu-id="e2ac1-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2ac1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2ac1-134">-WhatIf</span></span>
<span data-ttu-id="e2ac1-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2ac1-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2ac1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2ac1-137">CommonParameters</span></span>
<span data-ttu-id="e2ac1-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2ac1-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2ac1-140">입력</span><span class="sxs-lookup"><span data-stu-id="e2ac1-140">INPUTS</span></span>

### <span data-ttu-id="e2ac1-141">IImageBuilderIdentity-. i g a.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="e2ac1-142">출력</span><span class="sxs-lookup"><span data-stu-id="e2ac1-142">OUTPUTS</span></span>

### <span data-ttu-id="e2ac1-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e2ac1-143">System.Boolean</span></span>

## <span data-ttu-id="e2ac1-144">상속자</span><span class="sxs-lookup"><span data-stu-id="e2ac1-144">NOTES</span></span>

<span data-ttu-id="e2ac1-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="e2ac1-145">ALIASES</span></span>

<span data-ttu-id="e2ac1-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="e2ac1-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e2ac1-147">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e2ac1-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e2ac1-149">INPUTOBJECT <IImageBuilderIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e2ac1-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e2ac1-150">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="e2ac1-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e2ac1-151">`[ImageTemplateName <String>]`: 이미지 서식 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="e2ac1-152">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="e2ac1-153">`[RunOutputName <String>]`: 실행 출력의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="e2ac1-154">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e2ac1-155">구독 Id는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ac1-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e2ac1-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2ac1-156">RELATED LINKS</span></span>

