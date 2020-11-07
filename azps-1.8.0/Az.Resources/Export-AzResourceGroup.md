---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: f1801aab91887b3dd0d6a9842c7d4a6de1988a88
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93711944"
---
# <span data-ttu-id="6578d-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6578d-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="6578d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6578d-102">SYNOPSIS</span></span>
<span data-ttu-id="6578d-103">리소스 그룹을 서식 파일로 캡처하여 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6578d-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="6578d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6578d-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6578d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6578d-105">DESCRIPTION</span></span>
<span data-ttu-id="6578d-106">**Export-AzResourceGroup** cmdlet은 지정 된 리소스 그룹을 템플릿으로 캡처하여 JSON 파일에 저장 합니다. 이는 리소스 그룹에 리소스를 이미 만든 다음 서식 파일을 사용 하 여 얻을 수 있는 기능을 활용 하려는 시나리오에 유용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6578d-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="6578d-107">이 cmdlet을 사용 하면 리소스 그룹의 기존 리소스에 대 한 템플릿을 생성 하 여 쉽게 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6578d-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="6578d-108">이 cmdlet이 템플릿의 일부를 생성 하지 못하는 경우가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6578d-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="6578d-109">실패 한 리소스를 알리는 경고 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6578d-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="6578d-110">이 서식 파일은 성공한 파트에 대해 계속 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6578d-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="6578d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="6578d-111">EXAMPLES</span></span>

### <span data-ttu-id="6578d-112">예제 1: 리소스 그룹 내보내기</span><span class="sxs-lookup"><span data-stu-id="6578d-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="6578d-113">이 명령은 TestGroup 이라는 리소스 그룹을 템플릿으로 캡처하여 현재 디렉터리의 JSON 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6578d-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="6578d-114">변수</span><span class="sxs-lookup"><span data-stu-id="6578d-114">PARAMETERS</span></span>

### <span data-ttu-id="6578d-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6578d-115">-ApiVersion</span></span>
<span data-ttu-id="6578d-116">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6578d-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6578d-117">지정 하지 않으면 최신 API 버전이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6578d-117">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="6578d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6578d-118">-DefaultProfile</span></span>
<span data-ttu-id="6578d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6578d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6578d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6578d-120">-Force</span></span>
<span data-ttu-id="6578d-121">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6578d-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6578d-122">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="6578d-122">-IncludeComments</span></span>
<span data-ttu-id="6578d-123">이 작업에서 템플릿을 주석으로 내보내도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6578d-123">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="6578d-124">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="6578d-124">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="6578d-125">이 작업에서 템플릿 매개 변수를 기본값으로 내보내도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6578d-125">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="6578d-126">-Path</span><span class="sxs-lookup"><span data-stu-id="6578d-126">-Path</span></span>
<span data-ttu-id="6578d-127">서식 파일의 출력 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6578d-127">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="6578d-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="6578d-128">-Pre</span></span>
<span data-ttu-id="6578d-129">사용할 API 버전을 자동으로 결정할 때이 cmdlet이 시험판 API 버전을 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6578d-129">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="6578d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6578d-130">-ResourceGroupName</span></span>
<span data-ttu-id="6578d-131">내보낼 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6578d-131">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="6578d-132">-확인</span><span class="sxs-lookup"><span data-stu-id="6578d-132">-Confirm</span></span>
<span data-ttu-id="6578d-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6578d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6578d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6578d-134">-WhatIf</span></span>
<span data-ttu-id="6578d-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6578d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6578d-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6578d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6578d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6578d-137">CommonParameters</span></span>
<span data-ttu-id="6578d-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6578d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6578d-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6578d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6578d-140">입력</span><span class="sxs-lookup"><span data-stu-id="6578d-140">INPUTS</span></span>

### <span data-ttu-id="6578d-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6578d-141">System.String</span></span>

## <span data-ttu-id="6578d-142">출력</span><span class="sxs-lookup"><span data-stu-id="6578d-142">OUTPUTS</span></span>

### <span data-ttu-id="6578d-143">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="6578d-143">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6578d-144">상속자</span><span class="sxs-lookup"><span data-stu-id="6578d-144">NOTES</span></span>

## <span data-ttu-id="6578d-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6578d-145">RELATED LINKS</span></span>

[<span data-ttu-id="6578d-146">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6578d-146">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


