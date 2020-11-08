---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: a15804d0af664c46d443128e940e3b9f2c8a1acc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034262"
---
# <span data-ttu-id="92e39-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="92e39-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="92e39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92e39-102">SYNOPSIS</span></span>
<span data-ttu-id="92e39-103">배포 스크립트 및 해당 관련 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="92e39-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="92e39-104">구문과</span><span class="sxs-lookup"><span data-stu-id="92e39-104">SYNTAX</span></span>

### <span data-ttu-id="92e39-105">RemoveDeploymentScriptLogByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="92e39-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92e39-106">RemoveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="92e39-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92e39-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="92e39-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92e39-108">설명은</span><span class="sxs-lookup"><span data-stu-id="92e39-108">DESCRIPTION</span></span>
<span data-ttu-id="92e39-109">**AzDeploymentScript** cmdlet은 배포 스크립트 및 해당 관련 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="92e39-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="92e39-110">예제의</span><span class="sxs-lookup"><span data-stu-id="92e39-110">EXAMPLES</span></span>

### <span data-ttu-id="92e39-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="92e39-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="92e39-112">리소스 그룹 DS-TestRG에서 이름 MyDeploymentScript를 사용 하 여 배포 스크립트를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="92e39-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="92e39-113">변수</span><span class="sxs-lookup"><span data-stu-id="92e39-113">PARAMETERS</span></span>

### <span data-ttu-id="92e39-114">-확인</span><span class="sxs-lookup"><span data-stu-id="92e39-114">-Confirm</span></span>
<span data-ttu-id="92e39-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="92e39-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92e39-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e39-116">-DefaultProfile</span></span>
<span data-ttu-id="92e39-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92e39-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92e39-118">-Id</span><span class="sxs-lookup"><span data-stu-id="92e39-118">-Id</span></span>
<span data-ttu-id="92e39-119">배포 스크립트의 정규화 된 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="92e39-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="92e39-120">예:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="92e39-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="92e39-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92e39-121">-InputObject</span></span>
<span data-ttu-id="92e39-122">배포 스크립트 PowerShell 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="92e39-122">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="92e39-123">-이름</span><span class="sxs-lookup"><span data-stu-id="92e39-123">-Name</span></span>
<span data-ttu-id="92e39-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92e39-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="92e39-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92e39-125">-PassThru</span></span>
<span data-ttu-id="92e39-126">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="92e39-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="92e39-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92e39-127">-ResourceGroupName</span></span>
<span data-ttu-id="92e39-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92e39-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="92e39-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92e39-129">-WhatIf</span></span>
<span data-ttu-id="92e39-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="92e39-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92e39-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92e39-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92e39-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e39-132">CommonParameters</span></span>
<span data-ttu-id="92e39-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="92e39-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="92e39-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92e39-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e39-135">입력</span><span class="sxs-lookup"><span data-stu-id="92e39-135">INPUTS</span></span>

### <span data-ttu-id="92e39-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="92e39-136">System.String</span></span>

### <span data-ttu-id="92e39-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="92e39-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="92e39-138">출력</span><span class="sxs-lookup"><span data-stu-id="92e39-138">OUTPUTS</span></span>

### <span data-ttu-id="92e39-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="92e39-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="92e39-140">상속자</span><span class="sxs-lookup"><span data-stu-id="92e39-140">NOTES</span></span>

## <span data-ttu-id="92e39-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92e39-141">RELATED LINKS</span></span>
