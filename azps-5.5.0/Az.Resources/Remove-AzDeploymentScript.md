---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: 647fd1f2f36d052d4d116f090fc438aa22dcc862
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186372"
---
# <span data-ttu-id="1c2dd-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="1c2dd-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="1c2dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c2dd-102">SYNOPSIS</span></span>
<span data-ttu-id="1c2dd-103">배포 스크립트 및 관련 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1c2dd-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="1c2dd-104">구문</span><span class="sxs-lookup"><span data-stu-id="1c2dd-104">SYNTAX</span></span>

### <span data-ttu-id="1c2dd-105">RemoveDeploymentScriptLogByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="1c2dd-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c2dd-106">RemoveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="1c2dd-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c2dd-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="1c2dd-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c2dd-108">설명</span><span class="sxs-lookup"><span data-stu-id="1c2dd-108">DESCRIPTION</span></span>
<span data-ttu-id="1c2dd-109">**Remove-AzDeploymentScript** cmdlet은 배포 스크립트 및 관련 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1c2dd-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="1c2dd-110">예제</span><span class="sxs-lookup"><span data-stu-id="1c2dd-110">EXAMPLES</span></span>

### <span data-ttu-id="1c2dd-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1c2dd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="1c2dd-112">리소스 그룹 DS-TestRG에서 MyDeploymentScript 이름이 있는 배포 스크립트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1c2dd-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="1c2dd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c2dd-113">PARAMETERS</span></span>

### <span data-ttu-id="1c2dd-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c2dd-114">-Confirm</span></span>
<span data-ttu-id="1c2dd-115">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c2dd-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c2dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c2dd-116">-DefaultProfile</span></span>
<span data-ttu-id="1c2dd-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c2dd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c2dd-118">-Id</span><span class="sxs-lookup"><span data-stu-id="1c2dd-118">-Id</span></span>
<span data-ttu-id="1c2dd-119">배포 스크립트의 정식 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1c2dd-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="1c2dd-120">예: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="1c2dd-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c2dd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c2dd-121">-InputObject</span></span>
<span data-ttu-id="1c2dd-122">배포 스크립트 PowerShell 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1c2dd-122">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: RemoveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c2dd-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1c2dd-123">-Name</span></span>
<span data-ttu-id="1c2dd-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c2dd-124">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c2dd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c2dd-125">-PassThru</span></span>
<span data-ttu-id="1c2dd-126">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="1c2dd-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1c2dd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c2dd-127">-ResourceGroupName</span></span>
<span data-ttu-id="1c2dd-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c2dd-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c2dd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c2dd-129">-WhatIf</span></span>
<span data-ttu-id="1c2dd-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1c2dd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c2dd-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c2dd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c2dd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c2dd-132">CommonParameters</span></span>
<span data-ttu-id="1c2dd-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1c2dd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1c2dd-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1c2dd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c2dd-135">입력</span><span class="sxs-lookup"><span data-stu-id="1c2dd-135">INPUTS</span></span>

### <span data-ttu-id="1c2dd-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1c2dd-136">System.String</span></span>

### <span data-ttu-id="1c2dd-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="1c2dd-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="1c2dd-138">출력</span><span class="sxs-lookup"><span data-stu-id="1c2dd-138">OUTPUTS</span></span>

### <span data-ttu-id="1c2dd-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="1c2dd-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="1c2dd-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1c2dd-140">NOTES</span></span>

## <span data-ttu-id="1c2dd-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c2dd-141">RELATED LINKS</span></span>