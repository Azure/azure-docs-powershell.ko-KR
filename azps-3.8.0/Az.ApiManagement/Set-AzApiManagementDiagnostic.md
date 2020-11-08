---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: f3add9f35e56d4ba6d92b8438b970ddf8c682804
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043857"
---
# <span data-ttu-id="a6725-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a6725-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="a6725-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6725-102">SYNOPSIS</span></span>
<span data-ttu-id="a6725-103">전역 또는 Api 범위에서 API Management 진단을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="a6725-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a6725-104">SYNTAX</span></span>

### <span data-ttu-id="a6725-105">ExpandedParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="a6725-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6725-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a6725-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6725-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a6725-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6725-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a6725-108">DESCRIPTION</span></span>
<span data-ttu-id="a6725-109">Cmdlet **집합-AzApiManagementDiagnostic** 는 전역 또는 Api 범위에서 구성 된 진단을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="a6725-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a6725-110">EXAMPLES</span></span>

### <span data-ttu-id="a6725-111">예제 1: 전역 범위에서 진단 수정</span><span class="sxs-lookup"><span data-stu-id="a6725-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="a6725-112">이 명령은 지정 된 진단 샘플링 백분율을 100에서 50%로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

## <span data-ttu-id="a6725-113">변수</span><span class="sxs-lookup"><span data-stu-id="a6725-113">PARAMETERS</span></span>

### <span data-ttu-id="a6725-114">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="a6725-114">-AlwaysLog</span></span>
<span data-ttu-id="a6725-115">샘플링 설정을 적용 하지 않아야 하는 유형의 메시지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-115">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="a6725-116">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="a6725-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a6725-117">-ApiId</span></span>
<span data-ttu-id="a6725-118">기존 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-118">Identifier of existing API.</span></span>
<span data-ttu-id="a6725-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="a6725-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="a6725-120">-BackendSetting</span></span>
<span data-ttu-id="a6725-121">백 엔드에 수신/송신 Http 메시지에 대 한 진단 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="a6725-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="a6725-123">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="a6725-123">-Context</span></span>
<span data-ttu-id="a6725-124">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a6725-125">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-125">This parameter is required.</span></span>

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

### <span data-ttu-id="a6725-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6725-126">-DefaultProfile</span></span>
<span data-ttu-id="a6725-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6725-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="a6725-128">-DiagnosticId</span></span>
<span data-ttu-id="a6725-129">기존 진단의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-129">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="a6725-130">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-130">This parameter is required.</span></span>

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

### <span data-ttu-id="a6725-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="a6725-131">-FrontEndSetting</span></span>
<span data-ttu-id="a6725-132">게이트웨이로 들어오는/나가는 Http 메시지에 대 한 진단 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="a6725-133">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="a6725-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6725-134">-InputObject</span></span>
<span data-ttu-id="a6725-135">PsApiManagementDiagnostic의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-135">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="a6725-136">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-136">This parameter is required.</span></span>

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

### <span data-ttu-id="a6725-137">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="a6725-137">-LoggerId</span></span>
<span data-ttu-id="a6725-138">진단을 푸시할로 거의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-138">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="a6725-139">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-139">This parameter is required.</span></span>

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

### <span data-ttu-id="a6725-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6725-140">-PassThru</span></span>
<span data-ttu-id="a6725-141">지정한 경우 ApiManagement의 인스턴스가 set 진단을 나타내는 ServiceManagement 유형의 PsApiManagementDiagnostic 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-141">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="a6725-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6725-142">-ResourceId</span></span>
<span data-ttu-id="a6725-143">진단 또는 Api 진단의 팔 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-143">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="a6725-144">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-144">This parameter is required.</span></span>

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

### <span data-ttu-id="a6725-145">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="a6725-145">-SamplingSetting</span></span>
<span data-ttu-id="a6725-146">진단의 샘플링 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-146">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="a6725-147">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="a6725-148">-확인</span><span class="sxs-lookup"><span data-stu-id="a6725-148">-Confirm</span></span>
<span data-ttu-id="a6725-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6725-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6725-150">-WhatIf</span></span>
<span data-ttu-id="a6725-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6725-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6725-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6725-153">CommonParameters</span></span>
<span data-ttu-id="a6725-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6725-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6725-155">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a6725-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6725-156">입력</span><span class="sxs-lookup"><span data-stu-id="a6725-156">INPUTS</span></span>

### <span data-ttu-id="a6725-157">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a6725-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a6725-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a6725-158">System.String</span></span>

### <span data-ttu-id="a6725-159">ApiManagement. ServiceManagement. \ PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a6725-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="a6725-160">ApiManagement. ServiceManagement. \ PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="a6725-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="a6725-161">ApiManagement. ServiceManagement. \ PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="a6725-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="a6725-162">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a6725-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a6725-163">출력</span><span class="sxs-lookup"><span data-stu-id="a6725-163">OUTPUTS</span></span>

### <span data-ttu-id="a6725-164">ApiManagement. ServiceManagement. \ PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a6725-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="a6725-165">상속자</span><span class="sxs-lookup"><span data-stu-id="a6725-165">NOTES</span></span>

## <span data-ttu-id="a6725-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6725-166">RELATED LINKS</span></span>
