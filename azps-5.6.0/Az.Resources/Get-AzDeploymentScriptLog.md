---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: dc62e4766a83e1a2046b15fbdf6619e08c4b8e28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956635"
---
# <span data-ttu-id="4d4e8-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="4d4e8-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="4d4e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d4e8-102">SYNOPSIS</span></span>
<span data-ttu-id="4d4e8-103">배포 스크립트 실행의 로그를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4d4e8-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="4d4e8-104">구문</span><span class="sxs-lookup"><span data-stu-id="4d4e8-104">SYNTAX</span></span>

### <span data-ttu-id="4d4e8-105">GetDeploymentScriptLogByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="4d4e8-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d4e8-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="4d4e8-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d4e8-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="4d4e8-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d4e8-108">설명</span><span class="sxs-lookup"><span data-stu-id="4d4e8-108">DESCRIPTION</span></span>
<span data-ttu-id="4d4e8-109">**Get-AzDeploymentScriptLog** cmdlet은 배포 스크립트 실행의 로그를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4d4e8-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="4d4e8-110">예제</span><span class="sxs-lookup"><span data-stu-id="4d4e8-110">EXAMPLES</span></span>

### <span data-ttu-id="4d4e8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4d4e8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="4d4e8-112">리소스 그룹 DS-TestRG에서 MyDeploymentScript 이름으로 배포 스크립트의 로그를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4d4e8-112">Gets the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="4d4e8-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="4d4e8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -Tail 3
```

<span data-ttu-id="4d4e8-114">리소스 그룹 DS-TestRG의 MyDeploymentScript 이름이 있는 배포 스크립트의 마지막 3줄을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4d4e8-114">Gets the last 3 lines of the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="4d4e8-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="4d4e8-115">Example 3</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="4d4e8-116">첫 번째 명령은 리소스 그룹 DS-TestRG에서 MyDeploymentScript 이름이 있는 배포 스크립트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4d4e8-116">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="4d4e8-117">두 번째 명령은 주어진 배포 스크립트의 로그를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4d4e8-117">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="4d4e8-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4d4e8-118">PARAMETERS</span></span>

### <span data-ttu-id="4d4e8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d4e8-119">-DefaultProfile</span></span>
<span data-ttu-id="4d4e8-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d4e8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d4e8-121">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="4d4e8-121">-DeploymentScriptObject</span></span>
<span data-ttu-id="4d4e8-122">배포 스크립트 PowerShell 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4d4e8-122">The deployment script PowerShell object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d4e8-123">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="4d4e8-123">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="4d4e8-124">배포 스크립트의 완전히 자격을 갖춘 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4d4e8-124">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="4d4e8-125">예제: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resource/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="4d4e8-125">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d4e8-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4d4e8-126">-Name</span></span>
<span data-ttu-id="4d4e8-127">배포 스크립트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d4e8-127">The name of the deployment script.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d4e8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d4e8-128">-ResourceGroupName</span></span>
<span data-ttu-id="4d4e8-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d4e8-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d4e8-130">-Tail</span><span class="sxs-lookup"><span data-stu-id="4d4e8-130">-Tail</span></span>
<span data-ttu-id="4d4e8-131">출력을 마지막 n줄로 제한</span><span class="sxs-lookup"><span data-stu-id="4d4e8-131">Limit output to last n lines</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d4e8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d4e8-132">CommonParameters</span></span>
<span data-ttu-id="4d4e8-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4d4e8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d4e8-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d4e8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d4e8-135">입력</span><span class="sxs-lookup"><span data-stu-id="4d4e8-135">INPUTS</span></span>

### <span data-ttu-id="4d4e8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4d4e8-136">System.String</span></span>

### <span data-ttu-id="4d4e8-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="4d4e8-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="4d4e8-138">출력</span><span class="sxs-lookup"><span data-stu-id="4d4e8-138">OUTPUTS</span></span>

### <span data-ttu-id="4d4e8-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="4d4e8-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="4d4e8-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4d4e8-140">NOTES</span></span>

## <span data-ttu-id="4d4e8-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d4e8-141">RELATED LINKS</span></span>
