---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 876414b754a259d253dc56e5d92c570aa8f48318
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995204"
---
# <span data-ttu-id="21bc7-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="21bc7-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="21bc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21bc7-102">SYNOPSIS</span></span>
<span data-ttu-id="21bc7-103">배포 스크립트 실행 로그를 디스크에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="21bc7-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="21bc7-104">구문</span><span class="sxs-lookup"><span data-stu-id="21bc7-104">SYNTAX</span></span>

### <span data-ttu-id="21bc7-105">SaveDeploymentScriptLogByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="21bc7-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21bc7-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="21bc7-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21bc7-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="21bc7-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21bc7-108">설명</span><span class="sxs-lookup"><span data-stu-id="21bc7-108">DESCRIPTION</span></span>
<span data-ttu-id="21bc7-109">**Save-AzDeploymentScriptLog는** 배포 스크립트 실행 로그를 디스크에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="21bc7-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="21bc7-110">예제</span><span class="sxs-lookup"><span data-stu-id="21bc7-110">EXAMPLES</span></span>

### <span data-ttu-id="21bc7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="21bc7-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="21bc7-112">지정한 이름 및 리소스 그룹으로 배포 스크립트의 로그를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="21bc7-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="21bc7-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="21bc7-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="21bc7-114">지정한 이름 및 리소스 그룹으로 배포 스크립트의 마지막 3줄을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="21bc7-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="21bc7-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="21bc7-115">PARAMETERS</span></span>

### <span data-ttu-id="21bc7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21bc7-116">-DefaultProfile</span></span>
<span data-ttu-id="21bc7-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="21bc7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21bc7-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="21bc7-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="21bc7-119">배포 스크립트 PowerShell 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="21bc7-119">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="21bc7-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="21bc7-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="21bc7-121">배포 스크립트의 완전히 자격을 갖춘 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="21bc7-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="21bc7-122">예제: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resource/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="21bc7-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="21bc7-123">-Force</span><span class="sxs-lookup"><span data-stu-id="21bc7-123">-Force</span></span>
<span data-ttu-id="21bc7-124">기존 파일의 강제 덮어 니다.</span><span class="sxs-lookup"><span data-stu-id="21bc7-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="21bc7-125">-Name</span><span class="sxs-lookup"><span data-stu-id="21bc7-125">-Name</span></span>
<span data-ttu-id="21bc7-126">배포 스크립트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21bc7-126">The name of the deployment script.</span></span>

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

### <span data-ttu-id="21bc7-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="21bc7-127">-OutputPath</span></span>
<span data-ttu-id="21bc7-128">배포 스크립트 로그를 저장하는 디렉터리 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="21bc7-128">The directory path to save deployment script log.</span></span>

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

### <span data-ttu-id="21bc7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21bc7-129">-ResourceGroupName</span></span>
<span data-ttu-id="21bc7-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21bc7-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="21bc7-131">-Tail</span><span class="sxs-lookup"><span data-stu-id="21bc7-131">-Tail</span></span>
<span data-ttu-id="21bc7-132">출력을 마지막 n줄로 제한</span><span class="sxs-lookup"><span data-stu-id="21bc7-132">Limit output to last n lines</span></span>

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

### <span data-ttu-id="21bc7-133">-확인</span><span class="sxs-lookup"><span data-stu-id="21bc7-133">-Confirm</span></span>
<span data-ttu-id="21bc7-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="21bc7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21bc7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21bc7-135">-WhatIf</span></span>
<span data-ttu-id="21bc7-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="21bc7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21bc7-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21bc7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21bc7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21bc7-138">CommonParameters</span></span>
<span data-ttu-id="21bc7-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="21bc7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21bc7-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21bc7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21bc7-141">입력</span><span class="sxs-lookup"><span data-stu-id="21bc7-141">INPUTS</span></span>

### <span data-ttu-id="21bc7-142">System.String</span><span class="sxs-lookup"><span data-stu-id="21bc7-142">System.String</span></span>

## <span data-ttu-id="21bc7-143">출력</span><span class="sxs-lookup"><span data-stu-id="21bc7-143">OUTPUTS</span></span>

### <span data-ttu-id="21bc7-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="21bc7-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="21bc7-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="21bc7-145">NOTES</span></span>

## <span data-ttu-id="21bc7-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21bc7-146">RELATED LINKS</span></span>
