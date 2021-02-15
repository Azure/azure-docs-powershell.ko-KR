---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 0ac89ed099029fbbabe90e07da7ba9c204449db9
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400742"
---
# <span data-ttu-id="06e31-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="06e31-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="06e31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06e31-102">SYNOPSIS</span></span>
<span data-ttu-id="06e31-103">백end를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-103">Updates a Backend.</span></span>

## <span data-ttu-id="06e31-104">구문</span><span class="sxs-lookup"><span data-stu-id="06e31-104">SYNTAX</span></span>

```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06e31-105">설명</span><span class="sxs-lookup"><span data-stu-id="06e31-105">DESCRIPTION</span></span>
<span data-ttu-id="06e31-106">API Management에서 기존 백안을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="06e31-107">예제</span><span class="sxs-lookup"><span data-stu-id="06e31-107">EXAMPLES</span></span>

### <span data-ttu-id="06e31-108">백end 123에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="06e31-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06e31-109">PARAMETERS</span></span>

### <span data-ttu-id="06e31-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="06e31-110">-BackendId</span></span>
<span data-ttu-id="06e31-111">새 백end의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-111">Identifier of new backend.</span></span>
<span data-ttu-id="06e31-112">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-112">This parameter is required.</span></span>

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

### <span data-ttu-id="06e31-113">-Context</span><span class="sxs-lookup"><span data-stu-id="06e31-113">-Context</span></span>
<span data-ttu-id="06e31-114">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="06e31-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e31-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="06e31-116">-Credential</span></span>
<span data-ttu-id="06e31-117">백end와 대화할 때 사용할 자격 증명 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="06e31-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-118">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e31-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e31-119">-DefaultProfile</span></span>
<span data-ttu-id="06e31-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06e31-121">-Description</span><span class="sxs-lookup"><span data-stu-id="06e31-121">-Description</span></span>
<span data-ttu-id="06e31-122">백end 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-122">Backend Description.</span></span>
<span data-ttu-id="06e31-123">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="06e31-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06e31-124">-PassThru</span></span>
<span data-ttu-id="06e31-125">이 cmdlet이 이 cmdlet이 수정하는  **PsApiManagementBackend를** 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="06e31-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="06e31-126">-Protocol</span></span>
<span data-ttu-id="06e31-127">백end 통신 프로토콜(http 또는 soap)</span><span class="sxs-lookup"><span data-stu-id="06e31-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="06e31-128">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-128">This parameter is optional</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e31-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="06e31-129">-Proxy</span></span>
<span data-ttu-id="06e31-130">백end에 요청을 보내는 동안 사용할 프록시 서버 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="06e31-131">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-131">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e31-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06e31-132">-ResourceId</span></span>
<span data-ttu-id="06e31-133">외부 시스템의 리소스 관리 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="06e31-134">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-134">This parameter is optional.</span></span>
<span data-ttu-id="06e31-135">이 URL은 Logic Apps, Function Apps 또는 Api Apps의 Arm 리소스 ID일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="06e31-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="06e31-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="06e31-137">Service Fabric 클러스터 백end 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="06e31-138">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-138">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e31-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="06e31-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="06e31-140">백end와 대화할 때 인증서 체인 유효성 검사를 건너뛸지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="06e31-141">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-141">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e31-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="06e31-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="06e31-143">백end와 대화할 때 인증서 이름 유효성 검사를 건너뛸지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="06e31-144">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-144">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e31-145">-Title</span><span class="sxs-lookup"><span data-stu-id="06e31-145">-Title</span></span>
<span data-ttu-id="06e31-146">백end 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-146">Backend Title.</span></span>
<span data-ttu-id="06e31-147">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="06e31-148">-Url</span><span class="sxs-lookup"><span data-stu-id="06e31-148">-Url</span></span>
<span data-ttu-id="06e31-149">백end에 대한 런타임 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="06e31-150">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="06e31-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06e31-151">-Confirm</span></span>
<span data-ttu-id="06e31-152">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06e31-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06e31-153">-WhatIf</span></span>
<span data-ttu-id="06e31-154">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="06e31-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06e31-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06e31-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e31-156">CommonParameters</span></span>
<span data-ttu-id="06e31-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="06e31-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e31-158">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="06e31-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e31-159">입력</span><span class="sxs-lookup"><span data-stu-id="06e31-159">INPUTS</span></span>

### <span data-ttu-id="06e31-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="06e31-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="06e31-161">System.String</span><span class="sxs-lookup"><span data-stu-id="06e31-161">System.String</span></span>

### <span data-ttu-id="06e31-162">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="06e31-162">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="06e31-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="06e31-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="06e31-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="06e31-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="06e31-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="06e31-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="06e31-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="06e31-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="06e31-167">출력</span><span class="sxs-lookup"><span data-stu-id="06e31-167">OUTPUTS</span></span>

### <span data-ttu-id="06e31-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="06e31-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="06e31-169">참고 사항</span><span class="sxs-lookup"><span data-stu-id="06e31-169">NOTES</span></span>

## <span data-ttu-id="06e31-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06e31-170">RELATED LINKS</span></span>

[<span data-ttu-id="06e31-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="06e31-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="06e31-172">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="06e31-172">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="06e31-173">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="06e31-173">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="06e31-174">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="06e31-174">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="06e31-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="06e31-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
