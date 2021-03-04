---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: 7b61444bb4f3a23e1611e90b79545e1c174b0437
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956640"
---
# <span data-ttu-id="1a274-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="1a274-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="1a274-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a274-102">SYNOPSIS</span></span>
<span data-ttu-id="1a274-103">배포 스크립트를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="1a274-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="1a274-104">구문</span><span class="sxs-lookup"><span data-stu-id="1a274-104">SYNTAX</span></span>

### <span data-ttu-id="1a274-105">ListDeploymentScript(기본값)</span><span class="sxs-lookup"><span data-stu-id="1a274-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a274-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="1a274-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a274-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="1a274-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a274-108">설명</span><span class="sxs-lookup"><span data-stu-id="1a274-108">DESCRIPTION</span></span>
<span data-ttu-id="1a274-109">**Get-AzDeploymentScript** cmdlet은 단일 배포 스크립트 또는 배포 스크립트 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="1a274-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="1a274-110">예제</span><span class="sxs-lookup"><span data-stu-id="1a274-110">EXAMPLES</span></span>

### <span data-ttu-id="1a274-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1a274-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="1a274-112">현재 사용자의 컨텍스트에서 구독에 배포 스크립트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="1a274-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="1a274-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="1a274-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="1a274-114">리소스 그룹 DS-TestRg에 배포 스크립트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="1a274-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="1a274-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="1a274-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="1a274-116">리소스 그룹 DS-TestRG에서 MyDeploymentScript 이름이 있는 배포 스크립트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1a274-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="1a274-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="1a274-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="1a274-118">주어진 리소스 ID를 사용하여 배포 스크립트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1a274-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="1a274-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1a274-119">PARAMETERS</span></span>

### <span data-ttu-id="1a274-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a274-120">-DefaultProfile</span></span>
<span data-ttu-id="1a274-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a274-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a274-122">-Id</span><span class="sxs-lookup"><span data-stu-id="1a274-122">-Id</span></span>
<span data-ttu-id="1a274-123">배포 스크립트의 완전히 자격을 갖춘 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1a274-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="1a274-124">예제: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resource/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="1a274-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="1a274-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1a274-125">-Name</span></span>
<span data-ttu-id="1a274-126">배포 스크립트의 이름</span><span class="sxs-lookup"><span data-stu-id="1a274-126">The name of the deployment script</span></span>

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

### <span data-ttu-id="1a274-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a274-127">-ResourceGroupName</span></span>
<span data-ttu-id="1a274-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a274-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="1a274-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a274-129">CommonParameters</span></span>
<span data-ttu-id="1a274-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1a274-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1a274-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1a274-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a274-132">입력</span><span class="sxs-lookup"><span data-stu-id="1a274-132">INPUTS</span></span>

### <span data-ttu-id="1a274-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1a274-133">System.String</span></span>

## <span data-ttu-id="1a274-134">출력</span><span class="sxs-lookup"><span data-stu-id="1a274-134">OUTPUTS</span></span>

### <span data-ttu-id="1a274-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="1a274-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="1a274-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1a274-136">NOTES</span></span>

## <span data-ttu-id="1a274-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a274-137">RELATED LINKS</span></span>