---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4cc45f3b4cd21e41f1b2e410dd2b76b9571a4431
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337058"
---
# <span data-ttu-id="b63ff-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="b63ff-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="b63ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b63ff-102">SYNOPSIS</span></span>
<span data-ttu-id="b63ff-103">지정된 이미지 템플릿 리소스에 대해 지정된 실행 출력을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b63ff-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="b63ff-104">구문</span><span class="sxs-lookup"><span data-stu-id="b63ff-104">SYNTAX</span></span>

### <span data-ttu-id="b63ff-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="b63ff-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b63ff-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="b63ff-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b63ff-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b63ff-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b63ff-108">설명</span><span class="sxs-lookup"><span data-stu-id="b63ff-108">DESCRIPTION</span></span>
<span data-ttu-id="b63ff-109">지정된 이미지 템플릿 리소스에 대해 지정된 실행 출력을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b63ff-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="b63ff-110">예제</span><span class="sxs-lookup"><span data-stu-id="b63ff-110">EXAMPLES</span></span>

### <span data-ttu-id="b63ff-111">예제 1: 템플릿 아래에 모든 실행 결과 나열</span><span class="sxs-lookup"><span data-stu-id="b63ff-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="b63ff-112">이 명령은 템플릿 아래에 모든 실행 결과를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b63ff-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="b63ff-113">예제 2: 템플릿에서 실행 결과 얻기</span><span class="sxs-lookup"><span data-stu-id="b63ff-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="b63ff-114">이 명령은 템플릿 아래에서 실행 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b63ff-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="b63ff-115">예제 3: 템플릿에서 실행 결과 얻기</span><span class="sxs-lookup"><span data-stu-id="b63ff-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="b63ff-116">이 명령은 템플릿 아래에서 실행 결과를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b63ff-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="b63ff-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b63ff-117">PARAMETERS</span></span>

### <span data-ttu-id="b63ff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b63ff-118">-DefaultProfile</span></span>
<span data-ttu-id="b63ff-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b63ff-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b63ff-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="b63ff-120">-ImageTemplateName</span></span>
<span data-ttu-id="b63ff-121">이미지 템플릿의 이름</span><span class="sxs-lookup"><span data-stu-id="b63ff-121">The name of the image Template</span></span>

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

### <span data-ttu-id="b63ff-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b63ff-122">-InputObject</span></span>
<span data-ttu-id="b63ff-123">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="b63ff-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b63ff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b63ff-124">-ResourceGroupName</span></span>
<span data-ttu-id="b63ff-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b63ff-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="b63ff-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="b63ff-126">-RunOutputName</span></span>
<span data-ttu-id="b63ff-127">실행 출력의 이름</span><span class="sxs-lookup"><span data-stu-id="b63ff-127">The name of the run output</span></span>

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

### <span data-ttu-id="b63ff-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b63ff-128">-SubscriptionId</span></span>
<span data-ttu-id="b63ff-129">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="b63ff-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b63ff-130">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="b63ff-130">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b63ff-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b63ff-131">CommonParameters</span></span>
<span data-ttu-id="b63ff-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b63ff-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b63ff-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b63ff-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b63ff-134">입력</span><span class="sxs-lookup"><span data-stu-id="b63ff-134">INPUTS</span></span>

### <span data-ttu-id="b63ff-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="b63ff-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="b63ff-136">출력</span><span class="sxs-lookup"><span data-stu-id="b63ff-136">OUTPUTS</span></span>

### <span data-ttu-id="b63ff-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span><span class="sxs-lookup"><span data-stu-id="b63ff-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="b63ff-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b63ff-138">NOTES</span></span>

<span data-ttu-id="b63ff-139">별칭</span><span class="sxs-lookup"><span data-stu-id="b63ff-139">ALIASES</span></span>

<span data-ttu-id="b63ff-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b63ff-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b63ff-141">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b63ff-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b63ff-142">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b63ff-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b63ff-143">INPUTOBJECT: <IImageBuilderIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b63ff-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b63ff-144">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="b63ff-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b63ff-145">`[ImageTemplateName <String>]`: 이미지 템플릿의 이름</span><span class="sxs-lookup"><span data-stu-id="b63ff-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="b63ff-146">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b63ff-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b63ff-147">`[RunOutputName <String>]`: 실행 출력의 이름</span><span class="sxs-lookup"><span data-stu-id="b63ff-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="b63ff-148">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="b63ff-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b63ff-149">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="b63ff-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b63ff-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b63ff-150">RELATED LINKS</span></span>

