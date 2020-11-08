---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 1a86eb136fe976ba5e229ff36bd5d0e2a2cad340
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880885"
---
# <span data-ttu-id="987ed-101">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="987ed-101">Get-AzureRmDeployment</span></span>

## <span data-ttu-id="987ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="987ed-102">SYNOPSIS</span></span>
<span data-ttu-id="987ed-103">배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="987ed-103">Get deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="987ed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="987ed-104">SYNTAX</span></span>

### <span data-ttu-id="987ed-105">GetByDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="987ed-105">GetByDeploymentName (Default)</span></span>
```
Get-AzureRmDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="987ed-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="987ed-106">GetByDeploymentId</span></span>
```
Get-AzureRmDeployment [-Id <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="987ed-107">설명은</span><span class="sxs-lookup"><span data-stu-id="987ed-107">DESCRIPTION</span></span>
<span data-ttu-id="987ed-108">**Get-AzureRmDeployment** cmdlet은 현재 구독 범위에서 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="987ed-108">The **Get-AzureRmDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="987ed-109">*이름* 또는 *Id* 매개 변수를 지정 하 여 결과를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="987ed-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="987ed-110">기본적으로 **Get-AzureRmDeployment** 는 현재 구독 범위에서 모든 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="987ed-110">By default, **Get-AzureRmDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="987ed-111">예제의</span><span class="sxs-lookup"><span data-stu-id="987ed-111">EXAMPLES</span></span>

### <span data-ttu-id="987ed-112">예제 1: 구독 범위에서 모든 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="987ed-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzureRmDeployment
```

<span data-ttu-id="987ed-113">이 명령은 현재 구독 범위에서 모든 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="987ed-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="987ed-114">예제 2: 이름으로 배포 가져오기</span><span class="sxs-lookup"><span data-stu-id="987ed-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "DeployRoles01"
```

<span data-ttu-id="987ed-115">이 명령은 현재 구독 범위에서 DeployRoles01 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="987ed-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="987ed-116">**새 AzureRmDeployment** cmdlet을 사용 하 여 배포를 만들 때 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="987ed-116">You can assign a name to a deployment when you create it by using the **New-AzureRmDeployment** cmdlets.</span></span>
<span data-ttu-id="987ed-117">이름을 할당 하지 않으면 cmdlet은 배포를 만드는 데 사용 되는 템플릿을 기반으로 하는 기본 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="987ed-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="987ed-118">변수</span><span class="sxs-lookup"><span data-stu-id="987ed-118">PARAMETERS</span></span>

### <span data-ttu-id="987ed-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="987ed-119">-ApiVersion</span></span>
<span data-ttu-id="987ed-120">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="987ed-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="987ed-121">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="987ed-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="987ed-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="987ed-122">-DefaultProfile</span></span>
<span data-ttu-id="987ed-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="987ed-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="987ed-124">-Id</span><span class="sxs-lookup"><span data-stu-id="987ed-124">-Id</span></span>
<span data-ttu-id="987ed-125">배포의 정규화 된 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="987ed-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="987ed-126">예:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="987ed-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="987ed-127">-이름</span><span class="sxs-lookup"><span data-stu-id="987ed-127">-Name</span></span>
<span data-ttu-id="987ed-128">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="987ed-128">The name of deployment.</span></span>

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

### <span data-ttu-id="987ed-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="987ed-129">-Pre</span></span>
<span data-ttu-id="987ed-130">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="987ed-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="987ed-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="987ed-131">CommonParameters</span></span>
<span data-ttu-id="987ed-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="987ed-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="987ed-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="987ed-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="987ed-134">입력</span><span class="sxs-lookup"><span data-stu-id="987ed-134">INPUTS</span></span>

### <span data-ttu-id="987ed-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="987ed-135">System.String</span></span>

## <span data-ttu-id="987ed-136">출력</span><span class="sxs-lookup"><span data-stu-id="987ed-136">OUTPUTS</span></span>

### <span data-ttu-id="987ed-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="987ed-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="987ed-138">상속자</span><span class="sxs-lookup"><span data-stu-id="987ed-138">NOTES</span></span>

## <span data-ttu-id="987ed-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="987ed-139">RELATED LINKS</span></span>