---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/start-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
ms.openlocfilehash: 710c39adca3f3a82b91b1e27a7f63e0ef1f6b693
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212756"
---
# <span data-ttu-id="cb927-101">Start-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="cb927-101">Start-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="cb927-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb927-102">SYNOPSIS</span></span>
<span data-ttu-id="cb927-103">기존 이미지 서식 파일에서 아티팩트 만들기</span><span class="sxs-lookup"><span data-stu-id="cb927-103">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="cb927-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cb927-104">SYNTAX</span></span>

### <span data-ttu-id="cb927-105">실행 (기본값)</span><span class="sxs-lookup"><span data-stu-id="cb927-105">Run (Default)</span></span>
```
Start-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cb927-106">RunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cb927-106">RunViaIdentity</span></span>
```
Start-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cb927-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cb927-107">DESCRIPTION</span></span>
<span data-ttu-id="cb927-108">기존 이미지 서식 파일에서 아티팩트 만들기</span><span class="sxs-lookup"><span data-stu-id="cb927-108">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="cb927-109">예제의</span><span class="sxs-lookup"><span data-stu-id="cb927-109">EXAMPLES</span></span>

### <span data-ttu-id="cb927-110">예제 1: 이미지 서식 파일 시작</span><span class="sxs-lookup"><span data-stu-id="cb927-110">Example 1: Start an image template</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg

```

<span data-ttu-id="cb927-111">이 명령은 이미지 서식 파일을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb927-111">This command starts an image template.</span></span>

### <span data-ttu-id="cb927-112">예제 2: 이미지 서식 파일 시작</span><span class="sxs-lookup"><span data-stu-id="cb927-112">Example 2: Start an image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Start-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="cb927-113">이 명령은 이미지 서식 파일을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb927-113">This command starts an image template.</span></span>

## <span data-ttu-id="cb927-114">변수</span><span class="sxs-lookup"><span data-stu-id="cb927-114">PARAMETERS</span></span>

### <span data-ttu-id="cb927-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb927-115">-AsJob</span></span>
<span data-ttu-id="cb927-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="cb927-116">Run the command as a job</span></span>

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

### <span data-ttu-id="cb927-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb927-117">-DefaultProfile</span></span>
<span data-ttu-id="cb927-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb927-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb927-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="cb927-119">-ImageTemplateName</span></span>
<span data-ttu-id="cb927-120">이미지 서식 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb927-120">The name of the image Template</span></span>

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

### <span data-ttu-id="cb927-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb927-121">-InputObject</span></span>
<span data-ttu-id="cb927-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cb927-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cb927-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cb927-123">-NoWait</span></span>
<span data-ttu-id="cb927-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="cb927-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cb927-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb927-125">-PassThru</span></span>
<span data-ttu-id="cb927-126">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb927-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cb927-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb927-127">-ResourceGroupName</span></span>
<span data-ttu-id="cb927-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb927-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="cb927-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb927-129">-SubscriptionId</span></span>
<span data-ttu-id="cb927-130">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="cb927-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cb927-131">구독 Id는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb927-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cb927-132">-확인</span><span class="sxs-lookup"><span data-stu-id="cb927-132">-Confirm</span></span>
<span data-ttu-id="cb927-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb927-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb927-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb927-134">-WhatIf</span></span>
<span data-ttu-id="cb927-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cb927-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb927-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb927-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb927-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb927-137">CommonParameters</span></span>
<span data-ttu-id="cb927-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb927-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb927-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cb927-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb927-140">입력</span><span class="sxs-lookup"><span data-stu-id="cb927-140">INPUTS</span></span>

### <span data-ttu-id="cb927-141">IImageBuilderIdentity-. i g a.</span><span class="sxs-lookup"><span data-stu-id="cb927-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="cb927-142">출력</span><span class="sxs-lookup"><span data-stu-id="cb927-142">OUTPUTS</span></span>

### <span data-ttu-id="cb927-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="cb927-143">System.Boolean</span></span>

## <span data-ttu-id="cb927-144">상속자</span><span class="sxs-lookup"><span data-stu-id="cb927-144">NOTES</span></span>

<span data-ttu-id="cb927-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="cb927-145">ALIASES</span></span>

<span data-ttu-id="cb927-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="cb927-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cb927-147">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb927-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cb927-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="cb927-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cb927-149">INPUTOBJECT <IImageBuilderIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="cb927-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cb927-150">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="cb927-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cb927-151">`[ImageTemplateName <String>]`: 이미지 서식 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb927-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="cb927-152">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb927-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="cb927-153">`[RunOutputName <String>]`: 실행 출력의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb927-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="cb927-154">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="cb927-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cb927-155">구독 Id는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb927-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cb927-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb927-156">RELATED LINKS</span></span>

