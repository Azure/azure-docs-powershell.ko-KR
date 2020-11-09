---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: a1cfbf131286a8bae7b8837f798c32b83d566b2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308810"
---
# <span data-ttu-id="cf02a-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="cf02a-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="cf02a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf02a-102">SYNOPSIS</span></span>
<span data-ttu-id="cf02a-103">테 넌 트 범위에서 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="cf02a-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="cf02a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cf02a-104">SYNTAX</span></span>

### <span data-ttu-id="cf02a-105">GetByDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="cf02a-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf02a-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="cf02a-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf02a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cf02a-107">DESCRIPTION</span></span>
<span data-ttu-id="cf02a-108">**AzTenantDeployment** cmdlet은 테 넌 트 범위에서 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf02a-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="cf02a-109">*이름* 또는 *Id* 매개 변수를 지정 하 여 결과를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf02a-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="cf02a-110">기본적으로 **AzTenantDeployment** 는 테 넌 트 범위에서 모든 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf02a-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="cf02a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="cf02a-111">EXAMPLES</span></span>

### <span data-ttu-id="cf02a-112">예제 1: 테 넌 트 범위에서 모든 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="cf02a-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="cf02a-113">이 명령은 현재 테 넌 트 범위에 있는 모든 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf02a-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="cf02a-114">예제 2: 이름으로 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="cf02a-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="cf02a-115">이 명령은 현재 테 넌 트 범위에서 "Deploy01" 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf02a-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="cf02a-116">**새 AzTenantDeployment** cmdlet을 사용 하 여 배포를 만들 때 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cf02a-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="cf02a-117">이름을 할당 하지 않으면 cmdlet은 배포를 만드는 데 사용 되는 템플릿을 기반으로 하는 기본 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf02a-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="cf02a-118">예제 3: ID를 기준으로 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="cf02a-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="cf02a-119">이 명령은 테 넌 트 범위에서 "Deploy01" 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cf02a-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="cf02a-120">변수</span><span class="sxs-lookup"><span data-stu-id="cf02a-120">PARAMETERS</span></span>

### <span data-ttu-id="cf02a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf02a-121">-DefaultProfile</span></span>
<span data-ttu-id="cf02a-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cf02a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf02a-123">-Id</span><span class="sxs-lookup"><span data-stu-id="cf02a-123">-Id</span></span>
<span data-ttu-id="cf02a-124">배포의 정규화 된 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="cf02a-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="cf02a-125">예:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="cf02a-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="cf02a-126">-이름</span><span class="sxs-lookup"><span data-stu-id="cf02a-126">-Name</span></span>
<span data-ttu-id="cf02a-127">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf02a-127">The name of deployment.</span></span>

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

### <span data-ttu-id="cf02a-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="cf02a-128">-Pre</span></span>
<span data-ttu-id="cf02a-129">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cf02a-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="cf02a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf02a-130">CommonParameters</span></span>
<span data-ttu-id="cf02a-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf02a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf02a-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cf02a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf02a-133">입력</span><span class="sxs-lookup"><span data-stu-id="cf02a-133">INPUTS</span></span>

### <span data-ttu-id="cf02a-134">않아야</span><span class="sxs-lookup"><span data-stu-id="cf02a-134">None</span></span>

## <span data-ttu-id="cf02a-135">출력</span><span class="sxs-lookup"><span data-stu-id="cf02a-135">OUTPUTS</span></span>

### <span data-ttu-id="cf02a-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="cf02a-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="cf02a-137">상속자</span><span class="sxs-lookup"><span data-stu-id="cf02a-137">NOTES</span></span>

## <span data-ttu-id="cf02a-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf02a-138">RELATED LINKS</span></span>
