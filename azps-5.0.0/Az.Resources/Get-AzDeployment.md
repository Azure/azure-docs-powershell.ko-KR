---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 75ebbe0eedd9aad396500701d5e94efff76069f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215909"
---
# <span data-ttu-id="346fc-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="346fc-101">Get-AzDeployment</span></span>

## <span data-ttu-id="346fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="346fc-102">SYNOPSIS</span></span>
<span data-ttu-id="346fc-103">배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="346fc-103">Get deployment</span></span>

## <span data-ttu-id="346fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="346fc-104">SYNTAX</span></span>

### <span data-ttu-id="346fc-105">GetByDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="346fc-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="346fc-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="346fc-106">GetByDeploymentId</span></span>
```
Get-AzDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="346fc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="346fc-107">DESCRIPTION</span></span>
<span data-ttu-id="346fc-108">**Get-AzDeployment** cmdlet은 현재 구독 범위에서 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="346fc-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="346fc-109">*이름* 또는 *Id* 매개 변수를 지정 하 여 결과를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="346fc-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="346fc-110">기본적으로 **Get-AzDeployment** 는 현재 구독 범위에서 모든 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="346fc-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="346fc-111">예제의</span><span class="sxs-lookup"><span data-stu-id="346fc-111">EXAMPLES</span></span>

### <span data-ttu-id="346fc-112">예제 1: 구독 범위에서 모든 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="346fc-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="346fc-113">이 명령은 현재 구독 범위에서 모든 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="346fc-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="346fc-114">예제 2: 이름으로 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="346fc-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="346fc-115">이 명령은 현재 구독 범위에서 DeployRoles01 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="346fc-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="346fc-116">**새 AzDeployment** cmdlet을 사용 하 여 배포를 만들 때 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="346fc-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="346fc-117">이름을 할당 하지 않으면 cmdlet은 배포를 만드는 데 사용 되는 템플릿을 기반으로 하는 기본 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="346fc-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="346fc-118">변수</span><span class="sxs-lookup"><span data-stu-id="346fc-118">PARAMETERS</span></span>

### <span data-ttu-id="346fc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="346fc-119">-DefaultProfile</span></span>
<span data-ttu-id="346fc-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="346fc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="346fc-121">-Id</span><span class="sxs-lookup"><span data-stu-id="346fc-121">-Id</span></span>
<span data-ttu-id="346fc-122">배포의 정규화 된 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="346fc-122">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="346fc-123">예:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="346fc-123">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="346fc-124">-이름</span><span class="sxs-lookup"><span data-stu-id="346fc-124">-Name</span></span>
<span data-ttu-id="346fc-125">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="346fc-125">The name of deployment.</span></span>

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

### <span data-ttu-id="346fc-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="346fc-126">-Pre</span></span>
<span data-ttu-id="346fc-127">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="346fc-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="346fc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="346fc-128">CommonParameters</span></span>
<span data-ttu-id="346fc-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="346fc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="346fc-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="346fc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="346fc-131">입력</span><span class="sxs-lookup"><span data-stu-id="346fc-131">INPUTS</span></span>

### <span data-ttu-id="346fc-132">않아야</span><span class="sxs-lookup"><span data-stu-id="346fc-132">None</span></span>

## <span data-ttu-id="346fc-133">출력</span><span class="sxs-lookup"><span data-stu-id="346fc-133">OUTPUTS</span></span>

### <span data-ttu-id="346fc-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="346fc-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="346fc-135">상속자</span><span class="sxs-lookup"><span data-stu-id="346fc-135">NOTES</span></span>

## <span data-ttu-id="346fc-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="346fc-136">RELATED LINKS</span></span>
