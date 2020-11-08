---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 4820a1aec02355a535ec7798eb7f8e3dba6458b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214230"
---
# <span data-ttu-id="bea95-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="bea95-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="bea95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bea95-102">SYNOPSIS</span></span>
<span data-ttu-id="bea95-103">관리 그룹 배포에 대 한 배포 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="bea95-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="bea95-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bea95-104">SYNTAX</span></span>

### <span data-ttu-id="bea95-105">GetByDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="bea95-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bea95-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="bea95-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bea95-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bea95-107">DESCRIPTION</span></span>
<span data-ttu-id="bea95-108">**AzManagementGroupDeploymentOperation** cmdlet은 특정 배포에 대해 실패 한 정확한 작업에 대 한 자세한 정보를 식별 하 고 제공 하는 데 도움이 되도록 관리 그룹 배포의 일부인 모든 작업을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="bea95-109">포털의 배포 세부 정보에 제공 되는 정보와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="bea95-110">예제의</span><span class="sxs-lookup"><span data-stu-id="bea95-110">EXAMPLES</span></span>

### <span data-ttu-id="bea95-111">예제 1: 배포 이름이 지정 된 배포 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="bea95-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="bea95-112">관리 그룹 "myMG"에 이름이 "Deploy01" 인 배포 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="bea95-113">예제 2: 배포 가져오기 및 배포 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="bea95-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="bea95-114">이 명령은 관리 그룹 "myMG"의 배포 "Deploy01"를 가져와 배포 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="bea95-115">변수</span><span class="sxs-lookup"><span data-stu-id="bea95-115">PARAMETERS</span></span>

### <span data-ttu-id="bea95-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bea95-116">-ApiVersion</span></span>
<span data-ttu-id="bea95-117">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="bea95-118">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="bea95-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea95-119">-DefaultProfile</span></span>
<span data-ttu-id="bea95-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bea95-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="bea95-121">-DeploymentName</span></span>
<span data-ttu-id="bea95-122">배포 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-122">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea95-123">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="bea95-123">-DeploymentObject</span></span>
<span data-ttu-id="bea95-124">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-124">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bea95-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="bea95-125">-ManagementGroupId</span></span>
<span data-ttu-id="bea95-126">관리 그룹 id입니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-126">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea95-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="bea95-127">-OperationId</span></span>
<span data-ttu-id="bea95-128">배포 작업 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-128">The deployment operation Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea95-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="bea95-129">-Pre</span></span>
<span data-ttu-id="bea95-130">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="bea95-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea95-131">CommonParameters</span></span>
<span data-ttu-id="bea95-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea95-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bea95-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea95-134">입력</span><span class="sxs-lookup"><span data-stu-id="bea95-134">INPUTS</span></span>

### <span data-ttu-id="bea95-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="bea95-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="bea95-136">출력</span><span class="sxs-lookup"><span data-stu-id="bea95-136">OUTPUTS</span></span>

### <span data-ttu-id="bea95-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="bea95-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="bea95-138">상속자</span><span class="sxs-lookup"><span data-stu-id="bea95-138">NOTES</span></span>

## <span data-ttu-id="bea95-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bea95-139">RELATED LINKS</span></span>
