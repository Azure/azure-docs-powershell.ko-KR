---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: b5c3ca86129e622a90a84d099961a8f8dd433eef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215906"
---
# <span data-ttu-id="5f06c-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="5f06c-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="5f06c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f06c-102">SYNOPSIS</span></span>
<span data-ttu-id="5f06c-103">배포 스크립트를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f06c-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="5f06c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5f06c-104">SYNTAX</span></span>

### <span data-ttu-id="5f06c-105">ListDeploymentScript (기본값)</span><span class="sxs-lookup"><span data-stu-id="5f06c-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5f06c-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="5f06c-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f06c-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="5f06c-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f06c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5f06c-108">DESCRIPTION</span></span>
<span data-ttu-id="5f06c-109">**AzDeploymentScript** cmdlet은 단일 배포 스크립트 또는 배포 스크립트 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f06c-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="5f06c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5f06c-110">EXAMPLES</span></span>

### <span data-ttu-id="5f06c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5f06c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="5f06c-112">현재 사용자의 컨텍스트에서 구독에 있는 배포 스크립트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f06c-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="5f06c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="5f06c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="5f06c-114">리소스 그룹 DS-TestRg 배포 스크립트를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f06c-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="5f06c-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="5f06c-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="5f06c-116">리소스 그룹 DS-TestRG의 이름 MyDeploymentScript를 사용 하 여 배포 스크립트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f06c-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="5f06c-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="5f06c-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="5f06c-118">지정 된 리소스 Id를 사용 하 여 배포 스크립트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f06c-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="5f06c-119">변수</span><span class="sxs-lookup"><span data-stu-id="5f06c-119">PARAMETERS</span></span>

### <span data-ttu-id="5f06c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f06c-120">-DefaultProfile</span></span>
<span data-ttu-id="5f06c-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f06c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f06c-122">-Id</span><span class="sxs-lookup"><span data-stu-id="5f06c-122">-Id</span></span>
<span data-ttu-id="5f06c-123">배포 스크립트의 정규화 된 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="5f06c-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="5f06c-124">예:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="5f06c-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="5f06c-125">-이름</span><span class="sxs-lookup"><span data-stu-id="5f06c-125">-Name</span></span>
<span data-ttu-id="5f06c-126">배포 스크립트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5f06c-126">The name of the deployment script</span></span>

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

### <span data-ttu-id="5f06c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f06c-127">-ResourceGroupName</span></span>
<span data-ttu-id="5f06c-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5f06c-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="5f06c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f06c-129">CommonParameters</span></span>
<span data-ttu-id="5f06c-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f06c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5f06c-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f06c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f06c-132">입력</span><span class="sxs-lookup"><span data-stu-id="5f06c-132">INPUTS</span></span>

### <span data-ttu-id="5f06c-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5f06c-133">System.String</span></span>

## <span data-ttu-id="5f06c-134">출력</span><span class="sxs-lookup"><span data-stu-id="5f06c-134">OUTPUTS</span></span>

### <span data-ttu-id="5f06c-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="5f06c-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="5f06c-136">상속자</span><span class="sxs-lookup"><span data-stu-id="5f06c-136">NOTES</span></span>

## <span data-ttu-id="5f06c-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f06c-137">RELATED LINKS</span></span>