---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 5054fe397c49e437b34755200b7f53c583e6e94f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308924"
---
# <span data-ttu-id="0a914-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0a914-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="0a914-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a914-102">SYNOPSIS</span></span>
<span data-ttu-id="0a914-103">관리 그룹 배포에 대 한 배포 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="0a914-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="0a914-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0a914-104">SYNTAX</span></span>

### <span data-ttu-id="0a914-105">GetByDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="0a914-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a914-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="0a914-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a914-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0a914-107">DESCRIPTION</span></span>
<span data-ttu-id="0a914-108">**AzManagementGroupDeploymentOperation** cmdlet은 특정 배포에 대해 실패 한 정확한 작업에 대 한 자세한 정보를 식별 하 고 제공 하는 데 도움이 되도록 관리 그룹 배포의 일부인 모든 작업을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a914-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="0a914-109">포털의 배포 세부 정보에 제공 되는 정보와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a914-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="0a914-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0a914-110">EXAMPLES</span></span>

### <span data-ttu-id="0a914-111">예제 1: 배포 이름이 지정 된 배포 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="0a914-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="0a914-112">관리 그룹 "myMG"에 이름이 "Deploy01" 인 배포 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0a914-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="0a914-113">예제 2: 배포 가져오기 및 배포 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="0a914-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="0a914-114">이 명령은 관리 그룹 "myMG"의 배포 "Deploy01"를 가져와 배포 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0a914-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="0a914-115">변수</span><span class="sxs-lookup"><span data-stu-id="0a914-115">PARAMETERS</span></span>

### <span data-ttu-id="0a914-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a914-116">-DefaultProfile</span></span>
<span data-ttu-id="0a914-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0a914-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a914-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="0a914-118">-DeploymentName</span></span>
<span data-ttu-id="0a914-119">배포 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a914-119">The deployment name.</span></span>

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

### <span data-ttu-id="0a914-120">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="0a914-120">-DeploymentObject</span></span>
<span data-ttu-id="0a914-121">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0a914-121">The deployment object.</span></span>

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

### <span data-ttu-id="0a914-122">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="0a914-122">-ManagementGroupId</span></span>
<span data-ttu-id="0a914-123">관리 그룹 id입니다.</span><span class="sxs-lookup"><span data-stu-id="0a914-123">The management group id.</span></span>

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

### <span data-ttu-id="0a914-124">-OperationId</span><span class="sxs-lookup"><span data-stu-id="0a914-124">-OperationId</span></span>
<span data-ttu-id="0a914-125">배포 작업 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="0a914-125">The deployment operation Id.</span></span>

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

### <span data-ttu-id="0a914-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="0a914-126">-Pre</span></span>
<span data-ttu-id="0a914-127">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0a914-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0a914-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a914-128">CommonParameters</span></span>
<span data-ttu-id="0a914-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a914-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a914-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0a914-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a914-131">입력</span><span class="sxs-lookup"><span data-stu-id="0a914-131">INPUTS</span></span>

### <span data-ttu-id="0a914-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="0a914-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0a914-133">출력</span><span class="sxs-lookup"><span data-stu-id="0a914-133">OUTPUTS</span></span>

### <span data-ttu-id="0a914-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0a914-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="0a914-135">상속자</span><span class="sxs-lookup"><span data-stu-id="0a914-135">NOTES</span></span>

## <span data-ttu-id="0a914-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a914-136">RELATED LINKS</span></span>
