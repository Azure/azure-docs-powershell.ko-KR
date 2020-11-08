---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 608450112b7cd4f54ee0f08f0f29c3aa707fff9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215902"
---
# <span data-ttu-id="251d6-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="251d6-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="251d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="251d6-102">SYNOPSIS</span></span>
<span data-ttu-id="251d6-103">배포 스크립트 실행의 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="251d6-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="251d6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="251d6-104">SYNTAX</span></span>

### <span data-ttu-id="251d6-105">GetDeploymentScriptLogByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="251d6-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="251d6-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="251d6-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="251d6-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="251d6-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="251d6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="251d6-108">DESCRIPTION</span></span>
<span data-ttu-id="251d6-109">**AzDeploymentScriptLog** cmdlet은 배포 스크립트 실행의 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="251d6-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="251d6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="251d6-110">EXAMPLES</span></span>

### <span data-ttu-id="251d6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="251d6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="251d6-112">리소스 그룹 DS-TestRG의 이름 MyDeploymentScript를 사용 하 여 배포 스크립트의 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="251d6-112">Gets the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="251d6-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="251d6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -Tail 3
```

<span data-ttu-id="251d6-114">리소스 그룹 DS-TestRG의 이름 MyDeploymentScript를 사용 하 여 배포 스크립트 로그의 마지막 세 줄을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="251d6-114">Gets the last 3 lines of the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="251d6-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="251d6-115">Example 3</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="251d6-116">첫 번째 명령은 리소스 그룹 DS-TestRG의 이름 MyDeploymentScript를 사용 하 여 배포 스크립트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="251d6-116">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="251d6-117">두 번째 명령은 지정 된 배포 스크립트의 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="251d6-117">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="251d6-118">변수</span><span class="sxs-lookup"><span data-stu-id="251d6-118">PARAMETERS</span></span>

### <span data-ttu-id="251d6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="251d6-119">-DefaultProfile</span></span>
<span data-ttu-id="251d6-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="251d6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="251d6-121">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="251d6-121">-DeploymentScriptObject</span></span>
<span data-ttu-id="251d6-122">배포 스크립트 PowerShell 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="251d6-122">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="251d6-123">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="251d6-123">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="251d6-124">배포 스크립트의 정규화 된 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="251d6-124">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="251d6-125">예:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="251d6-125">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="251d6-126">-이름</span><span class="sxs-lookup"><span data-stu-id="251d6-126">-Name</span></span>
<span data-ttu-id="251d6-127">배포 스크립트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="251d6-127">The name of the deployment script.</span></span>

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

### <span data-ttu-id="251d6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="251d6-128">-ResourceGroupName</span></span>
<span data-ttu-id="251d6-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="251d6-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="251d6-130">-꼬리</span><span class="sxs-lookup"><span data-stu-id="251d6-130">-Tail</span></span>
<span data-ttu-id="251d6-131">출력을 지난 n 줄로 제한</span><span class="sxs-lookup"><span data-stu-id="251d6-131">Limit output to last n lines</span></span>

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

### <span data-ttu-id="251d6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="251d6-132">CommonParameters</span></span>
<span data-ttu-id="251d6-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="251d6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="251d6-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="251d6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="251d6-135">입력</span><span class="sxs-lookup"><span data-stu-id="251d6-135">INPUTS</span></span>

### <span data-ttu-id="251d6-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="251d6-136">System.String</span></span>

### <span data-ttu-id="251d6-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="251d6-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="251d6-138">출력</span><span class="sxs-lookup"><span data-stu-id="251d6-138">OUTPUTS</span></span>

### <span data-ttu-id="251d6-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="251d6-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="251d6-140">상속자</span><span class="sxs-lookup"><span data-stu-id="251d6-140">NOTES</span></span>

## <span data-ttu-id="251d6-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="251d6-141">RELATED LINKS</span></span>
