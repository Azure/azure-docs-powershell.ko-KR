---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 7d5d5ecc0f8facf03be72f952722ea30b56fa9ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041741"
---
# <span data-ttu-id="99279-101">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="99279-101">Save-AzResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="99279-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99279-102">SYNOPSIS</span></span>
<span data-ttu-id="99279-103">리소스 그룹 배포 템플릿을 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="99279-103">Saves a resource group deployment template to a file.</span></span>

## <span data-ttu-id="99279-104">구문과</span><span class="sxs-lookup"><span data-stu-id="99279-104">SYNTAX</span></span>

```
Save-AzResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99279-105">설명은</span><span class="sxs-lookup"><span data-stu-id="99279-105">DESCRIPTION</span></span>
<span data-ttu-id="99279-106">**AzResourceGroupDeploymentTemplate** cmdlet은 리소스 그룹 배포 템플릿을 JSON 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="99279-106">The **Save-AzResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="99279-107">예제의</span><span class="sxs-lookup"><span data-stu-id="99279-107">EXAMPLES</span></span>

### <span data-ttu-id="99279-108">예제 1: 배포 서식 파일 저장</span><span class="sxs-lookup"><span data-stu-id="99279-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="99279-109">이 명령은 TestDeployment에서 배포 템플릿을 가져와 현재 디렉터리에 JSON 파일로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="99279-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="99279-110">변수</span><span class="sxs-lookup"><span data-stu-id="99279-110">PARAMETERS</span></span>

### <span data-ttu-id="99279-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="99279-111">-ApiVersion</span></span>
<span data-ttu-id="99279-112">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99279-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="99279-113">지정 하지 않으면 최신 API 버전이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="99279-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="99279-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99279-114">-DefaultProfile</span></span>
<span data-ttu-id="99279-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="99279-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99279-116">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="99279-116">-DeploymentName</span></span>
<span data-ttu-id="99279-117">배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99279-117">Specifies the name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99279-118">-Force</span><span class="sxs-lookup"><span data-stu-id="99279-118">-Force</span></span>
<span data-ttu-id="99279-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="99279-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99279-120">-Path</span><span class="sxs-lookup"><span data-stu-id="99279-120">-Path</span></span>
<span data-ttu-id="99279-121">서식 파일의 출력 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99279-121">Specifies the output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99279-122">-Pre</span><span class="sxs-lookup"><span data-stu-id="99279-122">-Pre</span></span>
<span data-ttu-id="99279-123">사용할 API 버전을 자동으로 결정할 때이 cmdlet이 시험판 API 버전을 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="99279-123">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="99279-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99279-124">-ResourceGroupName</span></span>
<span data-ttu-id="99279-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99279-125">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99279-126">-확인</span><span class="sxs-lookup"><span data-stu-id="99279-126">-Confirm</span></span>
<span data-ttu-id="99279-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="99279-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99279-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99279-128">-WhatIf</span></span>
<span data-ttu-id="99279-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="99279-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99279-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99279-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99279-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99279-131">CommonParameters</span></span>
<span data-ttu-id="99279-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="99279-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99279-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="99279-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99279-134">입력</span><span class="sxs-lookup"><span data-stu-id="99279-134">INPUTS</span></span>

### <span data-ttu-id="99279-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="99279-135">System.String</span></span>

## <span data-ttu-id="99279-136">출력</span><span class="sxs-lookup"><span data-stu-id="99279-136">OUTPUTS</span></span>

### <span data-ttu-id="99279-137">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="99279-137">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="99279-138">상속자</span><span class="sxs-lookup"><span data-stu-id="99279-138">NOTES</span></span>

## <span data-ttu-id="99279-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99279-139">RELATED LINKS</span></span>
