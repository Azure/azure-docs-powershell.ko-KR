---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 855127362fbcbf906755affde0bec6de5e7f2698
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044319"
---
# <span data-ttu-id="c05bd-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="c05bd-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="c05bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c05bd-102">SYNOPSIS</span></span>
<span data-ttu-id="c05bd-103">배포 스크립트 실행의 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c05bd-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="c05bd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c05bd-104">SYNTAX</span></span>

### <span data-ttu-id="c05bd-105">GetDeploymentScriptLogByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c05bd-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c05bd-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="c05bd-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c05bd-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="c05bd-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptInputObject] <PsDeploymentScript>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c05bd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c05bd-108">DESCRIPTION</span></span>
<span data-ttu-id="c05bd-109">**AzDeploymentScriptLog** cmdlet은 배포 스크립트 실행의 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c05bd-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="c05bd-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c05bd-110">EXAMPLES</span></span>

### <span data-ttu-id="c05bd-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c05bd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="c05bd-112">리소스 그룹 DS-TestRG의 이름 MyDeploymentScript를 사용 하 여 배포 스크립트의 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c05bd-112">Gets log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="c05bd-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="c05bd-113">Example 2</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="c05bd-114">첫 번째 명령은 리소스 그룹 DS-TestRG의 이름 MyDeploymentScript를 사용 하 여 배포 스크립트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c05bd-114">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="c05bd-115">두 번째 명령은 지정 된 배포 스크립트의 로그를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c05bd-115">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="c05bd-116">변수</span><span class="sxs-lookup"><span data-stu-id="c05bd-116">PARAMETERS</span></span>

### <span data-ttu-id="c05bd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c05bd-117">-DefaultProfile</span></span>
<span data-ttu-id="c05bd-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c05bd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c05bd-119">-DeploymentScriptInputObject</span><span class="sxs-lookup"><span data-stu-id="c05bd-119">-DeploymentScriptInputObject</span></span>
<span data-ttu-id="c05bd-120">배포 스크립트 PowerShell 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c05bd-120">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c05bd-121">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="c05bd-121">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="c05bd-122">배포 스크립트의 정규화 된 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="c05bd-122">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="c05bd-123">예:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="c05bd-123">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c05bd-124">-이름</span><span class="sxs-lookup"><span data-stu-id="c05bd-124">-Name</span></span>
<span data-ttu-id="c05bd-125">배포 스크립트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c05bd-125">The name of the deployment script.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c05bd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c05bd-126">-ResourceGroupName</span></span>
<span data-ttu-id="c05bd-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c05bd-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c05bd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c05bd-128">CommonParameters</span></span>
<span data-ttu-id="c05bd-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c05bd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c05bd-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c05bd-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c05bd-131">입력</span><span class="sxs-lookup"><span data-stu-id="c05bd-131">INPUTS</span></span>

### <span data-ttu-id="c05bd-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c05bd-132">System.String</span></span>

### <span data-ttu-id="c05bd-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="c05bd-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="c05bd-134">출력</span><span class="sxs-lookup"><span data-stu-id="c05bd-134">OUTPUTS</span></span>

### <span data-ttu-id="c05bd-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="c05bd-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="c05bd-136">상속자</span><span class="sxs-lookup"><span data-stu-id="c05bd-136">NOTES</span></span>

## <span data-ttu-id="c05bd-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c05bd-137">RELATED LINKS</span></span>
