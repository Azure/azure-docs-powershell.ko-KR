---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: f9348090c3dd397573d6ef9d36fcad2aee3b55aa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041769"
---
# <span data-ttu-id="6b27f-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6b27f-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="6b27f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b27f-102">SYNOPSIS</span></span>
<span data-ttu-id="6b27f-103">관리 그룹 및 연결 된 작업에서 배포를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b27f-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="6b27f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6b27f-104">SYNTAX</span></span>

### <span data-ttu-id="6b27f-105">RemoveByDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="6b27f-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b27f-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="6b27f-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b27f-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="6b27f-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b27f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6b27f-108">DESCRIPTION</span></span>
<span data-ttu-id="6b27f-109">**AzManagementGroupDeployment** cmdlet은 관리 그룹 및 연결 된 작업에서 Azure 배포를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b27f-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="6b27f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6b27f-110">EXAMPLES</span></span>

### <span data-ttu-id="6b27f-111">예제 1: 지정 된 이름을 사용 하 여 배포 제거</span><span class="sxs-lookup"><span data-stu-id="6b27f-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="6b27f-112">이 명령은 관리 그룹 "myMG"에서 배포 "역할 배포"를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b27f-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="6b27f-113">예제 2: 배포 가져오기 및 제거</span><span class="sxs-lookup"><span data-stu-id="6b27f-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="6b27f-114">이 명령은 관리 그룹 "myMG"의 배포 "역할 배포"를 가져와 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b27f-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="6b27f-115">변수</span><span class="sxs-lookup"><span data-stu-id="6b27f-115">PARAMETERS</span></span>

### <span data-ttu-id="6b27f-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6b27f-116">-ApiVersion</span></span>
<span data-ttu-id="6b27f-117">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b27f-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="6b27f-118">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b27f-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="6b27f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b27f-119">-AsJob</span></span>
<span data-ttu-id="6b27f-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6b27f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b27f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b27f-121">-DefaultProfile</span></span>
<span data-ttu-id="6b27f-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b27f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b27f-123">-Id</span><span class="sxs-lookup"><span data-stu-id="6b27f-123">-Id</span></span>
<span data-ttu-id="6b27f-124">배포의 정규화 된 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="6b27f-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="6b27f-125">예:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="6b27f-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b27f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b27f-126">-InputObject</span></span>
<span data-ttu-id="6b27f-127">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6b27f-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b27f-128">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="6b27f-128">-ManagementGroupId</span></span>
<span data-ttu-id="6b27f-129">관리 그룹 id입니다.</span><span class="sxs-lookup"><span data-stu-id="6b27f-129">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b27f-130">-이름</span><span class="sxs-lookup"><span data-stu-id="6b27f-130">-Name</span></span>
<span data-ttu-id="6b27f-131">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b27f-131">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b27f-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b27f-132">-PassThru</span></span>
<span data-ttu-id="6b27f-133">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="6b27f-133">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="6b27f-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="6b27f-134">-Pre</span></span>
<span data-ttu-id="6b27f-135">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6b27f-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6b27f-136">-확인</span><span class="sxs-lookup"><span data-stu-id="6b27f-136">-Confirm</span></span>
<span data-ttu-id="6b27f-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b27f-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b27f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b27f-138">-WhatIf</span></span>
<span data-ttu-id="6b27f-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6b27f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b27f-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b27f-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b27f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b27f-141">CommonParameters</span></span>
<span data-ttu-id="6b27f-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b27f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b27f-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6b27f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b27f-144">입력</span><span class="sxs-lookup"><span data-stu-id="6b27f-144">INPUTS</span></span>

### <span data-ttu-id="6b27f-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="6b27f-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="6b27f-146">출력</span><span class="sxs-lookup"><span data-stu-id="6b27f-146">OUTPUTS</span></span>

### <span data-ttu-id="6b27f-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6b27f-147">System.Boolean</span></span>

## <span data-ttu-id="6b27f-148">상속자</span><span class="sxs-lookup"><span data-stu-id="6b27f-148">NOTES</span></span>

## <span data-ttu-id="6b27f-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b27f-149">RELATED LINKS</span></span>
