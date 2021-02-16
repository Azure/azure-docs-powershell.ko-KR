---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: b5c3ca86129e622a90a84d099961a8f8dd433eef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178836"
---
# <span data-ttu-id="36719-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="36719-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="36719-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36719-102">SYNOPSIS</span></span>
<span data-ttu-id="36719-103">배포 스크립트를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="36719-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="36719-104">구문</span><span class="sxs-lookup"><span data-stu-id="36719-104">SYNTAX</span></span>

### <span data-ttu-id="36719-105">ListDeploymentScript(기본값)</span><span class="sxs-lookup"><span data-stu-id="36719-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36719-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="36719-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36719-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="36719-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36719-108">설명</span><span class="sxs-lookup"><span data-stu-id="36719-108">DESCRIPTION</span></span>
<span data-ttu-id="36719-109">**Get-AzDeploymentScript** cmdlet은 단일 배포 스크립트 또는 배포 스크립트 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="36719-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="36719-110">예제</span><span class="sxs-lookup"><span data-stu-id="36719-110">EXAMPLES</span></span>

### <span data-ttu-id="36719-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="36719-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="36719-112">현재 사용자의 컨텍스트에서 구독의 배포 스크립트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="36719-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="36719-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="36719-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="36719-114">리소스 그룹 DS-TestRg의 배포 스크립트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="36719-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="36719-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="36719-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="36719-116">리소스 그룹 DS-TestRG에서 MyDeploymentScript 이름이 있는 배포 스크립트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="36719-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="36719-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="36719-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="36719-118">주어진 리소스 ID를 사용하여 배포 스크립트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="36719-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="36719-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36719-119">PARAMETERS</span></span>

### <span data-ttu-id="36719-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36719-120">-DefaultProfile</span></span>
<span data-ttu-id="36719-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36719-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36719-122">-Id</span><span class="sxs-lookup"><span data-stu-id="36719-122">-Id</span></span>
<span data-ttu-id="36719-123">배포 스크립트의 정식 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="36719-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="36719-124">예: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="36719-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36719-125">-Name</span><span class="sxs-lookup"><span data-stu-id="36719-125">-Name</span></span>
<span data-ttu-id="36719-126">배포 스크립트의 이름</span><span class="sxs-lookup"><span data-stu-id="36719-126">The name of the deployment script</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36719-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36719-127">-ResourceGroupName</span></span>
<span data-ttu-id="36719-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36719-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListDeploymentScript
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36719-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36719-129">CommonParameters</span></span>
<span data-ttu-id="36719-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36719-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="36719-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="36719-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36719-132">입력</span><span class="sxs-lookup"><span data-stu-id="36719-132">INPUTS</span></span>

### <span data-ttu-id="36719-133">System.String</span><span class="sxs-lookup"><span data-stu-id="36719-133">System.String</span></span>

## <span data-ttu-id="36719-134">출력</span><span class="sxs-lookup"><span data-stu-id="36719-134">OUTPUTS</span></span>

### <span data-ttu-id="36719-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="36719-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="36719-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="36719-136">NOTES</span></span>

## <span data-ttu-id="36719-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36719-137">RELATED LINKS</span></span>