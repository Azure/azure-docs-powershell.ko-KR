---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/start-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
ms.openlocfilehash: 75065d50b8176b256c5cf91c136f4f4588232e55
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964667"
---
# <span data-ttu-id="47925-101">Start-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="47925-101">Start-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="47925-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47925-102">SYNOPSIS</span></span>
<span data-ttu-id="47925-103">기존 이미지 템플릿에서 아티팩트 만들기</span><span class="sxs-lookup"><span data-stu-id="47925-103">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="47925-104">구문</span><span class="sxs-lookup"><span data-stu-id="47925-104">SYNTAX</span></span>

### <span data-ttu-id="47925-105">실행(기본값)</span><span class="sxs-lookup"><span data-stu-id="47925-105">Run (Default)</span></span>
```
Start-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="47925-106">RunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="47925-106">RunViaIdentity</span></span>
```
Start-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="47925-107">설명</span><span class="sxs-lookup"><span data-stu-id="47925-107">DESCRIPTION</span></span>
<span data-ttu-id="47925-108">기존 이미지 템플릿에서 아티팩트 만들기</span><span class="sxs-lookup"><span data-stu-id="47925-108">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="47925-109">예제</span><span class="sxs-lookup"><span data-stu-id="47925-109">EXAMPLES</span></span>

### <span data-ttu-id="47925-110">예제 1: 이미지 템플릿 시작</span><span class="sxs-lookup"><span data-stu-id="47925-110">Example 1: Start an image template</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg

```

<span data-ttu-id="47925-111">이 명령은 이미지 템플릿을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="47925-111">This command starts an image template.</span></span>

### <span data-ttu-id="47925-112">예제 2: 이미지 템플릿 시작</span><span class="sxs-lookup"><span data-stu-id="47925-112">Example 2: Start an image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Start-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="47925-113">이 명령은 이미지 템플릿을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="47925-113">This command starts an image template.</span></span>

## <span data-ttu-id="47925-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="47925-114">PARAMETERS</span></span>

### <span data-ttu-id="47925-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47925-115">-AsJob</span></span>
<span data-ttu-id="47925-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="47925-116">Run the command as a job</span></span>

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

### <span data-ttu-id="47925-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47925-117">-DefaultProfile</span></span>
<span data-ttu-id="47925-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47925-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47925-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="47925-119">-ImageTemplateName</span></span>
<span data-ttu-id="47925-120">이미지 템플릿의 이름</span><span class="sxs-lookup"><span data-stu-id="47925-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47925-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47925-121">-InputObject</span></span>
<span data-ttu-id="47925-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="47925-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: RunViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47925-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="47925-123">-NoWait</span></span>
<span data-ttu-id="47925-124">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="47925-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="47925-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47925-125">-PassThru</span></span>
<span data-ttu-id="47925-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="47925-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="47925-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47925-127">-ResourceGroupName</span></span>
<span data-ttu-id="47925-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47925-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47925-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47925-129">-SubscriptionId</span></span>
<span data-ttu-id="47925-130">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="47925-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="47925-131">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="47925-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47925-132">-확인</span><span class="sxs-lookup"><span data-stu-id="47925-132">-Confirm</span></span>
<span data-ttu-id="47925-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="47925-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47925-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47925-134">-WhatIf</span></span>
<span data-ttu-id="47925-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="47925-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47925-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47925-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47925-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47925-137">CommonParameters</span></span>
<span data-ttu-id="47925-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="47925-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47925-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47925-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47925-140">입력</span><span class="sxs-lookup"><span data-stu-id="47925-140">INPUTS</span></span>

### <span data-ttu-id="47925-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="47925-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="47925-142">출력</span><span class="sxs-lookup"><span data-stu-id="47925-142">OUTPUTS</span></span>

### <span data-ttu-id="47925-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="47925-143">System.Boolean</span></span>

## <span data-ttu-id="47925-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="47925-144">NOTES</span></span>

<span data-ttu-id="47925-145">별칭</span><span class="sxs-lookup"><span data-stu-id="47925-145">ALIASES</span></span>

<span data-ttu-id="47925-146">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="47925-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="47925-147">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="47925-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="47925-148">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="47925-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="47925-149">INPUTOBJECT <IImageBuilderIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="47925-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="47925-150">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="47925-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="47925-151">`[ImageTemplateName <String>]`: 이미지 템플릿의 이름</span><span class="sxs-lookup"><span data-stu-id="47925-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="47925-152">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47925-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="47925-153">`[RunOutputName <String>]`: 실행 출력의 이름</span><span class="sxs-lookup"><span data-stu-id="47925-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="47925-154">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="47925-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="47925-155">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="47925-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="47925-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47925-156">RELATED LINKS</span></span>

