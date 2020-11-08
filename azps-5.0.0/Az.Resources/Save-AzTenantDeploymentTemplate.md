---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-aztenantdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
ms.openlocfilehash: dcee9317e6aad113088dc3498a337e16e61b6320
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226528"
---
# <span data-ttu-id="811bd-101">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="811bd-101">Save-AzTenantDeploymentTemplate</span></span>

## <span data-ttu-id="811bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="811bd-102">SYNOPSIS</span></span>
<span data-ttu-id="811bd-103">배포 템플릿을 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="811bd-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="811bd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="811bd-104">SYNTAX</span></span>

### <span data-ttu-id="811bd-105">SaveByDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="811bd-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="811bd-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="811bd-106">SaveByDeploymentObject</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="811bd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="811bd-107">DESCRIPTION</span></span>
<span data-ttu-id="811bd-108">**AzTenantDeploymentTemplate** cmdlet은 배포 템플릿을 테 넌 트 범위에서 배포를 위해 JSON 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="811bd-108">The **Save-AzTenantDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at tenant scope.</span></span>

## <span data-ttu-id="811bd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="811bd-109">EXAMPLES</span></span>

### <span data-ttu-id="811bd-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="811bd-110">Example 1</span></span>
```powershell
PS C:\> Save-AzTenantDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="811bd-111">이 명령은 TestDeployment에서 배포 템플릿을 가져와 현재 디렉터리에 JSON 파일로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="811bd-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="811bd-112">예제 2: 배포 가져오기 및 서식 파일 저장</span><span class="sxs-lookup"><span data-stu-id="811bd-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzTenantDeploymentTemplate -Name "RolesDeployment" | Save-AzTenantDeploymentTemplate
```

<span data-ttu-id="811bd-113">이 명령은 현재 테 넌 트 범위의 배포 "역할 배포"를 가져오고 해당 템플릿을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="811bd-113">This command gets the deployment "RolesDeployment" at the current tenant scope and saves its template.</span></span>

## <span data-ttu-id="811bd-114">변수</span><span class="sxs-lookup"><span data-stu-id="811bd-114">PARAMETERS</span></span>

### <span data-ttu-id="811bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="811bd-115">-DefaultProfile</span></span>
<span data-ttu-id="811bd-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="811bd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="811bd-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="811bd-117">-DeploymentName</span></span>
<span data-ttu-id="811bd-118">배포 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="811bd-118">The deployment name.</span></span>

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

### <span data-ttu-id="811bd-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="811bd-119">-DeploymentObject</span></span>
<span data-ttu-id="811bd-120">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="811bd-120">The deployment object.</span></span>

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

### <span data-ttu-id="811bd-121">-Force</span><span class="sxs-lookup"><span data-stu-id="811bd-121">-Force</span></span>
<span data-ttu-id="811bd-122">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="811bd-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="811bd-123">-Path</span><span class="sxs-lookup"><span data-stu-id="811bd-123">-Path</span></span>
<span data-ttu-id="811bd-124">서식 파일의 출력 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="811bd-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="811bd-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="811bd-125">-Pre</span></span>
<span data-ttu-id="811bd-126">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="811bd-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="811bd-127">-확인</span><span class="sxs-lookup"><span data-stu-id="811bd-127">-Confirm</span></span>
<span data-ttu-id="811bd-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="811bd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="811bd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="811bd-129">-WhatIf</span></span>
<span data-ttu-id="811bd-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="811bd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="811bd-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="811bd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="811bd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="811bd-132">CommonParameters</span></span>
<span data-ttu-id="811bd-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="811bd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="811bd-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="811bd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="811bd-135">입력</span><span class="sxs-lookup"><span data-stu-id="811bd-135">INPUTS</span></span>

### <span data-ttu-id="811bd-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="811bd-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="811bd-137">출력</span><span class="sxs-lookup"><span data-stu-id="811bd-137">OUTPUTS</span></span>

### <span data-ttu-id="811bd-138">SdkModels. PSTemplatePath에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="811bd-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="811bd-139">상속자</span><span class="sxs-lookup"><span data-stu-id="811bd-139">NOTES</span></span>

## <span data-ttu-id="811bd-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="811bd-140">RELATED LINKS</span></span>
