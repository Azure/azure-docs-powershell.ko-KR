---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: a1cfbf131286a8bae7b8837f798c32b83d566b2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192764"
---
# <span data-ttu-id="7ca76-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="7ca76-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="7ca76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ca76-102">SYNOPSIS</span></span>
<span data-ttu-id="7ca76-103">테넌트 범위에서 배포하기</span><span class="sxs-lookup"><span data-stu-id="7ca76-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="7ca76-104">구문</span><span class="sxs-lookup"><span data-stu-id="7ca76-104">SYNTAX</span></span>

### <span data-ttu-id="7ca76-105">GetByDeploymentName(기본값)</span><span class="sxs-lookup"><span data-stu-id="7ca76-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ca76-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="7ca76-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ca76-107">설명</span><span class="sxs-lookup"><span data-stu-id="7ca76-107">DESCRIPTION</span></span>
<span data-ttu-id="7ca76-108">**Get-AzTenantDeployment** cmdlet은 테넌트 범위에서 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ca76-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="7ca76-109">결과를 필터링할 *이름* *또는 ID* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ca76-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="7ca76-110">기본적으로 **Get-AzTenantDeployment는** 테넌트 범위에서 모든 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ca76-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="7ca76-111">예제</span><span class="sxs-lookup"><span data-stu-id="7ca76-111">EXAMPLES</span></span>

### <span data-ttu-id="7ca76-112">예제 1: 테넌트 범위에서 모든 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ca76-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="7ca76-113">이 명령은 현재 테넌트 범위의 모든 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ca76-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="7ca76-114">예제 2: 이름으로 배포하기</span><span class="sxs-lookup"><span data-stu-id="7ca76-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="7ca76-115">이 명령은 현재 테넌트 범위에서 "Deploy01" 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ca76-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="7ca76-116">**New-AzTenantDeployment** cmdlet을 사용하여 배포를 만들 때 이름을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ca76-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="7ca76-117">이름을 할당하지 않는 경우 cmdlet은 배포를 만드는 데 사용되는 템플릿에 따라 기본 이름을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="7ca76-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="7ca76-118">예제 3: ID로 배포하기</span><span class="sxs-lookup"><span data-stu-id="7ca76-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="7ca76-119">이 명령은 테넌트 범위에서 "Deploy01" 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ca76-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="7ca76-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ca76-120">PARAMETERS</span></span>

### <span data-ttu-id="7ca76-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ca76-121">-DefaultProfile</span></span>
<span data-ttu-id="7ca76-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7ca76-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ca76-123">-Id</span><span class="sxs-lookup"><span data-stu-id="7ca76-123">-Id</span></span>
<span data-ttu-id="7ca76-124">배포의 정식 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7ca76-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="7ca76-125">예: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="7ca76-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="7ca76-126">-Name</span><span class="sxs-lookup"><span data-stu-id="7ca76-126">-Name</span></span>
<span data-ttu-id="7ca76-127">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ca76-127">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ca76-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="7ca76-128">-Pre</span></span>
<span data-ttu-id="7ca76-129">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7ca76-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7ca76-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ca76-130">CommonParameters</span></span>
<span data-ttu-id="7ca76-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ca76-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ca76-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7ca76-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ca76-133">입력</span><span class="sxs-lookup"><span data-stu-id="7ca76-133">INPUTS</span></span>

### <span data-ttu-id="7ca76-134">없음</span><span class="sxs-lookup"><span data-stu-id="7ca76-134">None</span></span>

## <span data-ttu-id="7ca76-135">출력</span><span class="sxs-lookup"><span data-stu-id="7ca76-135">OUTPUTS</span></span>

### <span data-ttu-id="7ca76-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSD</span><span class="sxs-lookup"><span data-stu-id="7ca76-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="7ca76-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7ca76-137">NOTES</span></span>

## <span data-ttu-id="7ca76-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ca76-138">RELATED LINKS</span></span>
