---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4cc45f3b4cd21e41f1b2e410dd2b76b9571a4431
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386814"
---
# <span data-ttu-id="dfa8e-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="dfa8e-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="dfa8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfa8e-102">SYNOPSIS</span></span>
<span data-ttu-id="dfa8e-103">지정된 이미지 템플릿 리소스에 대해 지정된 실행 출력을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8e-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="dfa8e-104">구문</span><span class="sxs-lookup"><span data-stu-id="dfa8e-104">SYNTAX</span></span>

### <span data-ttu-id="dfa8e-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="dfa8e-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dfa8e-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="dfa8e-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dfa8e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dfa8e-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="dfa8e-108">설명</span><span class="sxs-lookup"><span data-stu-id="dfa8e-108">DESCRIPTION</span></span>
<span data-ttu-id="dfa8e-109">지정된 이미지 템플릿 리소스에 대해 지정된 실행 출력을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8e-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="dfa8e-110">예제</span><span class="sxs-lookup"><span data-stu-id="dfa8e-110">EXAMPLES</span></span>

### <span data-ttu-id="dfa8e-111">예제 1: 템플릿 아래에 모든 실행 결과 나열</span><span class="sxs-lookup"><span data-stu-id="dfa8e-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="dfa8e-112">이 명령은 템플릿 아래에 모든 실행 결과를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8e-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="dfa8e-113">예제 2: 템플릿에서 실행 결과 얻기</span><span class="sxs-lookup"><span data-stu-id="dfa8e-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="dfa8e-114">이 명령은 템플릿 아래에서 실행 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8e-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="dfa8e-115">예제 3: 템플릿에서 실행 결과 얻기</span><span class="sxs-lookup"><span data-stu-id="dfa8e-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="dfa8e-116">이 명령은 템플릿 아래에서 실행 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8e-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="dfa8e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfa8e-117">PARAMETERS</span></span>

### <span data-ttu-id="dfa8e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfa8e-118">-DefaultProfile</span></span>
<span data-ttu-id="dfa8e-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfa8e-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="dfa8e-120">-ImageTemplateName</span></span>
<span data-ttu-id="dfa8e-121">이미지 템플릿의 이름</span><span class="sxs-lookup"><span data-stu-id="dfa8e-121">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa8e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfa8e-122">-InputObject</span></span>
<span data-ttu-id="dfa8e-123">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="dfa8e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfa8e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfa8e-124">-ResourceGroupName</span></span>
<span data-ttu-id="dfa8e-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8e-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa8e-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="dfa8e-126">-RunOutputName</span></span>
<span data-ttu-id="dfa8e-127">실행 출력의 이름</span><span class="sxs-lookup"><span data-stu-id="dfa8e-127">The name of the run output</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa8e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dfa8e-128">-SubscriptionId</span></span>
<span data-ttu-id="dfa8e-129">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8e-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dfa8e-130">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8e-130">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa8e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfa8e-131">CommonParameters</span></span>
<span data-ttu-id="dfa8e-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfa8e-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dfa8e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfa8e-134">입력</span><span class="sxs-lookup"><span data-stu-id="dfa8e-134">INPUTS</span></span>

### <span data-ttu-id="dfa8e-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="dfa8e-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="dfa8e-136">출력</span><span class="sxs-lookup"><span data-stu-id="dfa8e-136">OUTPUTS</span></span>

### <span data-ttu-id="dfa8e-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span><span class="sxs-lookup"><span data-stu-id="dfa8e-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="dfa8e-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dfa8e-138">NOTES</span></span>

<span data-ttu-id="dfa8e-139">별칭</span><span class="sxs-lookup"><span data-stu-id="dfa8e-139">ALIASES</span></span>

<span data-ttu-id="dfa8e-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="dfa8e-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dfa8e-141">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8e-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dfa8e-142">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dfa8e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dfa8e-143">INPUTOBJECT: <IImageBuilderIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="dfa8e-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dfa8e-144">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="dfa8e-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dfa8e-145">`[ImageTemplateName <String>]`: 이미지 템플릿의 이름</span><span class="sxs-lookup"><span data-stu-id="dfa8e-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="dfa8e-146">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8e-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="dfa8e-147">`[RunOutputName <String>]`: 실행 출력의 이름</span><span class="sxs-lookup"><span data-stu-id="dfa8e-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="dfa8e-148">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8e-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dfa8e-149">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="dfa8e-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="dfa8e-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dfa8e-150">RELATED LINKS</span></span>

