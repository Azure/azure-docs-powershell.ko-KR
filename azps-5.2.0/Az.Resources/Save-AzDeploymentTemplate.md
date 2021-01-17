---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
ms.openlocfilehash: dc6f7c5b66d72ae5c01ecbb8ec93fa737199d06e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345758"
---
# <span data-ttu-id="3654b-101">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="3654b-101">Save-AzDeploymentTemplate</span></span>

## <span data-ttu-id="3654b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3654b-102">SYNOPSIS</span></span>
<span data-ttu-id="3654b-103">배포 템플릿을 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3654b-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="3654b-104">구문</span><span class="sxs-lookup"><span data-stu-id="3654b-104">SYNTAX</span></span>

### <span data-ttu-id="3654b-105">SaveByDeploymentName(기본값)</span><span class="sxs-lookup"><span data-stu-id="3654b-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3654b-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="3654b-106">SaveByDeploymentObject</span></span>
```
Save-AzDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3654b-107">설명</span><span class="sxs-lookup"><span data-stu-id="3654b-107">DESCRIPTION</span></span>
<span data-ttu-id="3654b-108">**Save-AzDeploymentTemplate** cmdlet은 배포 템플릿을 JSON 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3654b-108">The **Save-AzDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="3654b-109">예제</span><span class="sxs-lookup"><span data-stu-id="3654b-109">EXAMPLES</span></span>

### <span data-ttu-id="3654b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3654b-110">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="3654b-111">이 명령은 TestDeployment에서 배포 템플릿을 다운로드하고 현재 디렉터리에 JSON 파일로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3654b-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="3654b-112">예제 2: 배포 및 템플릿 저장</span><span class="sxs-lookup"><span data-stu-id="3654b-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Save-AzDeploymentTemplate
```

<span data-ttu-id="3654b-113">이 명령은 현재 구독 범위에서 배포 "RolesDeployment"를 구하고 템플릿을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3654b-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="3654b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3654b-114">PARAMETERS</span></span>

### <span data-ttu-id="3654b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3654b-115">-DefaultProfile</span></span>
<span data-ttu-id="3654b-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3654b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3654b-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="3654b-117">-DeploymentName</span></span>
<span data-ttu-id="3654b-118">배포 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3654b-118">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3654b-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="3654b-119">-DeploymentObject</span></span>
<span data-ttu-id="3654b-120">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3654b-120">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3654b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3654b-121">-Force</span></span>
<span data-ttu-id="3654b-122">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3654b-122">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3654b-123">-Path</span><span class="sxs-lookup"><span data-stu-id="3654b-123">-Path</span></span>
<span data-ttu-id="3654b-124">템플릿 파일의 출력 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="3654b-124">The output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3654b-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="3654b-125">-Pre</span></span>
<span data-ttu-id="3654b-126">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3654b-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3654b-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3654b-127">-Confirm</span></span>
<span data-ttu-id="3654b-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3654b-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3654b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3654b-129">-WhatIf</span></span>
<span data-ttu-id="3654b-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3654b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3654b-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3654b-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3654b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3654b-132">CommonParameters</span></span>
<span data-ttu-id="3654b-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3654b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3654b-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3654b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3654b-135">입력</span><span class="sxs-lookup"><span data-stu-id="3654b-135">INPUTS</span></span>

### <span data-ttu-id="3654b-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSD</span><span class="sxs-lookup"><span data-stu-id="3654b-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="3654b-137">출력</span><span class="sxs-lookup"><span data-stu-id="3654b-137">OUTPUTS</span></span>

### <span data-ttu-id="3654b-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="3654b-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="3654b-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3654b-139">NOTES</span></span>

## <span data-ttu-id="3654b-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3654b-140">RELATED LINKS</span></span>
