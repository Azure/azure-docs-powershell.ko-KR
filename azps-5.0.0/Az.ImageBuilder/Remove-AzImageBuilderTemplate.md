---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/remove-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
ms.openlocfilehash: 998c4f05e8b6a03749a4872e3f4b069e29ef634d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304001"
---
# <span data-ttu-id="c4627-101">Remove-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="c4627-101">Remove-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="c4627-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4627-102">SYNOPSIS</span></span>
<span data-ttu-id="c4627-103">가상 컴퓨터 이미지 서식 파일 삭제</span><span class="sxs-lookup"><span data-stu-id="c4627-103">Delete a virtual machine image template</span></span>

## <span data-ttu-id="c4627-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c4627-104">SYNTAX</span></span>

### <span data-ttu-id="c4627-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="c4627-105">Delete (Default)</span></span>
```
Remove-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c4627-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c4627-106">DeleteViaIdentity</span></span>
```
Remove-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c4627-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c4627-107">DESCRIPTION</span></span>
<span data-ttu-id="c4627-108">가상 컴퓨터 이미지 서식 파일 삭제</span><span class="sxs-lookup"><span data-stu-id="c4627-108">Delete a virtual machine image template</span></span>

## <span data-ttu-id="c4627-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c4627-109">EXAMPLES</span></span>

### <span data-ttu-id="c4627-110">예제 1: 이미지 서식 파일 제거</span><span class="sxs-lookup"><span data-stu-id="c4627-110">Example 1: Remove a image template</span></span>
```powershell
PS C:\> Remove-AzImageBuilderTemplate -ImageTemplateName template-name-dmt6ze -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="c4627-111">이 명령은 이미지 템플릿을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4627-111">This command removes a image template.</span></span>

### <span data-ttu-id="c4627-112">예제 2: 이미지 서식 파일 제거</span><span class="sxs-lookup"><span data-stu-id="c4627-112">Example 2: Remove a image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ImageTemplateName template-name-3uo8p6 -ResourceGroupName wyunchi-imagebuilder
PS C:\> Remove-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="c4627-113">이 명령은 이미지 템플릿을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4627-113">This command removes a image template.</span></span>

## <span data-ttu-id="c4627-114">변수</span><span class="sxs-lookup"><span data-stu-id="c4627-114">PARAMETERS</span></span>

### <span data-ttu-id="c4627-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4627-115">-AsJob</span></span>
<span data-ttu-id="c4627-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="c4627-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c4627-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4627-117">-DefaultProfile</span></span>
<span data-ttu-id="c4627-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4627-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4627-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="c4627-119">-ImageTemplateName</span></span>
<span data-ttu-id="c4627-120">이미지 서식 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4627-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4627-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4627-121">-InputObject</span></span>
<span data-ttu-id="c4627-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c4627-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4627-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c4627-123">-NoWait</span></span>
<span data-ttu-id="c4627-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="c4627-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c4627-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4627-125">-PassThru</span></span>
<span data-ttu-id="c4627-126">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4627-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c4627-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4627-127">-ResourceGroupName</span></span>
<span data-ttu-id="c4627-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4627-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4627-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4627-129">-SubscriptionId</span></span>
<span data-ttu-id="c4627-130">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="c4627-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c4627-131">구독 Id는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4627-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4627-132">-확인</span><span class="sxs-lookup"><span data-stu-id="c4627-132">-Confirm</span></span>
<span data-ttu-id="c4627-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4627-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4627-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4627-134">-WhatIf</span></span>
<span data-ttu-id="c4627-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c4627-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4627-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4627-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4627-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4627-137">CommonParameters</span></span>
<span data-ttu-id="c4627-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4627-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4627-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c4627-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4627-140">입력</span><span class="sxs-lookup"><span data-stu-id="c4627-140">INPUTS</span></span>

### <span data-ttu-id="c4627-141">IImageBuilderIdentity-. i g a.</span><span class="sxs-lookup"><span data-stu-id="c4627-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="c4627-142">출력</span><span class="sxs-lookup"><span data-stu-id="c4627-142">OUTPUTS</span></span>

### <span data-ttu-id="c4627-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c4627-143">System.Boolean</span></span>

## <span data-ttu-id="c4627-144">상속자</span><span class="sxs-lookup"><span data-stu-id="c4627-144">NOTES</span></span>

<span data-ttu-id="c4627-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="c4627-145">ALIASES</span></span>

<span data-ttu-id="c4627-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="c4627-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c4627-147">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4627-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c4627-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="c4627-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c4627-149">INPUTOBJECT <IImageBuilderIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c4627-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c4627-150">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="c4627-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c4627-151">`[ImageTemplateName <String>]`: 이미지 서식 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4627-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="c4627-152">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4627-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c4627-153">`[RunOutputName <String>]`: 실행 출력의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4627-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="c4627-154">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="c4627-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c4627-155">구독 Id는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4627-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c4627-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4627-156">RELATED LINKS</span></span>

