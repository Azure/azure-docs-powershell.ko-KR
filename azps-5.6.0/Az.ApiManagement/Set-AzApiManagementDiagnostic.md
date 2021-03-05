---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: c9cb592713f7a24739651d36855fdf595ffc7eeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965424"
---
# <span data-ttu-id="5425f-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5425f-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="5425f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5425f-102">SYNOPSIS</span></span>
<span data-ttu-id="5425f-103">전역 또는 Api 범위에서 API Management 진단을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="5425f-104">구문</span><span class="sxs-lookup"><span data-stu-id="5425f-104">SYNTAX</span></span>

### <span data-ttu-id="5425f-105">ExpandedParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="5425f-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5425f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5425f-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5425f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5425f-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5425f-108">설명</span><span class="sxs-lookup"><span data-stu-id="5425f-108">DESCRIPTION</span></span>
<span data-ttu-id="5425f-109">cmdlet **Set-AzApiManagementDiagnostic는** 전역 또는 Api 범위에서 구성된 진단을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="5425f-110">예제</span><span class="sxs-lookup"><span data-stu-id="5425f-110">EXAMPLES</span></span>

### <span data-ttu-id="5425f-111">예제 1: 전역 범위에서 진단 수정</span><span class="sxs-lookup"><span data-stu-id="5425f-111">Example 1: Modify a diagnostic at the Global scope</span></span>
```powershell
PS c:\> $context =New-AzApiManagementContext -ResourceGroupName Api-Default-WestUS -ServiceName contoso
PS c:\> $diagnostic=Get-AzApiManagementDiagnostic -Context $context -DiagnosticId "applicationinsights"
PS c:\> $diagnostic

DiagnosticId      : applicationinsights
AlwaysLog         : allErrors
LoggerId          : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/loggers/backendapisachinc
Sampling          : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
Frontend          :
Backend           :
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso


PS c:\> $diagnostic.Sampling

SamplingType Percentage
------------ ----------
fixed               100

PS c:\> $diagnostic.Sampling.Percentage = 50
PS c:\> $diagnostic.Sampling

SamplingType Percentage
------------ ----------
fixed                50

PS c:\> Set-AzApiManagementDiagnostic -InputObject $diagnostic
```

<span data-ttu-id="5425f-112">이 명령은 지정된 진단 샘플링 비율을 100에서 50%로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

### <span data-ttu-id="5425f-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="5425f-113">Example 2</span></span>

<span data-ttu-id="5425f-114">전역 또는 Api 범위에서 API Management 진단을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-114">Modifies an API Management diagnostic at the Global or Api scope.</span></span> <span data-ttu-id="5425f-115">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="5425f-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementDiagnostic -AlwaysLog allErrors -ApiId '0001' -Context <PsApiManagementContext> -DiagnosticId 'applicationinsights' -LoggerId 'Logger123' -SamplingSetting <PsApiManagementSamplingSetting>
```

## <span data-ttu-id="5425f-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5425f-116">PARAMETERS</span></span>

### <span data-ttu-id="5425f-117">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="5425f-117">-AlwaysLog</span></span>
<span data-ttu-id="5425f-118">샘플링 설정이 적용되지 않는 메시지 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-118">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="5425f-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="5425f-120">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5425f-120">-ApiId</span></span>
<span data-ttu-id="5425f-121">기존 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-121">Identifier of existing API.</span></span>
<span data-ttu-id="5425f-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5425f-123">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="5425f-123">-BackendSetting</span></span>
<span data-ttu-id="5425f-124">백end에 대한 수신/발신 Http 메시지에 대한 진단 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-124">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="5425f-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-125">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5425f-126">-Context</span><span class="sxs-lookup"><span data-stu-id="5425f-126">-Context</span></span>
<span data-ttu-id="5425f-127">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5425f-128">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5425f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5425f-129">-DefaultProfile</span></span>
<span data-ttu-id="5425f-130">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5425f-131">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="5425f-131">-DiagnosticId</span></span>
<span data-ttu-id="5425f-132">기존 진단의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-132">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="5425f-133">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5425f-134">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="5425f-134">-FrontEndSetting</span></span>
<span data-ttu-id="5425f-135">게이트웨이에 대한 수신/외출 Http 메시지에 대한 진단 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-135">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="5425f-136">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-136">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5425f-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5425f-137">-InputObject</span></span>
<span data-ttu-id="5425f-138">PsApiManagementDiagnostic의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-138">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="5425f-139">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-139">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5425f-140">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="5425f-140">-LoggerId</span></span>
<span data-ttu-id="5425f-141">진단을 푸시할 로거의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-141">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="5425f-142">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-142">This parameter is required.</span></span>

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

### <span data-ttu-id="5425f-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5425f-143">-PassThru</span></span>
<span data-ttu-id="5425f-144">지정된 경우 Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic 형식의 인스턴스는 진단 집합을 나타내는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5425f-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5425f-145">-ResourceId</span></span>
<span data-ttu-id="5425f-146">진단 또는 Api 진단의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="5425f-147">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-147">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5425f-148">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="5425f-148">-SamplingSetting</span></span>
<span data-ttu-id="5425f-149">진단의 샘플링 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-149">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="5425f-150">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-150">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5425f-151">-확인</span><span class="sxs-lookup"><span data-stu-id="5425f-151">-Confirm</span></span>
<span data-ttu-id="5425f-152">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5425f-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5425f-153">-WhatIf</span></span>
<span data-ttu-id="5425f-154">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5425f-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5425f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5425f-156">CommonParameters</span></span>
<span data-ttu-id="5425f-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5425f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5425f-158">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5425f-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5425f-159">입력</span><span class="sxs-lookup"><span data-stu-id="5425f-159">INPUTS</span></span>

### <span data-ttu-id="5425f-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5425f-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5425f-161">System.String</span><span class="sxs-lookup"><span data-stu-id="5425f-161">System.String</span></span>

### <span data-ttu-id="5425f-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5425f-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="5425f-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="5425f-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="5425f-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="5425f-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="5425f-165">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5425f-165">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5425f-166">출력</span><span class="sxs-lookup"><span data-stu-id="5425f-166">OUTPUTS</span></span>

### <span data-ttu-id="5425f-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5425f-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="5425f-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5425f-168">NOTES</span></span>

## <span data-ttu-id="5425f-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5425f-169">RELATED LINKS</span></span>
