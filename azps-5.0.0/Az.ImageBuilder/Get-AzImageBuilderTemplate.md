---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
ms.openlocfilehash: d159a59f6fb94523868b4aa6109553900f1b289d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304031"
---
# <span data-ttu-id="9b443-101">Get-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="9b443-101">Get-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="9b443-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b443-102">SYNOPSIS</span></span>
<span data-ttu-id="9b443-103">가상 컴퓨터 이미지 서식 파일에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="9b443-103">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="9b443-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b443-104">SYNTAX</span></span>

### <span data-ttu-id="9b443-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="9b443-105">List (Default)</span></span>
```
Get-AzImageBuilderTemplate [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9b443-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="9b443-106">Get</span></span>
```
Get-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9b443-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9b443-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b443-108">List1</span><span class="sxs-lookup"><span data-stu-id="9b443-108">List1</span></span>
```
Get-AzImageBuilderTemplate -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9b443-109">설명은</span><span class="sxs-lookup"><span data-stu-id="9b443-109">DESCRIPTION</span></span>
<span data-ttu-id="9b443-110">가상 컴퓨터 이미지 서식 파일에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="9b443-110">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="9b443-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9b443-111">EXAMPLES</span></span>

### <span data-ttu-id="9b443-112">예제 1: 구독에서 모든 서식 파일 나열</span><span class="sxs-lookup"><span data-stu-id="9b443-112">Example 1: List all template under a subscription</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate

Location Name                      Type
-------- ----                      ----
eastus   HelloImageTemplateLinux01 Microsoft.VirtualMachineImages/imageTemplates
eastus   lucas-imagetemplate       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder         Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="9b443-113">이 명령은 구독 아래의 모든 서식 파일을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b443-113">This command lists all template under a subscription.</span></span>

### <span data-ttu-id="9b443-114">예제 2: 자원 그룹 아래에 모든 서식 파일 나열</span><span class="sxs-lookup"><span data-stu-id="9b443-114">Example 2: List all template under a resource group</span></span>
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

<span data-ttu-id="9b443-115">이 명령은 리소스 그룹 아래에 모든 서식 파일을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b443-115">This command lists all template under a resource group.</span></span>

### <span data-ttu-id="9b443-116">예제 3: 리소스 그룹에서 서식 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="9b443-116">Example 3: Get a template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                Type
-------- ----                ----
eastus   lucas-imagetemplate Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="9b443-117">이 명령은 리소스 그룹의 템플릿을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b443-117">This command gets a template under a resource group.</span></span>

### <span data-ttu-id="9b443-118">예제 4: 리소스 그룹에서 서식 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="9b443-118">Example 4: Get a template under a resource group</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -ImageTemplateName template-name-ep5z7v
PS C:\> Get-AzImageBuilderTemplate -InputObject $template

Location Name                 Type
-------- ----                 ----
eastus   template-name-ep5z7v Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="9b443-119">이 명령은 리소스 그룹의 템플릿을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b443-119">This command gets a template under a resource group.</span></span>

## <span data-ttu-id="9b443-120">변수</span><span class="sxs-lookup"><span data-stu-id="9b443-120">PARAMETERS</span></span>

### <span data-ttu-id="9b443-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b443-121">-DefaultProfile</span></span>
<span data-ttu-id="9b443-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b443-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b443-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="9b443-123">-ImageTemplateName</span></span>
<span data-ttu-id="9b443-124">이미지 서식 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b443-124">The name of the image Template</span></span>

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

### <span data-ttu-id="9b443-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b443-125">-InputObject</span></span>
<span data-ttu-id="9b443-126">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b443-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9b443-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b443-127">-ResourceGroupName</span></span>
<span data-ttu-id="9b443-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b443-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="9b443-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9b443-129">-SubscriptionId</span></span>
<span data-ttu-id="9b443-130">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="9b443-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9b443-131">구독 Id는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b443-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9b443-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b443-132">CommonParameters</span></span>
<span data-ttu-id="9b443-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b443-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b443-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9b443-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b443-135">입력</span><span class="sxs-lookup"><span data-stu-id="9b443-135">INPUTS</span></span>

### <span data-ttu-id="9b443-136">IImageBuilderIdentity-. i g a.</span><span class="sxs-lookup"><span data-stu-id="9b443-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="9b443-137">출력</span><span class="sxs-lookup"><span data-stu-id="9b443-137">OUTPUTS</span></span>

### <span data-ttu-id="9b443-138">Api20200214. IImageTemplate에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9b443-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="9b443-139">상속자</span><span class="sxs-lookup"><span data-stu-id="9b443-139">NOTES</span></span>

<span data-ttu-id="9b443-140">별칭과</span><span class="sxs-lookup"><span data-stu-id="9b443-140">ALIASES</span></span>

<span data-ttu-id="9b443-141">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="9b443-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9b443-142">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b443-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9b443-143">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="9b443-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9b443-144">INPUTOBJECT <IImageBuilderIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9b443-144">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9b443-145">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="9b443-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9b443-146">`[ImageTemplateName <String>]`: 이미지 서식 파일의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b443-146">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="9b443-147">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b443-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="9b443-148">`[RunOutputName <String>]`: 실행 출력의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b443-148">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="9b443-149">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="9b443-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9b443-150">구독 Id는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b443-150">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9b443-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b443-151">RELATED LINKS</span></span>

