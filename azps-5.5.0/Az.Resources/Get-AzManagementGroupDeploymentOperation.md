---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 5054fe397c49e437b34755200b7f53c583e6e94f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197996"
---
# <span data-ttu-id="aa22f-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="aa22f-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="aa22f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa22f-102">SYNOPSIS</span></span>
<span data-ttu-id="aa22f-103">관리 그룹 배포에 대한 배포 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="aa22f-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="aa22f-104">구문</span><span class="sxs-lookup"><span data-stu-id="aa22f-104">SYNTAX</span></span>

### <span data-ttu-id="aa22f-105">GetByDeploymentName(기본값)</span><span class="sxs-lookup"><span data-stu-id="aa22f-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa22f-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="aa22f-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa22f-107">설명</span><span class="sxs-lookup"><span data-stu-id="aa22f-107">DESCRIPTION</span></span>
<span data-ttu-id="aa22f-108">**Get-AzManagementGroupDeploymentOperation** cmdlet은 관리 그룹 배포의 일부인 모든 작업을 나열하여 특정 배포에 실패한 정확한 작업에 대한 자세한 정보를 식별하고 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="aa22f-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="aa22f-109">이는 포털의 배포 세부 정보에 제공된 동일한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="aa22f-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="aa22f-110">예제</span><span class="sxs-lookup"><span data-stu-id="aa22f-110">EXAMPLES</span></span>

### <span data-ttu-id="aa22f-111">예제 1: 배포 이름을 지정한 배포 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="aa22f-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="aa22f-112">관리 그룹 "myMG"에서 이름이 "Deploy01"인 배포 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aa22f-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="aa22f-113">예제 2: 배포를 시작하고 배포 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aa22f-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="aa22f-114">이 명령은 관리 그룹 "myMG"에서 배포 "Deploy01"을 사용하여 배포 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aa22f-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="aa22f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa22f-115">PARAMETERS</span></span>

### <span data-ttu-id="aa22f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa22f-116">-DefaultProfile</span></span>
<span data-ttu-id="aa22f-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa22f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa22f-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="aa22f-118">-DeploymentName</span></span>
<span data-ttu-id="aa22f-119">배포 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa22f-119">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa22f-120">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="aa22f-120">-DeploymentObject</span></span>
<span data-ttu-id="aa22f-121">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="aa22f-121">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa22f-122">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="aa22f-122">-ManagementGroupId</span></span>
<span data-ttu-id="aa22f-123">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="aa22f-123">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa22f-124">-OperationId</span><span class="sxs-lookup"><span data-stu-id="aa22f-124">-OperationId</span></span>
<span data-ttu-id="aa22f-125">배포 작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="aa22f-125">The deployment operation Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa22f-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="aa22f-126">-Pre</span></span>
<span data-ttu-id="aa22f-127">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="aa22f-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="aa22f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa22f-128">CommonParameters</span></span>
<span data-ttu-id="aa22f-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aa22f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa22f-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aa22f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa22f-131">입력</span><span class="sxs-lookup"><span data-stu-id="aa22f-131">INPUTS</span></span>

### <span data-ttu-id="aa22f-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSD</span><span class="sxs-lookup"><span data-stu-id="aa22f-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="aa22f-133">출력</span><span class="sxs-lookup"><span data-stu-id="aa22f-133">OUTPUTS</span></span>

### <span data-ttu-id="aa22f-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="aa22f-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="aa22f-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aa22f-135">NOTES</span></span>

## <span data-ttu-id="aa22f-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa22f-136">RELATED LINKS</span></span>
