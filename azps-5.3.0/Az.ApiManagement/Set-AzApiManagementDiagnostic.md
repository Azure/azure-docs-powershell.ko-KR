---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: c646e7f39b5149803161bfc7b97ed64b5517dd9e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381753"
---
# <span data-ttu-id="80859-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="80859-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="80859-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80859-102">SYNOPSIS</span></span>
<span data-ttu-id="80859-103">전역 또는 API 범위에서 API Management 진단을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="80859-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="80859-104">구문</span><span class="sxs-lookup"><span data-stu-id="80859-104">SYNTAX</span></span>

### <span data-ttu-id="80859-105">ExpandedParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="80859-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80859-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="80859-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80859-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="80859-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80859-108">설명</span><span class="sxs-lookup"><span data-stu-id="80859-108">DESCRIPTION</span></span>
<span data-ttu-id="80859-109">**Set-AzApiManagementDiagnostic** cmdlet은 전역 또는 API 범위에 구성된 진단을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="80859-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="80859-110">예제</span><span class="sxs-lookup"><span data-stu-id="80859-110">EXAMPLES</span></span>

### <span data-ttu-id="80859-111">예제 1: 전역 범위에서 진단 수정</span><span class="sxs-lookup"><span data-stu-id="80859-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="80859-112">이 명령은 지정된 진단 샘플링 비율을 100%에서 50%로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="80859-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

### <span data-ttu-id="80859-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="80859-113">Example 2</span></span>

<span data-ttu-id="80859-114">전역 또는 API 범위에서 API Management 진단을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="80859-114">Modifies an API Management diagnostic at the Global or Api scope.</span></span> <span data-ttu-id="80859-115">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="80859-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementDiagnostic -AlwaysLog allErrors -ApiId '0001' -Context <PsApiManagementContext> -DiagnosticId 'applicationinsights' -LoggerId 'Logger123' -SamplingSetting <PsApiManagementSamplingSetting>
```

## <span data-ttu-id="80859-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80859-116">PARAMETERS</span></span>

### <span data-ttu-id="80859-117">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="80859-117">-AlwaysLog</span></span>
<span data-ttu-id="80859-118">적용할 수 없는 메시지 샘플링 설정 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="80859-118">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="80859-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="80859-120">-ApiId</span><span class="sxs-lookup"><span data-stu-id="80859-120">-ApiId</span></span>
<span data-ttu-id="80859-121">기존 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-121">Identifier of existing API.</span></span>
<span data-ttu-id="80859-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="80859-123">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="80859-123">-BackendSetting</span></span>
<span data-ttu-id="80859-124">백end에 대한 수신/발신 Http 메시지에 대한 진단 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-124">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="80859-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="80859-126">-Context</span><span class="sxs-lookup"><span data-stu-id="80859-126">-Context</span></span>
<span data-ttu-id="80859-127">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="80859-128">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-128">This parameter is required.</span></span>

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

### <span data-ttu-id="80859-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80859-129">-DefaultProfile</span></span>
<span data-ttu-id="80859-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80859-131">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="80859-131">-DiagnosticId</span></span>
<span data-ttu-id="80859-132">기존 진단의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-132">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="80859-133">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-133">This parameter is required.</span></span>

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

### <span data-ttu-id="80859-134">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="80859-134">-FrontEndSetting</span></span>
<span data-ttu-id="80859-135">게이트웨이로 들어오는/보내기 Http 메시지에 대한 진단 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-135">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="80859-136">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="80859-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80859-137">-InputObject</span></span>
<span data-ttu-id="80859-138">PsApiManagementDiagnostic의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-138">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="80859-139">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-139">This parameter is required.</span></span>

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

### <span data-ttu-id="80859-140">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="80859-140">-LoggerId</span></span>
<span data-ttu-id="80859-141">진단을 푸시할 로거의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-141">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="80859-142">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-142">This parameter is required.</span></span>

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

### <span data-ttu-id="80859-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80859-143">-PassThru</span></span>
<span data-ttu-id="80859-144">지정된 경우 진단 집합을 나타내는 Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic 형식의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="80859-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80859-145">-ResourceId</span></span>
<span data-ttu-id="80859-146">진단 또는 Api 진단의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="80859-147">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-147">This parameter is required.</span></span>

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

### <span data-ttu-id="80859-148">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="80859-148">-SamplingSetting</span></span>
<span data-ttu-id="80859-149">진단의 샘플링 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-149">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="80859-150">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="80859-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="80859-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80859-151">-Confirm</span></span>
<span data-ttu-id="80859-152">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="80859-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80859-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80859-153">-WhatIf</span></span>
<span data-ttu-id="80859-154">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="80859-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80859-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80859-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80859-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80859-156">CommonParameters</span></span>
<span data-ttu-id="80859-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="80859-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80859-158">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="80859-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80859-159">입력</span><span class="sxs-lookup"><span data-stu-id="80859-159">INPUTS</span></span>

### <span data-ttu-id="80859-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="80859-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="80859-161">System.String</span><span class="sxs-lookup"><span data-stu-id="80859-161">System.String</span></span>

### <span data-ttu-id="80859-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="80859-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="80859-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="80859-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="80859-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="80859-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="80859-165">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="80859-165">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="80859-166">출력</span><span class="sxs-lookup"><span data-stu-id="80859-166">OUTPUTS</span></span>

### <span data-ttu-id="80859-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="80859-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="80859-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="80859-168">NOTES</span></span>

## <span data-ttu-id="80859-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80859-169">RELATED LINKS</span></span>
