---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: c3218141e495bb92216e254830ddaa7dd7a0a0c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043778"
---
# <span data-ttu-id="7e774-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="7e774-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="7e774-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e774-102">SYNOPSIS</span></span>
<span data-ttu-id="7e774-103">테 넌 트 범위에서 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="7e774-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="7e774-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e774-104">SYNTAX</span></span>

### <span data-ttu-id="7e774-105">GetByDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="7e774-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e774-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="7e774-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e774-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7e774-107">DESCRIPTION</span></span>
<span data-ttu-id="7e774-108">**AzTenantDeployment** cmdlet은 테 넌 트 범위에서 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e774-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="7e774-109">*이름* 또는 *Id* 매개 변수를 지정 하 여 결과를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e774-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="7e774-110">기본적으로 **AzTenantDeployment** 는 테 넌 트 범위에서 모든 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e774-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="7e774-111">예제의</span><span class="sxs-lookup"><span data-stu-id="7e774-111">EXAMPLES</span></span>

### <span data-ttu-id="7e774-112">예제 1: 테 넌 트 범위에서 모든 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="7e774-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="7e774-113">이 명령은 현재 테 넌 트 범위에 있는 모든 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e774-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="7e774-114">예제 2: 이름으로 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="7e774-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="7e774-115">이 명령은 현재 테 넌 트 범위에서 "Deploy01" 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e774-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="7e774-116">**새 AzTenantDeployment** cmdlet을 사용 하 여 배포를 만들 때 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7e774-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="7e774-117">이름을 할당 하지 않으면 cmdlet은 배포를 만드는 데 사용 되는 템플릿을 기반으로 하는 기본 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e774-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="7e774-118">예제 3: ID를 기준으로 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="7e774-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="7e774-119">이 명령은 테 넌 트 범위에서 "Deploy01" 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7e774-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="7e774-120">변수</span><span class="sxs-lookup"><span data-stu-id="7e774-120">PARAMETERS</span></span>

### <span data-ttu-id="7e774-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7e774-121">-ApiVersion</span></span>
<span data-ttu-id="7e774-122">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7e774-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="7e774-123">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e774-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="7e774-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e774-124">-DefaultProfile</span></span>
<span data-ttu-id="7e774-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e774-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e774-126">-Id</span><span class="sxs-lookup"><span data-stu-id="7e774-126">-Id</span></span>
<span data-ttu-id="7e774-127">배포의 정규화 된 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="7e774-127">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="7e774-128">예:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="7e774-128">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="7e774-129">-이름</span><span class="sxs-lookup"><span data-stu-id="7e774-129">-Name</span></span>
<span data-ttu-id="7e774-130">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e774-130">The name of deployment.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e774-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="7e774-131">-Pre</span></span>
<span data-ttu-id="7e774-132">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7e774-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7e774-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e774-133">CommonParameters</span></span>
<span data-ttu-id="7e774-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e774-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e774-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7e774-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e774-136">입력</span><span class="sxs-lookup"><span data-stu-id="7e774-136">INPUTS</span></span>

### <span data-ttu-id="7e774-137">않아야</span><span class="sxs-lookup"><span data-stu-id="7e774-137">None</span></span>

## <span data-ttu-id="7e774-138">출력</span><span class="sxs-lookup"><span data-stu-id="7e774-138">OUTPUTS</span></span>

### <span data-ttu-id="7e774-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="7e774-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="7e774-140">상속자</span><span class="sxs-lookup"><span data-stu-id="7e774-140">NOTES</span></span>

## <span data-ttu-id="7e774-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e774-141">RELATED LINKS</span></span>
