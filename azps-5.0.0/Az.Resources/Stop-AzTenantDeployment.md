---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: bda1d2e79e7ef67e69d7b425761750a95c2f3777
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217026"
---
# <span data-ttu-id="5d8b1-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="5d8b1-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="5d8b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d8b1-102">SYNOPSIS</span></span>
<span data-ttu-id="5d8b1-103">테 넌 트 범위에서 실행 중인 배포 취소</span><span class="sxs-lookup"><span data-stu-id="5d8b1-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="5d8b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5d8b1-104">SYNTAX</span></span>

### <span data-ttu-id="5d8b1-105">StopByDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="5d8b1-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d8b1-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="5d8b1-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d8b1-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="5d8b1-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d8b1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5d8b1-108">DESCRIPTION</span></span>
<span data-ttu-id="5d8b1-109">**AzTenantDeployment** cmdlet은 시작 되었지만 현재 테 넌 트 범위에서 완료 되지 않은 배포를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="5d8b1-110">배포를 중지 하려면 배포에는 프로비저닝 등의 완료 되지 않은 상태 (예: 프로 비전 됨 또는 실패)가 아닌 완전 한 프로비저닝 상태가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="5d8b1-111">테 넌 트 범위에서 배포를 만들려면 New-AzTenantDeployment cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="5d8b1-112">예제의</span><span class="sxs-lookup"><span data-stu-id="5d8b1-112">EXAMPLES</span></span>

### <span data-ttu-id="5d8b1-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="5d8b1-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="5d8b1-114">이 명령은 현재 테 넌 트 범위에서 실행 중인 배포 "deployment01"를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="5d8b1-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="5d8b1-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="5d8b1-116">이 명령은 현재 테 넌 트 범위에서 배포 "deployment01"를 가져와 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="5d8b1-117">변수</span><span class="sxs-lookup"><span data-stu-id="5d8b1-117">PARAMETERS</span></span>

### <span data-ttu-id="5d8b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d8b1-118">-DefaultProfile</span></span>
<span data-ttu-id="5d8b1-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d8b1-120">-Id</span><span class="sxs-lookup"><span data-stu-id="5d8b1-120">-Id</span></span>
<span data-ttu-id="5d8b1-121">배포의 정규화 된 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="5d8b1-122">예:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="5d8b1-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8b1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d8b1-123">-InputObject</span></span>
<span data-ttu-id="5d8b1-124">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d8b1-125">-이름</span><span class="sxs-lookup"><span data-stu-id="5d8b1-125">-Name</span></span>
<span data-ttu-id="5d8b1-126">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d8b1-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d8b1-127">-PassThru</span></span>
<span data-ttu-id="5d8b1-128">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="5d8b1-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="5d8b1-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="5d8b1-129">-Pre</span></span>
<span data-ttu-id="5d8b1-130">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5d8b1-131">-확인</span><span class="sxs-lookup"><span data-stu-id="5d8b1-131">-Confirm</span></span>
<span data-ttu-id="5d8b1-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d8b1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d8b1-133">-WhatIf</span></span>
<span data-ttu-id="5d8b1-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d8b1-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d8b1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d8b1-136">CommonParameters</span></span>
<span data-ttu-id="5d8b1-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d8b1-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d8b1-139">입력</span><span class="sxs-lookup"><span data-stu-id="5d8b1-139">INPUTS</span></span>

### <span data-ttu-id="5d8b1-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="5d8b1-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="5d8b1-141">출력</span><span class="sxs-lookup"><span data-stu-id="5d8b1-141">OUTPUTS</span></span>

### <span data-ttu-id="5d8b1-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="5d8b1-142">System.Boolean</span></span>

## <span data-ttu-id="5d8b1-143">상속자</span><span class="sxs-lookup"><span data-stu-id="5d8b1-143">NOTES</span></span>

## <span data-ttu-id="5d8b1-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d8b1-144">RELATED LINKS</span></span>
