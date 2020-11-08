---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 4e32726b3e7af6608092d29fd52f7a41be042d42
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041787"
---
# <span data-ttu-id="f708b-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="f708b-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="f708b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f708b-102">SYNOPSIS</span></span>
<span data-ttu-id="f708b-103">배포 스크립트 실행의 로그를 디스크에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f708b-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="f708b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f708b-104">SYNTAX</span></span>

### <span data-ttu-id="f708b-105">SaveDeploymentScriptLogByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="f708b-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f708b-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="f708b-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f708b-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="f708b-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptInputObject] <PsDeploymentScript> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f708b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f708b-108">DESCRIPTION</span></span>
<span data-ttu-id="f708b-109">**저장-AzDeploymentScriptLog** 는 배포 스크립트 실행의 로그를 디스크에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f708b-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="f708b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f708b-110">EXAMPLES</span></span>

### <span data-ttu-id="f708b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f708b-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="f708b-112">배포 스크립트의 로그를 지정 된 이름 및 리소스 그룹으로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f708b-112">Saves the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="f708b-113">변수</span><span class="sxs-lookup"><span data-stu-id="f708b-113">PARAMETERS</span></span>

### <span data-ttu-id="f708b-114">-확인</span><span class="sxs-lookup"><span data-stu-id="f708b-114">-Confirm</span></span>
<span data-ttu-id="f708b-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f708b-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f708b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f708b-116">-DefaultProfile</span></span>
<span data-ttu-id="f708b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f708b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f708b-118">-DeploymentScriptInputObject</span><span class="sxs-lookup"><span data-stu-id="f708b-118">-DeploymentScriptInputObject</span></span>
<span data-ttu-id="f708b-119">배포 스크립트 PowerShell 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f708b-119">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: SaveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f708b-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="f708b-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="f708b-121">배포 스크립트의 정규화 된 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="f708b-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="f708b-122">예:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="f708b-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f708b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="f708b-123">-Force</span></span>
<span data-ttu-id="f708b-124">기존 파일을 강제로 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="f708b-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="f708b-125">-이름</span><span class="sxs-lookup"><span data-stu-id="f708b-125">-Name</span></span>
<span data-ttu-id="f708b-126">배포 스크립트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f708b-126">The name of the deployment script.</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f708b-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="f708b-127">-OutputPath</span></span>
<span data-ttu-id="f708b-128">배포 스크립트 로그를 저장할 디렉터리 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="f708b-128">The directory path to save deployment script log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f708b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f708b-129">-ResourceGroupName</span></span>
<span data-ttu-id="f708b-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f708b-130">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f708b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f708b-131">-WhatIf</span></span>
<span data-ttu-id="f708b-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f708b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f708b-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f708b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f708b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f708b-134">CommonParameters</span></span>
<span data-ttu-id="f708b-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f708b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f708b-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f708b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f708b-137">입력</span><span class="sxs-lookup"><span data-stu-id="f708b-137">INPUTS</span></span>

### <span data-ttu-id="f708b-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f708b-138">System.String</span></span>

## <span data-ttu-id="f708b-139">출력</span><span class="sxs-lookup"><span data-stu-id="f708b-139">OUTPUTS</span></span>

### <span data-ttu-id="f708b-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="f708b-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="f708b-141">상속자</span><span class="sxs-lookup"><span data-stu-id="f708b-141">NOTES</span></span>

## <span data-ttu-id="f708b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f708b-142">RELATED LINKS</span></span>
