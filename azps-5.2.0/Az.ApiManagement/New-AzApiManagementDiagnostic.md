---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
ms.openlocfilehash: f977b4dab003b3d1a1b83f1b81701a6089e1cefa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332349"
---
# <span data-ttu-id="d8054-101">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d8054-101">New-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="d8054-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8054-102">SYNOPSIS</span></span>
<span data-ttu-id="d8054-103">전역 범위 또는 API 범위에서 새 진단을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-103">Creates a new diagnostics at the Global scope or Api Scope.</span></span>

## <span data-ttu-id="d8054-104">구문</span><span class="sxs-lookup"><span data-stu-id="d8054-104">SYNTAX</span></span>

```
New-AzApiManagementDiagnostic -Context <PsApiManagementContext> -LoggerId <String> [-DiagnosticId <String>]
 [-AlwaysLog <String>] [-ApiId <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8054-105">설명</span><span class="sxs-lookup"><span data-stu-id="d8054-105">DESCRIPTION</span></span>
<span data-ttu-id="d8054-106">**New-AzApiManagementDiagnostic** cmdlet은 전역 범위 또는 특정 API 범위에서 진단 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-106">The cmdlet **New-AzApiManagementDiagnostic** creates a diagnostic entity either at Global scope or specific Api scope.</span></span>

## <span data-ttu-id="d8054-107">예제</span><span class="sxs-lookup"><span data-stu-id="d8054-107">EXAMPLES</span></span>

### <span data-ttu-id="d8054-108">예제 1: 새 전역 범위 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="d8054-108">Example 1: Create a new Global scope Diagnostic</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS D:\github\azure-powershell> $logger = Get-AzApiManagementLogger -Context $context -LoggerId "backendapisachinc"
PS D:\github\azure-powershell> $samplingsetting = New-AzApiManagementSamplingSetting -SamplingType fixed -SamplingPercentage 100
PS D:\github\azure-powershell> New-AzApiManagementDiagnostic -LoggerId $logger.LoggerId -Context $context -AlwaysLog allErrors -SamplingSetting $samplingSetting  -DiagnosticId "applicationinsights"

DiagnosticId                 : applicationinsights
ApiId                        :
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUs/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUs
ServiceName                  : contoso
```

<span data-ttu-id="d8054-109">이 예제에서는 전역 범위에서 진단 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-109">This example create a diagnostic entity at the Global Scope.</span></span>

### <span data-ttu-id="d8054-110">예제 2: API 범위에서 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="d8054-110">Example 2: Create a diagnostic at Api scope</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS D:\github\azure-powershell> $logger = Get-AzApiManagementLogger -Context $context -LoggerId azuremonitor
PS D:\github\azure-powershell> $samplingsetting = New-AzApiManagementSamplingSetting -SamplingType fixed -SamplingPercentage 100
PS D:\github\azure-powershell> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -HeadersToLog 'Content-Type', 'User-Agent' -BodyBytesToLog 100
PS D:\github\azure-powershell> $pipelineDiagnostic = New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic
PS D:\github\azure-powershell> New-AzApiManagementDiagnostic -LoggerId $logger.LoggerId -Context $context -ApiId httpbin -AlwaysLog allErrors -SamplingSetting $samplingsetting -FrontEndSetting $pipelineDiagnostic -BackendSetting $pipelineDiagnostic -DiagnosticId azuremonitor

DiagnosticId                 : azuremonitor
ApiId                        : httpbin
AlwaysLog                    : allErrors
LoggerId                     : azuremonitor
EnableHttpCorrelationHeaders :
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
BackendSetting               : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/httpbin/diagnostics/azuremonitor      
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="d8054-111">위의 예제에서는 헤더 및 100 Bytes의 본문을 로거에 기록하는 API에 `httpbin` 대한 `azuremonitor` 진단을 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-111">The example above create a diagnostic for the API `httpbin` to log the Header and 100 Bytes of Body to `azuremonitor` logger.</span></span>

## <span data-ttu-id="d8054-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8054-112">PARAMETERS</span></span>

### <span data-ttu-id="d8054-113">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="d8054-113">-AlwaysLog</span></span>
<span data-ttu-id="d8054-114">적용할 수 없는 메시지 샘플링 설정 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-114">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="d8054-115">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="d8054-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d8054-116">-ApiId</span></span>
<span data-ttu-id="d8054-117">기존 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-117">Identifier of existing API.</span></span>
<span data-ttu-id="d8054-118">지정된 경우 API 범위 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-118">If specified will set API-scope policy.</span></span>
<span data-ttu-id="d8054-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-119">This parameters is required.</span></span>

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

### <span data-ttu-id="d8054-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="d8054-120">-BackendSetting</span></span>
<span data-ttu-id="d8054-121">백end에 대한 수신/발신 Http 메시지에 대한 진단 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="d8054-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="d8054-123">-Context</span><span class="sxs-lookup"><span data-stu-id="d8054-123">-Context</span></span>
<span data-ttu-id="d8054-124">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d8054-125">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8054-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8054-126">-DefaultProfile</span></span>
<span data-ttu-id="d8054-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8054-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="d8054-128">-DiagnosticId</span></span>
<span data-ttu-id="d8054-129">진단 엔터티의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-129">Identifier of the diagnostics entity.</span></span>
<span data-ttu-id="d8054-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="d8054-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="d8054-131">-FrontEndSetting</span></span>
<span data-ttu-id="d8054-132">게이트웨이로 들어오는/보내기 Http 메시지에 대한 진단 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="d8054-133">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="d8054-134">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="d8054-134">-LoggerId</span></span>
<span data-ttu-id="d8054-135">진단을 푸시할 로거의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-135">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="d8054-136">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-136">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8054-137">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="d8054-137">-SamplingSetting</span></span>
<span data-ttu-id="d8054-138">진단의 샘플링 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-138">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="d8054-139">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="d8054-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8054-140">-Confirm</span></span>
<span data-ttu-id="d8054-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8054-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8054-142">-WhatIf</span></span>
<span data-ttu-id="d8054-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d8054-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8054-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8054-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8054-145">CommonParameters</span></span>
<span data-ttu-id="d8054-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d8054-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8054-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d8054-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8054-148">입력</span><span class="sxs-lookup"><span data-stu-id="d8054-148">INPUTS</span></span>

### <span data-ttu-id="d8054-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d8054-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d8054-150">System.String</span><span class="sxs-lookup"><span data-stu-id="d8054-150">System.String</span></span>

### <span data-ttu-id="d8054-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="d8054-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="d8054-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="d8054-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="d8054-153">출력</span><span class="sxs-lookup"><span data-stu-id="d8054-153">OUTPUTS</span></span>

### <span data-ttu-id="d8054-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d8054-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="d8054-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d8054-155">NOTES</span></span>

## <span data-ttu-id="d8054-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8054-156">RELATED LINKS</span></span>

[<span data-ttu-id="d8054-157">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d8054-157">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="d8054-158">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d8054-158">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="d8054-159">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d8054-159">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="d8054-160">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d8054-160">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

[<span data-ttu-id="d8054-161">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="d8054-161">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)