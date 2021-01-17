---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 75ebbe0eedd9aad396500701d5e94efff76069f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490576"
---
# <span data-ttu-id="0119a-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0119a-101">Get-AzDeployment</span></span>

## <span data-ttu-id="0119a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0119a-102">SYNOPSIS</span></span>
<span data-ttu-id="0119a-103">배포를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0119a-103">Get deployment</span></span>

## <span data-ttu-id="0119a-104">구문</span><span class="sxs-lookup"><span data-stu-id="0119a-104">SYNTAX</span></span>

### <span data-ttu-id="0119a-105">GetByDeploymentName(기본값)</span><span class="sxs-lookup"><span data-stu-id="0119a-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0119a-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="0119a-106">GetByDeploymentId</span></span>
```
Get-AzDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0119a-107">설명</span><span class="sxs-lookup"><span data-stu-id="0119a-107">DESCRIPTION</span></span>
<span data-ttu-id="0119a-108">**Get-AzDeployment** cmdlet은 현재 구독 범위에서 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0119a-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="0119a-109">결과를 필터링할 *이름* 또는 *ID* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0119a-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="0119a-110">기본적으로 **Get-AzDeployment는** 현재 구독 범위에서 모든 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0119a-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="0119a-111">예제</span><span class="sxs-lookup"><span data-stu-id="0119a-111">EXAMPLES</span></span>

### <span data-ttu-id="0119a-112">예제 1: 구독 범위에서 모든 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0119a-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="0119a-113">이 명령은 현재 구독 범위의 모든 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0119a-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="0119a-114">예제 2: 이름으로 배포하기</span><span class="sxs-lookup"><span data-stu-id="0119a-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="0119a-115">이 명령은 현재 구독 범위에서 DeployRoles01 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0119a-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="0119a-116">**New-AzDeployment** cmdlet을 사용하여 배포를 만들 때 이름을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0119a-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="0119a-117">이름을 할당하지 않는 경우 cmdlet은 배포를 만드는 데 사용되는 템플릿에 따라 기본 이름을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0119a-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="0119a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0119a-118">PARAMETERS</span></span>

### <span data-ttu-id="0119a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0119a-119">-DefaultProfile</span></span>
<span data-ttu-id="0119a-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0119a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0119a-121">-Id</span><span class="sxs-lookup"><span data-stu-id="0119a-121">-Id</span></span>
<span data-ttu-id="0119a-122">배포의 정식 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0119a-122">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="0119a-123">예: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="0119a-123">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="0119a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0119a-124">-Name</span></span>
<span data-ttu-id="0119a-125">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0119a-125">The name of deployment.</span></span>

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

### <span data-ttu-id="0119a-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="0119a-126">-Pre</span></span>
<span data-ttu-id="0119a-127">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0119a-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0119a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0119a-128">CommonParameters</span></span>
<span data-ttu-id="0119a-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0119a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0119a-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0119a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0119a-131">입력</span><span class="sxs-lookup"><span data-stu-id="0119a-131">INPUTS</span></span>

### <span data-ttu-id="0119a-132">없음</span><span class="sxs-lookup"><span data-stu-id="0119a-132">None</span></span>

## <span data-ttu-id="0119a-133">출력</span><span class="sxs-lookup"><span data-stu-id="0119a-133">OUTPUTS</span></span>

### <span data-ttu-id="0119a-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSD</span><span class="sxs-lookup"><span data-stu-id="0119a-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0119a-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0119a-135">NOTES</span></span>

## <span data-ttu-id="0119a-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0119a-136">RELATED LINKS</span></span>
