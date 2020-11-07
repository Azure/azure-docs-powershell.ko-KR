---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
ms.openlocfilehash: f9532ebaffaaae6a1429cb7ce8680283572c1775
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699319"
---
# <span data-ttu-id="9f286-101">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="9f286-101">Save-AzResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="9f286-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f286-102">SYNOPSIS</span></span>
<span data-ttu-id="9f286-103">리소스 그룹 배포 템플릿을 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f286-103">Saves a resource group deployment template to a file.</span></span>

## <span data-ttu-id="9f286-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9f286-104">SYNTAX</span></span>

```
Save-AzResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9f286-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9f286-105">DESCRIPTION</span></span>
<span data-ttu-id="9f286-106">**AzResourceGroupDeploymentTemplate** cmdlet은 리소스 그룹 배포 템플릿을 JSON 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f286-106">The **Save-AzResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="9f286-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9f286-107">EXAMPLES</span></span>

### <span data-ttu-id="9f286-108">예제 1: 배포 서식 파일 저장</span><span class="sxs-lookup"><span data-stu-id="9f286-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="9f286-109">이 명령은 TestDeployment에서 배포 템플릿을 가져와 현재 디렉터리에 JSON 파일로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f286-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="9f286-110">변수</span><span class="sxs-lookup"><span data-stu-id="9f286-110">PARAMETERS</span></span>

### <span data-ttu-id="9f286-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9f286-111">-ApiVersion</span></span>
<span data-ttu-id="9f286-112">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f286-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9f286-113">지정 하지 않으면 최신 API 버전이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f286-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="9f286-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f286-114">-DefaultProfile</span></span>
<span data-ttu-id="9f286-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9f286-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f286-116">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="9f286-116">-DeploymentName</span></span>
<span data-ttu-id="9f286-117">배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f286-117">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="9f286-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9f286-118">-Force</span></span>
<span data-ttu-id="9f286-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f286-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9f286-120">-Path</span><span class="sxs-lookup"><span data-stu-id="9f286-120">-Path</span></span>
<span data-ttu-id="9f286-121">서식 파일의 출력 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f286-121">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="9f286-122">-Pre</span><span class="sxs-lookup"><span data-stu-id="9f286-122">-Pre</span></span>
<span data-ttu-id="9f286-123">사용할 API 버전을 자동으로 결정할 때이 cmdlet이 시험판 API 버전을 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9f286-123">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="9f286-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f286-124">-ResourceGroupName</span></span>
<span data-ttu-id="9f286-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f286-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9f286-126">-확인</span><span class="sxs-lookup"><span data-stu-id="9f286-126">-Confirm</span></span>
<span data-ttu-id="9f286-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f286-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f286-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f286-128">-WhatIf</span></span>
<span data-ttu-id="9f286-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9f286-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f286-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f286-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f286-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f286-131">CommonParameters</span></span>
<span data-ttu-id="9f286-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f286-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f286-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f286-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f286-134">입력</span><span class="sxs-lookup"><span data-stu-id="9f286-134">INPUTS</span></span>

### <span data-ttu-id="9f286-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9f286-135">System.String</span></span>

## <span data-ttu-id="9f286-136">출력</span><span class="sxs-lookup"><span data-stu-id="9f286-136">OUTPUTS</span></span>

### <span data-ttu-id="9f286-137">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="9f286-137">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9f286-138">상속자</span><span class="sxs-lookup"><span data-stu-id="9f286-138">NOTES</span></span>

## <span data-ttu-id="9f286-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f286-139">RELATED LINKS</span></span>
