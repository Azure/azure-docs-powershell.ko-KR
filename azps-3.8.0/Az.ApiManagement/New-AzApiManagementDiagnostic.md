---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
ms.openlocfilehash: 1c3bea7efffe066ec85b44ec9e5f0f7c222efcf8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042241"
---
# <span data-ttu-id="11e6c-101">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="11e6c-101">New-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="11e6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="11e6c-103">전역 범위 또는 Api 범위에서 새 진단을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-103">Creates a new diagnostics at the Global scope or Api Scope.</span></span>

## <span data-ttu-id="11e6c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11e6c-104">SYNTAX</span></span>

```
New-AzApiManagementDiagnostic -Context <PsApiManagementContext> -LoggerId <String> [-DiagnosticId <String>]
 [-AlwaysLog <String>] [-ApiId <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11e6c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="11e6c-105">DESCRIPTION</span></span>
<span data-ttu-id="11e6c-106">Cmdlet **AzApiManagementDiagnostic** 는 전역 범위 또는 특정 Api 범위에서 진단 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-106">The cmdlet **New-AzApiManagementDiagnostic** creates a diagnostic entity either at Global scope or specific Api scope.</span></span>

## <span data-ttu-id="11e6c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="11e6c-107">EXAMPLES</span></span>

### <span data-ttu-id="11e6c-108">예제 1: 새 전역 범위 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="11e6c-108">Example 1 : Create a new Global scope Diagnostic</span></span>
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

<span data-ttu-id="11e6c-109">이 예제에서는 전역 범위에서 진단 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-109">This example create a diagnostic entity at the Global Scope.</span></span>

### <span data-ttu-id="11e6c-110">예제 2: Api 범위에서 진단 만들기</span><span class="sxs-lookup"><span data-stu-id="11e6c-110">Example 2: Create a diagnostic at Api scope</span></span>
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

<span data-ttu-id="11e6c-111">위의 예제에서는 API에 대 한 진단 유틸리티를 만들어 `httpbin` 헤더 및 100 바이트의 본문을 `azuremonitor` 로 거에 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-111">The example above create a diagnostic for the API `httpbin` to log the Header and 100 Bytes of Body to `azuremonitor` logger.</span></span>

## <span data-ttu-id="11e6c-112">변수</span><span class="sxs-lookup"><span data-stu-id="11e6c-112">PARAMETERS</span></span>

### <span data-ttu-id="11e6c-113">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="11e6c-113">-AlwaysLog</span></span>
<span data-ttu-id="11e6c-114">샘플링 설정을 적용 하지 않아야 하는 유형의 메시지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-114">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="11e6c-115">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="11e6c-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="11e6c-116">-ApiId</span></span>
<span data-ttu-id="11e6c-117">기존 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-117">Identifier of existing API.</span></span>
<span data-ttu-id="11e6c-118">지정 된 경우 API 범위 정책이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-118">If specified will set API-scope policy.</span></span>
<span data-ttu-id="11e6c-119">이 매개 변수는 필수 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-119">This parameters is required.</span></span>

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

### <span data-ttu-id="11e6c-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="11e6c-120">-BackendSetting</span></span>
<span data-ttu-id="11e6c-121">백 엔드에 수신/송신 Http 메시지에 대 한 진단 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="11e6c-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="11e6c-123">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="11e6c-123">-Context</span></span>
<span data-ttu-id="11e6c-124">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="11e6c-125">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-125">This parameter is required.</span></span>

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

### <span data-ttu-id="11e6c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e6c-126">-DefaultProfile</span></span>
<span data-ttu-id="11e6c-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11e6c-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="11e6c-128">-DiagnosticId</span></span>
<span data-ttu-id="11e6c-129">진단 엔터티의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-129">Identifier of the diagnostics entity.</span></span>
<span data-ttu-id="11e6c-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="11e6c-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="11e6c-131">-FrontEndSetting</span></span>
<span data-ttu-id="11e6c-132">게이트웨이로 들어오는/나가는 Http 메시지에 대 한 진단 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="11e6c-133">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="11e6c-134">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="11e6c-134">-LoggerId</span></span>
<span data-ttu-id="11e6c-135">진단을 푸시할로 거의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-135">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="11e6c-136">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-136">This parameter is required.</span></span>

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

### <span data-ttu-id="11e6c-137">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="11e6c-137">-SamplingSetting</span></span>
<span data-ttu-id="11e6c-138">진단의 샘플링 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-138">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="11e6c-139">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="11e6c-140">-확인</span><span class="sxs-lookup"><span data-stu-id="11e6c-140">-Confirm</span></span>
<span data-ttu-id="11e6c-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11e6c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11e6c-142">-WhatIf</span></span>
<span data-ttu-id="11e6c-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11e6c-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11e6c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e6c-145">CommonParameters</span></span>
<span data-ttu-id="11e6c-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11e6c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e6c-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="11e6c-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e6c-148">입력</span><span class="sxs-lookup"><span data-stu-id="11e6c-148">INPUTS</span></span>

### <span data-ttu-id="11e6c-149">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="11e6c-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="11e6c-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="11e6c-150">System.String</span></span>

### <span data-ttu-id="11e6c-151">ApiManagement. ServiceManagement. \ PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="11e6c-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="11e6c-152">ApiManagement. ServiceManagement. \ PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="11e6c-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="11e6c-153">출력</span><span class="sxs-lookup"><span data-stu-id="11e6c-153">OUTPUTS</span></span>

### <span data-ttu-id="11e6c-154">ApiManagement. ServiceManagement. \ PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="11e6c-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="11e6c-155">상속자</span><span class="sxs-lookup"><span data-stu-id="11e6c-155">NOTES</span></span>

## <span data-ttu-id="11e6c-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11e6c-156">RELATED LINKS</span></span>

[<span data-ttu-id="11e6c-157">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="11e6c-157">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="11e6c-158">제거-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="11e6c-158">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="11e6c-159">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="11e6c-159">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="11e6c-160">새로운 AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="11e6c-160">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

[<span data-ttu-id="11e6c-161">새로운 AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="11e6c-161">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)