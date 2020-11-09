---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 6c873dfda563c24104abc5e89b00569358084d96
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308936"
---
# <span data-ttu-id="4b5cf-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4b5cf-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="4b5cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b5cf-102">SYNOPSIS</span></span>
<span data-ttu-id="4b5cf-103">관리 그룹에서 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="4b5cf-103">Get deployment at a management group</span></span>

## <span data-ttu-id="4b5cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4b5cf-104">SYNTAX</span></span>

### <span data-ttu-id="4b5cf-105">GetByDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="4b5cf-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b5cf-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="4b5cf-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b5cf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4b5cf-107">DESCRIPTION</span></span>
<span data-ttu-id="4b5cf-108">**AzManagementGroupDeployment** cmdlet은 a 관리 그룹에서 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4b5cf-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="4b5cf-109">*이름* 또는 *Id* 매개 변수를 지정 하 여 결과를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5cf-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="4b5cf-110">기본적으로 **Get-AzManagementGroupDeployment** 는 관리 그룹의 모든 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4b5cf-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="4b5cf-111">예제의</span><span class="sxs-lookup"><span data-stu-id="4b5cf-111">EXAMPLES</span></span>

### <span data-ttu-id="4b5cf-112">예제 1: 관리 그룹에서 모든 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="4b5cf-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="4b5cf-113">이 명령은 관리 그룹 "myMG"에 있는 모든 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4b5cf-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="4b5cf-114">예제 2: 이름으로 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="4b5cf-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="4b5cf-115">이 명령은 관리 그룹 "myMG"에서 "Deploy01" 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4b5cf-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="4b5cf-116">**새 AzManagementGroupDeployment** cmdlet을 사용 하 여 배포를 만들 때 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b5cf-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="4b5cf-117">이름을 할당 하지 않으면 cmdlet은 배포를 만드는 데 사용 되는 템플릿을 기반으로 하는 기본 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5cf-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="4b5cf-118">예제 3: ID를 기준으로 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="4b5cf-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="4b5cf-119">이 명령은 관리 그룹 "myMG"에서 "Deploy01" 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4b5cf-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="4b5cf-120">변수</span><span class="sxs-lookup"><span data-stu-id="4b5cf-120">PARAMETERS</span></span>

### <span data-ttu-id="4b5cf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b5cf-121">-DefaultProfile</span></span>
<span data-ttu-id="4b5cf-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b5cf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b5cf-123">-Id</span><span class="sxs-lookup"><span data-stu-id="4b5cf-123">-Id</span></span>
<span data-ttu-id="4b5cf-124">배포의 정규화 된 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="4b5cf-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="4b5cf-125">예:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="4b5cf-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="4b5cf-126">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="4b5cf-126">-ManagementGroupId</span></span>
<span data-ttu-id="4b5cf-127">관리 그룹 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4b5cf-127">The management group id.</span></span>

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

### <span data-ttu-id="4b5cf-128">-이름</span><span class="sxs-lookup"><span data-stu-id="4b5cf-128">-Name</span></span>
<span data-ttu-id="4b5cf-129">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b5cf-129">The name of deployment.</span></span>

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

### <span data-ttu-id="4b5cf-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="4b5cf-130">-Pre</span></span>
<span data-ttu-id="4b5cf-131">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4b5cf-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4b5cf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b5cf-132">CommonParameters</span></span>
<span data-ttu-id="4b5cf-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b5cf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b5cf-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4b5cf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b5cf-135">입력</span><span class="sxs-lookup"><span data-stu-id="4b5cf-135">INPUTS</span></span>

### <span data-ttu-id="4b5cf-136">않아야</span><span class="sxs-lookup"><span data-stu-id="4b5cf-136">None</span></span>

## <span data-ttu-id="4b5cf-137">출력</span><span class="sxs-lookup"><span data-stu-id="4b5cf-137">OUTPUTS</span></span>

### <span data-ttu-id="4b5cf-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="4b5cf-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="4b5cf-139">상속자</span><span class="sxs-lookup"><span data-stu-id="4b5cf-139">NOTES</span></span>

## <span data-ttu-id="4b5cf-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b5cf-140">RELATED LINKS</span></span>
