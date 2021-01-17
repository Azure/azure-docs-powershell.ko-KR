---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: 74605a57ab3f2c0898bf3eeb80950f86d4f65d94
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490623"
---
# <span data-ttu-id="c1772-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c1772-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="c1772-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1772-102">SYNOPSIS</span></span>
<span data-ttu-id="c1772-103">리소스 그룹을 템플릿으로 캡처하고 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="c1772-104">구문</span><span class="sxs-lookup"><span data-stu-id="c1772-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-SkipResourceNameParameterization] [-SkipAllParameterization] [-Resource <String[]>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1772-105">설명</span><span class="sxs-lookup"><span data-stu-id="c1772-105">DESCRIPTION</span></span>
<span data-ttu-id="c1772-106">**Export-AzResourceGroup** cmdlet은 지정된 리소스 그룹을 템플릿으로 캡처하고 JSON 파일에 저장합니다. 리소스 그룹에 일부 리소스를 이미 만든 다음 템플릿 지원 배포를 사용하는 이점을 활용하려는 시나리오에서 유용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="c1772-107">이 cmdlet을 사용하면 리소스 그룹의 기존 리소스에 대한 템플릿을 생성하여 쉽게 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="c1772-108">이 cmdlet이 템플릿의 일부를 생성하지 못하는 경우도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="c1772-109">경고 메시지는 실패한 리소스를 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="c1772-110">템플릿은 성공한 부분에 대해 계속 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="c1772-111">예제</span><span class="sxs-lookup"><span data-stu-id="c1772-111">EXAMPLES</span></span>

### <span data-ttu-id="c1772-112">예제 1: 리소스 그룹 내보내기</span><span class="sxs-lookup"><span data-stu-id="c1772-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="c1772-113">이 명령은 TestGroup이라는 리소스 그룹을 템플릿으로 캡처하고 현재 디렉터리의 JSON 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="c1772-114">예제 2: 리소스 그룹에서 단일 리소스 내보내기</span><span class="sxs-lookup"><span data-stu-id="c1772-114">Example 2: Export a single resource from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -Resource "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVirtualMachine"
```

<span data-ttu-id="c1772-115">이 명령은 "TestGroup" 리소스 그룹에서 "TestVirtualMachine"이라는 Virtual Machine 리소스를 템플릿으로 캡처하고 현재 디렉터리의 JSON 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-115">This command captures the Virtual Machine resource named "TestVirtualMachine" from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="c1772-116">예제 3: 리소스 그룹에서 선택된 리소스 내보내기</span><span class="sxs-lookup"><span data-stu-id="c1772-116">Example 3: Export a selection of resources from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -SkipAllParameterization -Resource @(
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVm",
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Network/networkInterfaces/TestNic"
)
```

<span data-ttu-id="c1772-117">이 명령은 "TestGroup" 리소스 그룹의 두 리소스를 템플릿으로 캡처하고 현재 디렉터리의 JSON 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-117">This command captures two resources from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span> <span data-ttu-id="c1772-118">생성된 템플릿에는 생성된 매개 변수가 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-118">The generated template will not contain any generated parameters.</span></span>

## <span data-ttu-id="c1772-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1772-119">PARAMETERS</span></span>

### <span data-ttu-id="c1772-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c1772-120">-ApiVersion</span></span>
<span data-ttu-id="c1772-121">사용할 리소스 공급자 API의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c1772-122">지정하지 않으면 최신 API 버전이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-122">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="c1772-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1772-123">-DefaultProfile</span></span>
<span data-ttu-id="c1772-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c1772-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1772-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c1772-125">-Force</span></span>
<span data-ttu-id="c1772-126">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c1772-127">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="c1772-127">-IncludeComments</span></span>
<span data-ttu-id="c1772-128">이 작업은 주석이 있는 템플릿을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-128">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="c1772-129">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="c1772-129">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="c1772-130">이 작업은 기본값으로 템플릿 매개 변수를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-130">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="c1772-131">-Path</span><span class="sxs-lookup"><span data-stu-id="c1772-131">-Path</span></span>
<span data-ttu-id="c1772-132">템플릿 파일의 출력 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="c1772-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="c1772-133">-Pre</span></span>
<span data-ttu-id="c1772-134">사용할 API 버전을 자동으로 결정할 때 이 cmdlet이 릴리스 전 API 버전을 사용 중입니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="c1772-135">-Resource</span><span class="sxs-lookup"><span data-stu-id="c1772-135">-Resource</span></span>
<span data-ttu-id="c1772-136">결과를 필터링할 resourceId 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-136">A list of resourceIds to filter the results by.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1772-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1772-137">-ResourceGroupName</span></span>
<span data-ttu-id="c1772-138">내보낼 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-138">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="c1772-139">-SkipAllParameterization</span><span class="sxs-lookup"><span data-stu-id="c1772-139">-SkipAllParameterization</span></span>
<span data-ttu-id="c1772-140">모든 매개 변수화를 건너뜁.</span><span class="sxs-lookup"><span data-stu-id="c1772-140">Skip all parameterization.</span></span>

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

### <span data-ttu-id="c1772-141">-SkipResourceNameParameterization</span><span class="sxs-lookup"><span data-stu-id="c1772-141">-SkipResourceNameParameterization</span></span>
<span data-ttu-id="c1772-142">리소스 이름 매개 변수화 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="c1772-142">Skip resource name parameterization.</span></span>

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

### <span data-ttu-id="c1772-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1772-143">-Confirm</span></span>
<span data-ttu-id="c1772-144">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1772-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1772-145">-WhatIf</span></span>
<span data-ttu-id="c1772-146">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c1772-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1772-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1772-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1772-148">CommonParameters</span></span>
<span data-ttu-id="c1772-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c1772-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1772-150">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c1772-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1772-151">입력</span><span class="sxs-lookup"><span data-stu-id="c1772-151">INPUTS</span></span>

### <span data-ttu-id="c1772-152">System.String</span><span class="sxs-lookup"><span data-stu-id="c1772-152">System.String</span></span>

## <span data-ttu-id="c1772-153">출력</span><span class="sxs-lookup"><span data-stu-id="c1772-153">OUTPUTS</span></span>

### <span data-ttu-id="c1772-154">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="c1772-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c1772-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c1772-155">NOTES</span></span>

## <span data-ttu-id="c1772-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1772-156">RELATED LINKS</span></span>

[<span data-ttu-id="c1772-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c1772-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


