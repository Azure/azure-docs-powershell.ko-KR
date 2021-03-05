---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 73a124070dd329daff52ec5c0de16fb55ef74354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973568"
---
# <span data-ttu-id="862a8-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="862a8-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="862a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="862a8-102">SYNOPSIS</span></span>
<span data-ttu-id="862a8-103">관리 그룹에서 배포하기</span><span class="sxs-lookup"><span data-stu-id="862a8-103">Get deployment at a management group</span></span>

## <span data-ttu-id="862a8-104">구문</span><span class="sxs-lookup"><span data-stu-id="862a8-104">SYNTAX</span></span>

### <span data-ttu-id="862a8-105">GetByDeploymentName(기본값)</span><span class="sxs-lookup"><span data-stu-id="862a8-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="862a8-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="862a8-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="862a8-107">설명</span><span class="sxs-lookup"><span data-stu-id="862a8-107">DESCRIPTION</span></span>
<span data-ttu-id="862a8-108">**Get-AzManagementGroupDeployment** cmdlet은 관리 그룹에서 배포를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="862a8-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="862a8-109">결과를 필터링하기 위해 *이름* 또는 *ID 매개* 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="862a8-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="862a8-110">기본적으로 **Get-AzManagementGroupDeployment는** 관리 그룹의 모든 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="862a8-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="862a8-111">예제</span><span class="sxs-lookup"><span data-stu-id="862a8-111">EXAMPLES</span></span>

### <span data-ttu-id="862a8-112">예제 1: 관리 그룹의 모든 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="862a8-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="862a8-113">이 명령은 관리 그룹 "myMG"에서 모든 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="862a8-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="862a8-114">예제 2: 이름으로 배포하기</span><span class="sxs-lookup"><span data-stu-id="862a8-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="862a8-115">이 명령은 관리 그룹 "myMG"에서 "Deploy01" 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="862a8-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="862a8-116">**New-AzManagementGroupDeployment** cmdlet을 사용하여 배포에 이름을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="862a8-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="862a8-117">이름을 할당하지 않는 경우 cmdlet은 배포를 만드는 데 사용되는 템플릿을 기반으로 기본 이름을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="862a8-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="862a8-118">예제 3: ID로 배포하기</span><span class="sxs-lookup"><span data-stu-id="862a8-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="862a8-119">이 명령은 관리 그룹 "myMG"에서 "Deploy01" 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="862a8-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="862a8-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="862a8-120">PARAMETERS</span></span>

### <span data-ttu-id="862a8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="862a8-121">-DefaultProfile</span></span>
<span data-ttu-id="862a8-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="862a8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862a8-123">-Id</span><span class="sxs-lookup"><span data-stu-id="862a8-123">-Id</span></span>
<span data-ttu-id="862a8-124">배포의 완전히 자격을 갖춘 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="862a8-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="862a8-125">예제: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="862a8-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862a8-126">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="862a8-126">-ManagementGroupId</span></span>
<span data-ttu-id="862a8-127">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="862a8-127">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862a8-128">-Name</span><span class="sxs-lookup"><span data-stu-id="862a8-128">-Name</span></span>
<span data-ttu-id="862a8-129">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="862a8-129">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862a8-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="862a8-130">-Pre</span></span>
<span data-ttu-id="862a8-131">설정하면 cmdlet이 사용할 버전을 자동으로 결정할 때 미리 릴리스 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="862a8-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="862a8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="862a8-132">CommonParameters</span></span>
<span data-ttu-id="862a8-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="862a8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="862a8-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="862a8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="862a8-135">입력</span><span class="sxs-lookup"><span data-stu-id="862a8-135">INPUTS</span></span>

### <span data-ttu-id="862a8-136">없음</span><span class="sxs-lookup"><span data-stu-id="862a8-136">None</span></span>

## <span data-ttu-id="862a8-137">출력</span><span class="sxs-lookup"><span data-stu-id="862a8-137">OUTPUTS</span></span>

### <span data-ttu-id="862a8-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDMicrosoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSD</span><span class="sxs-lookup"><span data-stu-id="862a8-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="862a8-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="862a8-139">NOTES</span></span>

## <span data-ttu-id="862a8-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="862a8-140">RELATED LINKS</span></span>
