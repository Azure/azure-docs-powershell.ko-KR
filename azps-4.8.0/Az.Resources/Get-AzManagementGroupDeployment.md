---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 79eeb4e1725adf38b2f1dc70fe181280312fa1e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214227"
---
# <span data-ttu-id="fe722-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="fe722-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="fe722-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe722-102">SYNOPSIS</span></span>
<span data-ttu-id="fe722-103">관리 그룹에서 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="fe722-103">Get deployment at a management group</span></span>

## <span data-ttu-id="fe722-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fe722-104">SYNTAX</span></span>

### <span data-ttu-id="fe722-105">GetByDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="fe722-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe722-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="fe722-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe722-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fe722-107">DESCRIPTION</span></span>
<span data-ttu-id="fe722-108">**AzManagementGroupDeployment** cmdlet은 a 관리 그룹에서 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe722-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="fe722-109">*이름* 또는 *Id* 매개 변수를 지정 하 여 결과를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe722-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="fe722-110">기본적으로 **Get-AzManagementGroupDeployment** 는 관리 그룹의 모든 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe722-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="fe722-111">예제의</span><span class="sxs-lookup"><span data-stu-id="fe722-111">EXAMPLES</span></span>

### <span data-ttu-id="fe722-112">예제 1: 관리 그룹에서 모든 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="fe722-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="fe722-113">이 명령은 관리 그룹 "myMG"에 있는 모든 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe722-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="fe722-114">예제 2: 이름으로 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="fe722-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="fe722-115">이 명령은 관리 그룹 "myMG"에서 "Deploy01" 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe722-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="fe722-116">**새 AzManagementGroupDeployment** cmdlet을 사용 하 여 배포를 만들 때 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe722-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="fe722-117">이름을 할당 하지 않으면 cmdlet은 배포를 만드는 데 사용 되는 템플릿을 기반으로 하는 기본 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe722-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="fe722-118">예제 3: ID를 기준으로 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="fe722-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="fe722-119">이 명령은 관리 그룹 "myMG"에서 "Deploy01" 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe722-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="fe722-120">변수</span><span class="sxs-lookup"><span data-stu-id="fe722-120">PARAMETERS</span></span>

### <span data-ttu-id="fe722-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fe722-121">-ApiVersion</span></span>
<span data-ttu-id="fe722-122">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fe722-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="fe722-123">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fe722-123">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe722-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe722-124">-DefaultProfile</span></span>
<span data-ttu-id="fe722-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fe722-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe722-126">-Id</span><span class="sxs-lookup"><span data-stu-id="fe722-126">-Id</span></span>
<span data-ttu-id="fe722-127">배포의 정규화 된 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="fe722-127">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="fe722-128">예:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="fe722-128">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe722-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="fe722-129">-ManagementGroupId</span></span>
<span data-ttu-id="fe722-130">관리 그룹 id입니다.</span><span class="sxs-lookup"><span data-stu-id="fe722-130">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe722-131">-이름</span><span class="sxs-lookup"><span data-stu-id="fe722-131">-Name</span></span>
<span data-ttu-id="fe722-132">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fe722-132">The name of deployment.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe722-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="fe722-133">-Pre</span></span>
<span data-ttu-id="fe722-134">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fe722-134">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe722-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe722-135">CommonParameters</span></span>
<span data-ttu-id="fe722-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe722-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe722-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fe722-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe722-138">입력</span><span class="sxs-lookup"><span data-stu-id="fe722-138">INPUTS</span></span>

### <span data-ttu-id="fe722-139">않아야</span><span class="sxs-lookup"><span data-stu-id="fe722-139">None</span></span>

## <span data-ttu-id="fe722-140">출력</span><span class="sxs-lookup"><span data-stu-id="fe722-140">OUTPUTS</span></span>

### <span data-ttu-id="fe722-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="fe722-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="fe722-142">상속자</span><span class="sxs-lookup"><span data-stu-id="fe722-142">NOTES</span></span>

## <span data-ttu-id="fe722-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe722-143">RELATED LINKS</span></span>
