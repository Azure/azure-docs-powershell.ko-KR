---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 8f146c6516226c800f45489e1f7fa5d37173e151
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711498"
---
# <span data-ttu-id="9673d-101">Save-AzureRmResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="9673d-101">Save-AzureRmResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="9673d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9673d-102">SYNOPSIS</span></span>
<span data-ttu-id="9673d-103">리소스 그룹 배포 템플릿을 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9673d-103">Saves a resource group deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9673d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9673d-104">SYNTAX</span></span>

```
Save-AzureRmResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9673d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9673d-105">DESCRIPTION</span></span>
<span data-ttu-id="9673d-106">**AzureRmResourceGroupDeploymentTemplate** cmdlet은 리소스 그룹 배포 템플릿을 JSON 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9673d-106">The **Save-AzureRmResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="9673d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9673d-107">EXAMPLES</span></span>

### <span data-ttu-id="9673d-108">예제 1: 배포 서식 파일 저장</span><span class="sxs-lookup"><span data-stu-id="9673d-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzureRmResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="9673d-109">이 명령은 TestDeployment에서 배포 템플릿을 가져와 현재 디렉터리에 JSON 파일로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9673d-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="9673d-110">변수</span><span class="sxs-lookup"><span data-stu-id="9673d-110">PARAMETERS</span></span>

### <span data-ttu-id="9673d-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9673d-111">-ApiVersion</span></span>
<span data-ttu-id="9673d-112">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9673d-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9673d-113">지정 하지 않으면 최신 API 버전이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9673d-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="9673d-114">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="9673d-114">-DeploymentName</span></span>
<span data-ttu-id="9673d-115">배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9673d-115">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="9673d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9673d-116">-Force</span></span>
<span data-ttu-id="9673d-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9673d-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9673d-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9673d-118">-InformationAction</span></span>
<span data-ttu-id="9673d-119">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9673d-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9673d-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9673d-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9673d-121">하기로</span><span class="sxs-lookup"><span data-stu-id="9673d-121">Continue</span></span>
- <span data-ttu-id="9673d-122">숨기기</span><span class="sxs-lookup"><span data-stu-id="9673d-122">Ignore</span></span>
- <span data-ttu-id="9673d-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="9673d-123">Inquire</span></span>
- <span data-ttu-id="9673d-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9673d-124">SilentlyContinue</span></span>
- <span data-ttu-id="9673d-125">중지가</span><span class="sxs-lookup"><span data-stu-id="9673d-125">Stop</span></span>
- <span data-ttu-id="9673d-126">대기</span><span class="sxs-lookup"><span data-stu-id="9673d-126">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9673d-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9673d-127">-InformationVariable</span></span>
<span data-ttu-id="9673d-128">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9673d-128">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9673d-129">-Path</span><span class="sxs-lookup"><span data-stu-id="9673d-129">-Path</span></span>
<span data-ttu-id="9673d-130">서식 파일의 출력 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9673d-130">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="9673d-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="9673d-131">-Pre</span></span>
<span data-ttu-id="9673d-132">사용할 API 버전을 자동으로 결정할 때이 cmdlet이 시험판 API 버전을 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9673d-132">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="9673d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9673d-133">-ResourceGroupName</span></span>
<span data-ttu-id="9673d-134">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9673d-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9673d-135">-확인</span><span class="sxs-lookup"><span data-stu-id="9673d-135">-Confirm</span></span>
<span data-ttu-id="9673d-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9673d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9673d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9673d-137">-WhatIf</span></span>
<span data-ttu-id="9673d-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9673d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9673d-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9673d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9673d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9673d-140">-DefaultProfile</span></span>
<span data-ttu-id="9673d-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9673d-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9673d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9673d-142">CommonParameters</span></span>
<span data-ttu-id="9673d-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9673d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9673d-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9673d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9673d-145">입력</span><span class="sxs-lookup"><span data-stu-id="9673d-145">INPUTS</span></span>

## <span data-ttu-id="9673d-146">출력</span><span class="sxs-lookup"><span data-stu-id="9673d-146">OUTPUTS</span></span>

### <span data-ttu-id="9673d-147">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="9673d-147">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9673d-148">상속자</span><span class="sxs-lookup"><span data-stu-id="9673d-148">NOTES</span></span>

## <span data-ttu-id="9673d-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9673d-149">RELATED LINKS</span></span>

