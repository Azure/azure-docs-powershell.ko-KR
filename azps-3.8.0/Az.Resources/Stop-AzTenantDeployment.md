---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: 6c79d4b8d853d629a3b8e0422efb6a86eee18e34
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041709"
---
# <span data-ttu-id="f0d5d-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="f0d5d-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="f0d5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0d5d-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d5d-103">테 넌 트 범위에서 실행 중인 배포 취소</span><span class="sxs-lookup"><span data-stu-id="f0d5d-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="f0d5d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f0d5d-104">SYNTAX</span></span>

### <span data-ttu-id="f0d5d-105">StopByDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="f0d5d-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0d5d-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="f0d5d-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0d5d-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="f0d5d-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0d5d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f0d5d-108">DESCRIPTION</span></span>
<span data-ttu-id="f0d5d-109">**AzTenantDeployment** cmdlet은 시작 되었지만 현재 테 넌 트 범위에서 완료 되지 않은 배포를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0d5d-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="f0d5d-110">배포를 중지 하려면 배포에는 프로비저닝 등의 완료 되지 않은 상태 (예: 프로 비전 됨 또는 실패)가 아닌 완전 한 프로비저닝 상태가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0d5d-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="f0d5d-111">테 넌 트 범위에서 배포를 만들려면 New-AzTenantDeployment cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0d5d-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="f0d5d-112">예제의</span><span class="sxs-lookup"><span data-stu-id="f0d5d-112">EXAMPLES</span></span>

### <span data-ttu-id="f0d5d-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="f0d5d-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="f0d5d-114">이 명령은 현재 테 넌 트 범위에서 실행 중인 배포 "deployment01"를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0d5d-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="f0d5d-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="f0d5d-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="f0d5d-116">이 명령은 현재 테 넌 트 범위에서 배포 "deployment01"를 가져와 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0d5d-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="f0d5d-117">변수</span><span class="sxs-lookup"><span data-stu-id="f0d5d-117">PARAMETERS</span></span>

### <span data-ttu-id="f0d5d-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f0d5d-118">-ApiVersion</span></span>
<span data-ttu-id="f0d5d-119">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f0d5d-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f0d5d-120">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0d5d-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f0d5d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d5d-121">-DefaultProfile</span></span>
<span data-ttu-id="f0d5d-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f0d5d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0d5d-123">-Id</span><span class="sxs-lookup"><span data-stu-id="f0d5d-123">-Id</span></span>
<span data-ttu-id="f0d5d-124">배포의 정규화 된 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="f0d5d-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="f0d5d-125">예:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="f0d5d-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d5d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0d5d-126">-InputObject</span></span>
<span data-ttu-id="f0d5d-127">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f0d5d-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0d5d-128">-이름</span><span class="sxs-lookup"><span data-stu-id="f0d5d-128">-Name</span></span>
<span data-ttu-id="f0d5d-129">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0d5d-129">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d5d-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0d5d-130">-PassThru</span></span>
<span data-ttu-id="f0d5d-131">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="f0d5d-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="f0d5d-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="f0d5d-132">-Pre</span></span>
<span data-ttu-id="f0d5d-133">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f0d5d-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f0d5d-134">-확인</span><span class="sxs-lookup"><span data-stu-id="f0d5d-134">-Confirm</span></span>
<span data-ttu-id="f0d5d-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0d5d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0d5d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0d5d-136">-WhatIf</span></span>
<span data-ttu-id="f0d5d-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f0d5d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0d5d-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0d5d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0d5d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d5d-139">CommonParameters</span></span>
<span data-ttu-id="f0d5d-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0d5d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d5d-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f0d5d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d5d-142">입력</span><span class="sxs-lookup"><span data-stu-id="f0d5d-142">INPUTS</span></span>

### <span data-ttu-id="f0d5d-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="f0d5d-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="f0d5d-144">출력</span><span class="sxs-lookup"><span data-stu-id="f0d5d-144">OUTPUTS</span></span>

### <span data-ttu-id="f0d5d-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f0d5d-145">System.Boolean</span></span>

## <span data-ttu-id="f0d5d-146">상속자</span><span class="sxs-lookup"><span data-stu-id="f0d5d-146">NOTES</span></span>

## <span data-ttu-id="f0d5d-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0d5d-147">RELATED LINKS</span></span>
