---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: 15dc9e6a24aa78523a020af541250c5c51b32994
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699300"
---
# <span data-ttu-id="54358-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="54358-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="54358-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54358-102">SYNOPSIS</span></span>
<span data-ttu-id="54358-103">실행 중인 배포 Cancal</span><span class="sxs-lookup"><span data-stu-id="54358-103">Cancal a running deployment</span></span>

## <span data-ttu-id="54358-104">구문과</span><span class="sxs-lookup"><span data-stu-id="54358-104">SYNTAX</span></span>

### <span data-ttu-id="54358-105">StopByDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="54358-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54358-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="54358-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54358-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="54358-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54358-108">설명은</span><span class="sxs-lookup"><span data-stu-id="54358-108">DESCRIPTION</span></span>
<span data-ttu-id="54358-109">**AzDeployment** cmdlet은 시작 되었지만 완료 되지 않은 구독 범위에서 배포를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="54358-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="54358-110">배포를 중지 하려면 배포에는 프로비저닝 등의 완료 되지 않은 상태 (예: 프로 비전 됨 또는 실패)가 아닌 완전 한 프로비저닝 상태가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="54358-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="54358-111">구독 범위에서 배포를 만들려면 New-AzDeployment cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="54358-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="54358-112">이 cmdlet는 실행 중인 하나의 배포만 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="54358-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="54358-113">특정 배포를 중지 하려면 *Name* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="54358-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="54358-114">예제의</span><span class="sxs-lookup"><span data-stu-id="54358-114">EXAMPLES</span></span>

### <span data-ttu-id="54358-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="54358-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="54358-116">이 명령은 현재 구독 범위에서 실행 중인 배포 "deployment01"를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="54358-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="54358-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="54358-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="54358-118">이 명령은 현재 구독 범위에서 배포 "deployment01"를 가져와 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="54358-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="54358-119">변수</span><span class="sxs-lookup"><span data-stu-id="54358-119">PARAMETERS</span></span>

### <span data-ttu-id="54358-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="54358-120">-ApiVersion</span></span>
<span data-ttu-id="54358-121">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="54358-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="54358-122">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="54358-122">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="54358-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54358-123">-DefaultProfile</span></span>
<span data-ttu-id="54358-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="54358-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54358-125">-Id</span><span class="sxs-lookup"><span data-stu-id="54358-125">-Id</span></span>
<span data-ttu-id="54358-126">배포의 정규화 된 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="54358-126">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="54358-127">예:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="54358-127">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="54358-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54358-128">-InputObject</span></span>
<span data-ttu-id="54358-129">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="54358-129">The deployment object.</span></span>

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

### <span data-ttu-id="54358-130">-이름</span><span class="sxs-lookup"><span data-stu-id="54358-130">-Name</span></span>
<span data-ttu-id="54358-131">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54358-131">The name of the deployment.</span></span>

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

### <span data-ttu-id="54358-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54358-132">-PassThru</span></span>
<span data-ttu-id="54358-133">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="54358-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="54358-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="54358-134">-Pre</span></span>
<span data-ttu-id="54358-135">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="54358-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="54358-136">-확인</span><span class="sxs-lookup"><span data-stu-id="54358-136">-Confirm</span></span>
<span data-ttu-id="54358-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="54358-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54358-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54358-138">-WhatIf</span></span>
<span data-ttu-id="54358-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="54358-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54358-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54358-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54358-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54358-141">CommonParameters</span></span>
<span data-ttu-id="54358-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54358-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54358-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54358-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54358-144">입력</span><span class="sxs-lookup"><span data-stu-id="54358-144">INPUTS</span></span>

### <span data-ttu-id="54358-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="54358-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="54358-146">출력</span><span class="sxs-lookup"><span data-stu-id="54358-146">OUTPUTS</span></span>

### <span data-ttu-id="54358-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="54358-147">System.Boolean</span></span>

## <span data-ttu-id="54358-148">상속자</span><span class="sxs-lookup"><span data-stu-id="54358-148">NOTES</span></span>

## <span data-ttu-id="54358-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54358-149">RELATED LINKS</span></span>
