---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 25f20b56ef7da59851d4726ad573c07d4da259e1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358758"
---
# <span data-ttu-id="ba91f-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="ba91f-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="ba91f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba91f-102">SYNOPSIS</span></span>
<span data-ttu-id="ba91f-103">배포 스크립트 실행 로그를 디스크에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ba91f-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="ba91f-104">구문</span><span class="sxs-lookup"><span data-stu-id="ba91f-104">SYNTAX</span></span>

### <span data-ttu-id="ba91f-105">SaveDeploymentScriptLogByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="ba91f-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba91f-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="ba91f-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba91f-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="ba91f-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba91f-108">설명</span><span class="sxs-lookup"><span data-stu-id="ba91f-108">DESCRIPTION</span></span>
<span data-ttu-id="ba91f-109">**Save-AzDeploymentScriptLog는** 배포 스크립트 실행 로그를 디스크에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ba91f-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="ba91f-110">예제</span><span class="sxs-lookup"><span data-stu-id="ba91f-110">EXAMPLES</span></span>

### <span data-ttu-id="ba91f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ba91f-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="ba91f-112">지정한 이름 및 리소스 그룹으로 배포 스크립트의 로그를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ba91f-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="ba91f-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="ba91f-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="ba91f-114">지정한 이름 및 리소스 그룹으로 배포 스크립트의 로그의 마지막 3줄을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ba91f-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="ba91f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba91f-115">PARAMETERS</span></span>

### <span data-ttu-id="ba91f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba91f-116">-DefaultProfile</span></span>
<span data-ttu-id="ba91f-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba91f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba91f-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="ba91f-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="ba91f-119">배포 스크립트 PowerShell 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ba91f-119">The deployment script PowerShell object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: SaveDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba91f-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="ba91f-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="ba91f-121">배포 스크립트의 정식 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ba91f-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="ba91f-122">예: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="ba91f-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba91f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ba91f-123">-Force</span></span>
<span data-ttu-id="ba91f-124">기존 파일의 덮어를 강제로 덮어 덮어 습니다.</span><span class="sxs-lookup"><span data-stu-id="ba91f-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="ba91f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ba91f-125">-Name</span></span>
<span data-ttu-id="ba91f-126">배포 스크립트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ba91f-126">The name of the deployment script.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba91f-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="ba91f-127">-OutputPath</span></span>
<span data-ttu-id="ba91f-128">배포 스크립트 로그를 저장할 디렉터리 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="ba91f-128">The directory path to save deployment script log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba91f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba91f-129">-ResourceGroupName</span></span>
<span data-ttu-id="ba91f-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ba91f-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba91f-131">-Tail</span><span class="sxs-lookup"><span data-stu-id="ba91f-131">-Tail</span></span>
<span data-ttu-id="ba91f-132">출력을 마지막 n줄로 제한</span><span class="sxs-lookup"><span data-stu-id="ba91f-132">Limit output to last n lines</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba91f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba91f-133">-Confirm</span></span>
<span data-ttu-id="ba91f-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba91f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba91f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba91f-135">-WhatIf</span></span>
<span data-ttu-id="ba91f-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ba91f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba91f-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba91f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba91f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba91f-138">CommonParameters</span></span>
<span data-ttu-id="ba91f-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ba91f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba91f-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ba91f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba91f-141">입력</span><span class="sxs-lookup"><span data-stu-id="ba91f-141">INPUTS</span></span>

### <span data-ttu-id="ba91f-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ba91f-142">System.String</span></span>

## <span data-ttu-id="ba91f-143">출력</span><span class="sxs-lookup"><span data-stu-id="ba91f-143">OUTPUTS</span></span>

### <span data-ttu-id="ba91f-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="ba91f-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="ba91f-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ba91f-145">NOTES</span></span>

## <span data-ttu-id="ba91f-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba91f-146">RELATED LINKS</span></span>
