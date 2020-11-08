---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 25f20b56ef7da59851d4726ad573c07d4da259e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204396"
---
# <span data-ttu-id="c3e80-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="c3e80-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="c3e80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3e80-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e80-103">배포 스크립트 실행의 로그를 디스크에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e80-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="c3e80-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c3e80-104">SYNTAX</span></span>

### <span data-ttu-id="c3e80-105">SaveDeploymentScriptLogByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c3e80-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3e80-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="c3e80-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3e80-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="c3e80-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3e80-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c3e80-108">DESCRIPTION</span></span>
<span data-ttu-id="c3e80-109">**저장-AzDeploymentScriptLog** 는 배포 스크립트 실행의 로그를 디스크에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e80-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="c3e80-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c3e80-110">EXAMPLES</span></span>

### <span data-ttu-id="c3e80-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c3e80-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="c3e80-112">배포 스크립트의 로그를 지정 된 이름 및 리소스 그룹으로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e80-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="c3e80-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="c3e80-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="c3e80-114">배포 스크립트 로그의 마지막 세 줄을 지정 된 이름 및 리소스 그룹으로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e80-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="c3e80-115">변수</span><span class="sxs-lookup"><span data-stu-id="c3e80-115">PARAMETERS</span></span>

### <span data-ttu-id="c3e80-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e80-116">-DefaultProfile</span></span>
<span data-ttu-id="c3e80-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c3e80-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3e80-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="c3e80-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="c3e80-119">배포 스크립트 PowerShell 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c3e80-119">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="c3e80-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="c3e80-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="c3e80-121">배포 스크립트의 정규화 된 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="c3e80-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="c3e80-122">예:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="c3e80-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="c3e80-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c3e80-123">-Force</span></span>
<span data-ttu-id="c3e80-124">기존 파일을 강제로 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="c3e80-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="c3e80-125">-이름</span><span class="sxs-lookup"><span data-stu-id="c3e80-125">-Name</span></span>
<span data-ttu-id="c3e80-126">배포 스크립트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3e80-126">The name of the deployment script.</span></span>

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

### <span data-ttu-id="c3e80-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="c3e80-127">-OutputPath</span></span>
<span data-ttu-id="c3e80-128">배포 스크립트 로그를 저장할 디렉터리 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c3e80-128">The directory path to save deployment script log.</span></span>

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

### <span data-ttu-id="c3e80-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3e80-129">-ResourceGroupName</span></span>
<span data-ttu-id="c3e80-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3e80-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="c3e80-131">-꼬리</span><span class="sxs-lookup"><span data-stu-id="c3e80-131">-Tail</span></span>
<span data-ttu-id="c3e80-132">출력을 지난 n 줄로 제한</span><span class="sxs-lookup"><span data-stu-id="c3e80-132">Limit output to last n lines</span></span>

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

### <span data-ttu-id="c3e80-133">-확인</span><span class="sxs-lookup"><span data-stu-id="c3e80-133">-Confirm</span></span>
<span data-ttu-id="c3e80-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e80-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3e80-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3e80-135">-WhatIf</span></span>
<span data-ttu-id="c3e80-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c3e80-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3e80-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c3e80-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3e80-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e80-138">CommonParameters</span></span>
<span data-ttu-id="c3e80-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e80-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e80-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c3e80-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e80-141">입력</span><span class="sxs-lookup"><span data-stu-id="c3e80-141">INPUTS</span></span>

### <span data-ttu-id="c3e80-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c3e80-142">System.String</span></span>

## <span data-ttu-id="c3e80-143">출력</span><span class="sxs-lookup"><span data-stu-id="c3e80-143">OUTPUTS</span></span>

### <span data-ttu-id="c3e80-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="c3e80-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="c3e80-145">상속자</span><span class="sxs-lookup"><span data-stu-id="c3e80-145">NOTES</span></span>

## <span data-ttu-id="c3e80-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3e80-146">RELATED LINKS</span></span>
