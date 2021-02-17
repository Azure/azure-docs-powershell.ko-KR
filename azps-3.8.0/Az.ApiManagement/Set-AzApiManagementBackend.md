---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 8631120178a256aa1ec5b817727f9362f6d8f076
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407287"
---
# <span data-ttu-id="10a25-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="10a25-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="10a25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10a25-102">SYNOPSIS</span></span>
<span data-ttu-id="10a25-103">백end를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-103">Updates a Backend.</span></span>

## <span data-ttu-id="10a25-104">구문</span><span class="sxs-lookup"><span data-stu-id="10a25-104">SYNTAX</span></span>

### <span data-ttu-id="10a25-105">ContextParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="10a25-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10a25-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="10a25-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10a25-107">설명</span><span class="sxs-lookup"><span data-stu-id="10a25-107">DESCRIPTION</span></span>
<span data-ttu-id="10a25-108">API Management에서 기존 백안을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="10a25-109">예제</span><span class="sxs-lookup"><span data-stu-id="10a25-109">EXAMPLES</span></span>

### <span data-ttu-id="10a25-110">백end 123에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="10a25-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10a25-111">PARAMETERS</span></span>

### <span data-ttu-id="10a25-112">-BackendId</span><span class="sxs-lookup"><span data-stu-id="10a25-112">-BackendId</span></span>
<span data-ttu-id="10a25-113">새 백end의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-113">Identifier of new backend.</span></span>
<span data-ttu-id="10a25-114">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-114">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a25-115">-Context</span><span class="sxs-lookup"><span data-stu-id="10a25-115">-Context</span></span>
<span data-ttu-id="10a25-116">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="10a25-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10a25-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="10a25-118">-Credential</span></span>
<span data-ttu-id="10a25-119">백end와 대화할 때 사용할 자격 증명 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="10a25-120">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="10a25-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10a25-121">-DefaultProfile</span></span>
<span data-ttu-id="10a25-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10a25-123">-Description</span><span class="sxs-lookup"><span data-stu-id="10a25-123">-Description</span></span>
<span data-ttu-id="10a25-124">백end 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-124">Backend Description.</span></span>
<span data-ttu-id="10a25-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="10a25-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10a25-126">-InputObject</span></span>
<span data-ttu-id="10a25-127">PsApiManagementBackend의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="10a25-128">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10a25-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10a25-129">-PassThru</span></span>
<span data-ttu-id="10a25-130">이 cmdlet이 이 cmdlet이 수정하는  **PsApiManagementBackend를** 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="10a25-131">-Protocol</span><span class="sxs-lookup"><span data-stu-id="10a25-131">-Protocol</span></span>
<span data-ttu-id="10a25-132">백end 통신 프로토콜(http 또는 soap)</span><span class="sxs-lookup"><span data-stu-id="10a25-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="10a25-133">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-133">This parameter is optional</span></span>

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

### <span data-ttu-id="10a25-134">-Proxy</span><span class="sxs-lookup"><span data-stu-id="10a25-134">-Proxy</span></span>
<span data-ttu-id="10a25-135">백end에 요청을 보내는 동안 사용할 프록시 서버 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="10a25-136">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="10a25-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10a25-137">-ResourceId</span></span>
<span data-ttu-id="10a25-138">외부 시스템의 리소스 관리 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="10a25-139">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-139">This parameter is optional.</span></span>
<span data-ttu-id="10a25-140">이 URL은 Logic Apps, Function Apps 또는 Api Apps의 Arm 리소스 ID일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="10a25-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="10a25-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="10a25-142">Service Fabric 클러스터 백end 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="10a25-143">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="10a25-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="10a25-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="10a25-145">백end와 대화할 때 인증서 체인 유효성 검사를 건너뛸지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="10a25-146">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="10a25-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="10a25-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="10a25-148">백end와 대화할 때 인증서 이름 유효성 검사를 건너뛸지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="10a25-149">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="10a25-150">-Title</span><span class="sxs-lookup"><span data-stu-id="10a25-150">-Title</span></span>
<span data-ttu-id="10a25-151">백end 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-151">Backend Title.</span></span>
<span data-ttu-id="10a25-152">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="10a25-153">-Url</span><span class="sxs-lookup"><span data-stu-id="10a25-153">-Url</span></span>
<span data-ttu-id="10a25-154">백end에 대한 런타임 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="10a25-155">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="10a25-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10a25-156">-Confirm</span></span>
<span data-ttu-id="10a25-157">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10a25-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10a25-158">-WhatIf</span></span>
<span data-ttu-id="10a25-159">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="10a25-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10a25-160">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10a25-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a25-161">CommonParameters</span></span>
<span data-ttu-id="10a25-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="10a25-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a25-163">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="10a25-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a25-164">입력</span><span class="sxs-lookup"><span data-stu-id="10a25-164">INPUTS</span></span>

### <span data-ttu-id="10a25-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="10a25-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="10a25-166">System.String</span><span class="sxs-lookup"><span data-stu-id="10a25-166">System.String</span></span>

### <span data-ttu-id="10a25-167">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="10a25-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="10a25-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="10a25-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="10a25-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="10a25-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="10a25-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10a25-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="10a25-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="10a25-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="10a25-172">출력</span><span class="sxs-lookup"><span data-stu-id="10a25-172">OUTPUTS</span></span>

### <span data-ttu-id="10a25-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="10a25-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="10a25-174">참고 사항</span><span class="sxs-lookup"><span data-stu-id="10a25-174">NOTES</span></span>

## <span data-ttu-id="10a25-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10a25-175">RELATED LINKS</span></span>

[<span data-ttu-id="10a25-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="10a25-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="10a25-177">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="10a25-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="10a25-178">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="10a25-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="10a25-179">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="10a25-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="10a25-180">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="10a25-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
