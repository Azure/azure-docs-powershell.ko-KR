---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
ms.openlocfilehash: d159a59f6fb94523868b4aa6109553900f1b289d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492906"
---
# <span data-ttu-id="43d0a-101">Get-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="43d0a-101">Get-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="43d0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43d0a-102">SYNOPSIS</span></span>
<span data-ttu-id="43d0a-103">가상 머신 이미지 템플릿에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="43d0a-103">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="43d0a-104">구문</span><span class="sxs-lookup"><span data-stu-id="43d0a-104">SYNTAX</span></span>

### <span data-ttu-id="43d0a-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="43d0a-105">List (Default)</span></span>
```
Get-AzImageBuilderTemplate [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43d0a-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="43d0a-106">Get</span></span>
```
Get-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="43d0a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="43d0a-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="43d0a-108">List1</span><span class="sxs-lookup"><span data-stu-id="43d0a-108">List1</span></span>
```
Get-AzImageBuilderTemplate -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="43d0a-109">설명</span><span class="sxs-lookup"><span data-stu-id="43d0a-109">DESCRIPTION</span></span>
<span data-ttu-id="43d0a-110">가상 머신 이미지 템플릿에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="43d0a-110">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="43d0a-111">예제</span><span class="sxs-lookup"><span data-stu-id="43d0a-111">EXAMPLES</span></span>

### <span data-ttu-id="43d0a-112">예제 1: 구독의 모든 템플릿 나열</span><span class="sxs-lookup"><span data-stu-id="43d0a-112">Example 1: List all template under a subscription</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate

Location Name                      Type
-------- ----                      ----
eastus   HelloImageTemplateLinux01 Microsoft.VirtualMachineImages/imageTemplates
eastus   lucas-imagetemplate       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder         Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="43d0a-113">이 명령은 구독의 모든 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="43d0a-113">This command lists all template under a subscription.</span></span>

### <span data-ttu-id="43d0a-114">예제 2: 리소스 그룹 아래에 모든 템플릿 나열</span><span class="sxs-lookup"><span data-stu-id="43d0a-114">Example 2: List all template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                       Type
-------- ----                       ----
eastus   HelloImageTemplateLinux01  Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ax01b7       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ep5z7v       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-klcuav       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-u7gjqx       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder          Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-managedimg-managedimg Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-platform-managed      Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-shareimg-managedimg   Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="43d0a-115">이 명령은 리소스 그룹 아래에 있는 모든 템플릿을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="43d0a-115">This command lists all template under a resource group.</span></span>

### <span data-ttu-id="43d0a-116">예제 3: 리소스 그룹에서 템플릿을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43d0a-116">Example 3: Get a template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                Type
-------- ----                ----
eastus   lucas-imagetemplate Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="43d0a-117">이 명령은 리소스 그룹 아래에서 템플릿을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43d0a-117">This command gets a template under a resource group.</span></span>

### <span data-ttu-id="43d0a-118">예제 4: 리소스 그룹에서 템플릿을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43d0a-118">Example 4: Get a template under a resource group</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -ImageTemplateName template-name-ep5z7v
PS C:\> Get-AzImageBuilderTemplate -InputObject $template

Location Name                 Type
-------- ----                 ----
eastus   template-name-ep5z7v Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="43d0a-119">이 명령은 리소스 그룹 아래에서 템플릿을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43d0a-119">This command gets a template under a resource group.</span></span>

## <span data-ttu-id="43d0a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43d0a-120">PARAMETERS</span></span>

### <span data-ttu-id="43d0a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43d0a-121">-DefaultProfile</span></span>
<span data-ttu-id="43d0a-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="43d0a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43d0a-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="43d0a-123">-ImageTemplateName</span></span>
<span data-ttu-id="43d0a-124">이미지 템플릿의 이름</span><span class="sxs-lookup"><span data-stu-id="43d0a-124">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d0a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43d0a-125">-InputObject</span></span>
<span data-ttu-id="43d0a-126">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="43d0a-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="43d0a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43d0a-127">-ResourceGroupName</span></span>
<span data-ttu-id="43d0a-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43d0a-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d0a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="43d0a-129">-SubscriptionId</span></span>
<span data-ttu-id="43d0a-130">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="43d0a-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="43d0a-131">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="43d0a-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d0a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d0a-132">CommonParameters</span></span>
<span data-ttu-id="43d0a-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="43d0a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d0a-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="43d0a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d0a-135">입력</span><span class="sxs-lookup"><span data-stu-id="43d0a-135">INPUTS</span></span>

### <span data-ttu-id="43d0a-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="43d0a-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="43d0a-137">출력</span><span class="sxs-lookup"><span data-stu-id="43d0a-137">OUTPUTS</span></span>

### <span data-ttu-id="43d0a-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="43d0a-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="43d0a-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="43d0a-139">NOTES</span></span>

<span data-ttu-id="43d0a-140">별칭</span><span class="sxs-lookup"><span data-stu-id="43d0a-140">ALIASES</span></span>

<span data-ttu-id="43d0a-141">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="43d0a-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="43d0a-142">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="43d0a-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="43d0a-143">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="43d0a-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="43d0a-144">INPUTOBJECT: <IImageBuilderIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="43d0a-144">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="43d0a-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="43d0a-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="43d0a-146">`[ImageTemplateName <String>]`: 이미지 템플릿의 이름</span><span class="sxs-lookup"><span data-stu-id="43d0a-146">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="43d0a-147">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43d0a-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="43d0a-148">`[RunOutputName <String>]`: 실행 출력의 이름</span><span class="sxs-lookup"><span data-stu-id="43d0a-148">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="43d0a-149">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="43d0a-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="43d0a-150">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="43d0a-150">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="43d0a-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43d0a-151">RELATED LINKS</span></span>

