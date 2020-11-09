---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4cc45f3b4cd21e41f1b2e410dd2b76b9571a4431
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304037"
---
# <span data-ttu-id="43099-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="43099-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="43099-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43099-102">SYNOPSIS</span></span>
<span data-ttu-id="43099-103">지정한 이미지 서식 파일 리소스에 대해 지정 된 실행 출력 가져오기</span><span class="sxs-lookup"><span data-stu-id="43099-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="43099-104">구문과</span><span class="sxs-lookup"><span data-stu-id="43099-104">SYNTAX</span></span>

### <span data-ttu-id="43099-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="43099-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43099-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="43099-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43099-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="43099-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="43099-108">설명은</span><span class="sxs-lookup"><span data-stu-id="43099-108">DESCRIPTION</span></span>
<span data-ttu-id="43099-109">지정한 이미지 서식 파일 리소스에 대해 지정 된 실행 출력 가져오기</span><span class="sxs-lookup"><span data-stu-id="43099-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="43099-110">예제의</span><span class="sxs-lookup"><span data-stu-id="43099-110">EXAMPLES</span></span>

### <span data-ttu-id="43099-111">예제 1: 서식 파일에서 모든 실행 결과 나열</span><span class="sxs-lookup"><span data-stu-id="43099-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="43099-112">이 명령은 모든 실행 결과를 서식 파일에 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="43099-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="43099-113">예제 2: 템플릿 아래에서 실행 결과 가져오기</span><span class="sxs-lookup"><span data-stu-id="43099-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="43099-114">이 명령은 서식 파일 아래에서 실행 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43099-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="43099-115">예제 3: 템플릿 아래에서 실행 결과 가져오기</span><span class="sxs-lookup"><span data-stu-id="43099-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="43099-116">이 명령은 서식 파일 아래에서 실행 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43099-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="43099-117">변수</span><span class="sxs-lookup"><span data-stu-id="43099-117">PARAMETERS</span></span>

### <span data-ttu-id="43099-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43099-118">-DefaultProfile</span></span>
<span data-ttu-id="43099-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="43099-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43099-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="43099-120">-ImageTemplateName</span></span>
<span data-ttu-id="43099-121">이미지 서식 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43099-121">The name of the image Template</span></span>

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

### <span data-ttu-id="43099-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43099-122">-InputObject</span></span>
<span data-ttu-id="43099-123">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43099-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="43099-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43099-124">-ResourceGroupName</span></span>
<span data-ttu-id="43099-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43099-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="43099-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="43099-126">-RunOutputName</span></span>
<span data-ttu-id="43099-127">실행 출력의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43099-127">The name of the run output</span></span>

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

### <span data-ttu-id="43099-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="43099-128">-SubscriptionId</span></span>
<span data-ttu-id="43099-129">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="43099-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="43099-130">구독 Id는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="43099-130">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="43099-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43099-131">CommonParameters</span></span>
<span data-ttu-id="43099-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="43099-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43099-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="43099-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43099-134">입력</span><span class="sxs-lookup"><span data-stu-id="43099-134">INPUTS</span></span>

### <span data-ttu-id="43099-135">IImageBuilderIdentity-. i g a.</span><span class="sxs-lookup"><span data-stu-id="43099-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="43099-136">출력</span><span class="sxs-lookup"><span data-stu-id="43099-136">OUTPUTS</span></span>

### <span data-ttu-id="43099-137">Api20200214. a g a. IRunOutput.</span><span class="sxs-lookup"><span data-stu-id="43099-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="43099-138">상속자</span><span class="sxs-lookup"><span data-stu-id="43099-138">NOTES</span></span>

<span data-ttu-id="43099-139">별칭과</span><span class="sxs-lookup"><span data-stu-id="43099-139">ALIASES</span></span>

<span data-ttu-id="43099-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="43099-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="43099-141">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="43099-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="43099-142">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="43099-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="43099-143">INPUTOBJECT <IImageBuilderIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="43099-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="43099-144">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="43099-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="43099-145">`[ImageTemplateName <String>]`: 이미지 서식 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43099-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="43099-146">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43099-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="43099-147">`[RunOutputName <String>]`: 실행 출력의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43099-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="43099-148">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="43099-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="43099-149">구독 Id는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="43099-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="43099-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43099-150">RELATED LINKS</span></span>

