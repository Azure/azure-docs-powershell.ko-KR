---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
ms.openlocfilehash: dbc5238819c6dc7a7555dd1f95ec0ba3478f2b2b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699351"
---
# <span data-ttu-id="c2dfb-101">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="c2dfb-101">Remove-AzDeployment</span></span>

## <span data-ttu-id="c2dfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="c2dfb-103">배포 및 연결 된 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-103">Removes a deployment and any associated operations</span></span>

## <span data-ttu-id="c2dfb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c2dfb-104">SYNTAX</span></span>

### <span data-ttu-id="c2dfb-105">RemoveByDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c2dfb-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzDeployment [-Name] <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2dfb-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="c2dfb-106">RemoveByDeploymentId</span></span>
```
Remove-AzDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2dfb-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="c2dfb-107">RemoveByInputObject</span></span>
```
Remove-AzDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2dfb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c2dfb-108">DESCRIPTION</span></span>
<span data-ttu-id="c2dfb-109">**AzDeployment** cmdlet은 구독 범위 및 연결 된 작업에서 Azure 배포를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-109">The **Remove-AzDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="c2dfb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c2dfb-110">EXAMPLES</span></span>

### <span data-ttu-id="c2dfb-111">예제 1: 지정 된 이름을 사용 하 여 배포 제거</span><span class="sxs-lookup"><span data-stu-id="c2dfb-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzDeployment -Name "RolesDeployment"
```

<span data-ttu-id="c2dfb-112">이 명령은 현재 구독 범위에서 배포 "역할 배포"를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="c2dfb-113">예제 2: 배포 가져오기 및 제거</span><span class="sxs-lookup"><span data-stu-id="c2dfb-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Remove-AzDeployment
```

<span data-ttu-id="c2dfb-114">이 명령은 현재 구독 범위에서 배포 "역할 배포"를 가져와 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="c2dfb-115">변수</span><span class="sxs-lookup"><span data-stu-id="c2dfb-115">PARAMETERS</span></span>

### <span data-ttu-id="c2dfb-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c2dfb-116">-ApiVersion</span></span>
<span data-ttu-id="c2dfb-117">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c2dfb-118">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2dfb-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2dfb-119">-AsJob</span></span>
<span data-ttu-id="c2dfb-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c2dfb-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2dfb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2dfb-121">-DefaultProfile</span></span>
<span data-ttu-id="c2dfb-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2dfb-123">-Id</span><span class="sxs-lookup"><span data-stu-id="c2dfb-123">-Id</span></span>
<span data-ttu-id="c2dfb-124">배포의 정규화 된 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="c2dfb-125">예:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="c2dfb-125">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2dfb-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2dfb-126">-InputObject</span></span>
<span data-ttu-id="c2dfb-127">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-127">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2dfb-128">-이름</span><span class="sxs-lookup"><span data-stu-id="c2dfb-128">-Name</span></span>
<span data-ttu-id="c2dfb-129">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-129">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2dfb-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2dfb-130">-PassThru</span></span>
<span data-ttu-id="c2dfb-131">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="c2dfb-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c2dfb-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="c2dfb-132">-Pre</span></span>
<span data-ttu-id="c2dfb-133">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c2dfb-134">-확인</span><span class="sxs-lookup"><span data-stu-id="c2dfb-134">-Confirm</span></span>
<span data-ttu-id="c2dfb-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2dfb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2dfb-136">-WhatIf</span></span>
<span data-ttu-id="c2dfb-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2dfb-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2dfb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2dfb-139">CommonParameters</span></span>
<span data-ttu-id="c2dfb-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2dfb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2dfb-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2dfb-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2dfb-142">입력</span><span class="sxs-lookup"><span data-stu-id="c2dfb-142">INPUTS</span></span>

### <span data-ttu-id="c2dfb-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c2dfb-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c2dfb-144">출력</span><span class="sxs-lookup"><span data-stu-id="c2dfb-144">OUTPUTS</span></span>

### <span data-ttu-id="c2dfb-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c2dfb-145">System.Boolean</span></span>

## <span data-ttu-id="c2dfb-146">상속자</span><span class="sxs-lookup"><span data-stu-id="c2dfb-146">NOTES</span></span>

## <span data-ttu-id="c2dfb-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2dfb-147">RELATED LINKS</span></span>
