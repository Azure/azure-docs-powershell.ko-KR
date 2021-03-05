---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: 813291fd0014665958dbee85be36060801b3e569
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976464"
---
# <span data-ttu-id="6fb4e-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="6fb4e-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="6fb4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fb4e-102">SYNOPSIS</span></span>
<span data-ttu-id="6fb4e-103">배포 스크립트 및 해당 관련 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6fb4e-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="6fb4e-104">구문</span><span class="sxs-lookup"><span data-stu-id="6fb4e-104">SYNTAX</span></span>

### <span data-ttu-id="6fb4e-105">RemoveDeploymentScriptLogByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="6fb4e-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fb4e-106">RemoveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="6fb4e-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fb4e-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="6fb4e-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fb4e-108">설명</span><span class="sxs-lookup"><span data-stu-id="6fb4e-108">DESCRIPTION</span></span>
<span data-ttu-id="6fb4e-109">**Remove-AzDeploymentScript** cmdlet은 배포 스크립트 및 해당 관련 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6fb4e-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="6fb4e-110">예제</span><span class="sxs-lookup"><span data-stu-id="6fb4e-110">EXAMPLES</span></span>

### <span data-ttu-id="6fb4e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6fb4e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="6fb4e-112">리소스 그룹 DS-TestRG에서 MyDeploymentScript 이름으로 배포 스크립트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6fb4e-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="6fb4e-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6fb4e-113">PARAMETERS</span></span>

### <span data-ttu-id="6fb4e-114">-확인</span><span class="sxs-lookup"><span data-stu-id="6fb4e-114">-Confirm</span></span>
<span data-ttu-id="6fb4e-115">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6fb4e-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fb4e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fb4e-116">-DefaultProfile</span></span>
<span data-ttu-id="6fb4e-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6fb4e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fb4e-118">-Id</span><span class="sxs-lookup"><span data-stu-id="6fb4e-118">-Id</span></span>
<span data-ttu-id="6fb4e-119">배포 스크립트의 완전히 자격을 갖춘 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6fb4e-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="6fb4e-120">예제: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resource/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="6fb4e-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="6fb4e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fb4e-121">-InputObject</span></span>
<span data-ttu-id="6fb4e-122">배포 스크립트 PowerShell 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6fb4e-122">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="6fb4e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6fb4e-123">-Name</span></span>
<span data-ttu-id="6fb4e-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6fb4e-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="6fb4e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6fb4e-125">-PassThru</span></span>
<span data-ttu-id="6fb4e-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6fb4e-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6fb4e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fb4e-127">-ResourceGroupName</span></span>
<span data-ttu-id="6fb4e-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6fb4e-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="6fb4e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fb4e-129">-WhatIf</span></span>
<span data-ttu-id="6fb4e-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6fb4e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fb4e-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6fb4e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fb4e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fb4e-132">CommonParameters</span></span>
<span data-ttu-id="6fb4e-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6fb4e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6fb4e-134">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6fb4e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fb4e-135">입력</span><span class="sxs-lookup"><span data-stu-id="6fb4e-135">INPUTS</span></span>

### <span data-ttu-id="6fb4e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="6fb4e-136">System.String</span></span>

### <span data-ttu-id="6fb4e-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="6fb4e-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="6fb4e-138">출력</span><span class="sxs-lookup"><span data-stu-id="6fb4e-138">OUTPUTS</span></span>

### <span data-ttu-id="6fb4e-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="6fb4e-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="6fb4e-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6fb4e-140">NOTES</span></span>

## <span data-ttu-id="6fb4e-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6fb4e-141">RELATED LINKS</span></span>