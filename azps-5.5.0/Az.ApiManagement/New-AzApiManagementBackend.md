---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: 4ed63d0e3b801572698b123038a2022e89672a88
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205701"
---
# <span data-ttu-id="6d4dc-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6d4dc-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="6d4dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d4dc-102">SYNOPSIS</span></span>
<span data-ttu-id="6d4dc-103">새 백end 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="6d4dc-104">구문</span><span class="sxs-lookup"><span data-stu-id="6d4dc-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d4dc-105">설명</span><span class="sxs-lookup"><span data-stu-id="6d4dc-105">DESCRIPTION</span></span>
<span data-ttu-id="6d4dc-106">Api Management에서 새 백 엔트 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="6d4dc-107">예제</span><span class="sxs-lookup"><span data-stu-id="6d4dc-107">EXAMPLES</span></span>

### <span data-ttu-id="6d4dc-108">예제 1: 기본 권한 부여 체계를 사용하여 백end 123 만들기</span><span class="sxs-lookup"><span data-stu-id="6d4dc-108">Example 1: Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="6d4dc-109">새 백end를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-109">Creates a new Backend</span></span>

## <span data-ttu-id="6d4dc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d4dc-110">PARAMETERS</span></span>

### <span data-ttu-id="6d4dc-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="6d4dc-111">-BackendId</span></span>
<span data-ttu-id="6d4dc-112">새 백end의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-112">Identifier of new backend.</span></span>
<span data-ttu-id="6d4dc-113">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-113">This parameter is optional.</span></span>
<span data-ttu-id="6d4dc-114">지정하지 않으면 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="6d4dc-115">-Context</span><span class="sxs-lookup"><span data-stu-id="6d4dc-115">-Context</span></span>
<span data-ttu-id="6d4dc-116">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6d4dc-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d4dc-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="6d4dc-118">-Credential</span></span>
<span data-ttu-id="6d4dc-119">백end와 대화할 때 사용할 자격 증명 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="6d4dc-120">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="6d4dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d4dc-121">-DefaultProfile</span></span>
<span data-ttu-id="6d4dc-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d4dc-123">-Description</span><span class="sxs-lookup"><span data-stu-id="6d4dc-123">-Description</span></span>
<span data-ttu-id="6d4dc-124">백end 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-124">Backend Description.</span></span>
<span data-ttu-id="6d4dc-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="6d4dc-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="6d4dc-126">-Protocol</span></span>
<span data-ttu-id="6d4dc-127">백end 통신 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-127">Backend Communication protocol.</span></span>
<span data-ttu-id="6d4dc-128">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-128">This parameter is required.</span></span>
<span data-ttu-id="6d4dc-129">유효한 값은 'http' 및 'soap'입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-129">Valid values are 'http' and 'soap'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: http, soap

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d4dc-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="6d4dc-130">-Proxy</span></span>
<span data-ttu-id="6d4dc-131">백end에 요청을 보내는 동안 사용할 프록시 서버 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="6d4dc-132">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="6d4dc-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d4dc-133">-ResourceId</span></span>
<span data-ttu-id="6d4dc-134">외부 시스템의 리소스 관리 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="6d4dc-135">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-135">This parameter is optional.</span></span>
<span data-ttu-id="6d4dc-136">이 URL은 Logic Apps, Function Apps 또는 Api Apps의 Arm 리소스 ID일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="6d4dc-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="6d4dc-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="6d4dc-138">Service Fabric 클러스터 백end 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="6d4dc-139">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="6d4dc-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="6d4dc-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="6d4dc-141">백end와 대화할 때 인증서 체인 유효성 검사를 건너뛸지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="6d4dc-142">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="6d4dc-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="6d4dc-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="6d4dc-144">백end와 대화할 때 인증서 이름 유효성 검사를 건너뛸지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="6d4dc-145">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="6d4dc-146">-Title</span><span class="sxs-lookup"><span data-stu-id="6d4dc-146">-Title</span></span>
<span data-ttu-id="6d4dc-147">백end 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-147">Backend Title.</span></span>
<span data-ttu-id="6d4dc-148">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="6d4dc-149">-Url</span><span class="sxs-lookup"><span data-stu-id="6d4dc-149">-Url</span></span>
<span data-ttu-id="6d4dc-150">백end에 대한 런타임 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="6d4dc-151">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-151">This parameter is required.</span></span>

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

### <span data-ttu-id="6d4dc-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d4dc-152">-Confirm</span></span>
<span data-ttu-id="6d4dc-153">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d4dc-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d4dc-154">-WhatIf</span></span>
<span data-ttu-id="6d4dc-155">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6d4dc-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d4dc-156">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d4dc-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d4dc-157">CommonParameters</span></span>
<span data-ttu-id="6d4dc-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d4dc-159">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6d4dc-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d4dc-160">입력</span><span class="sxs-lookup"><span data-stu-id="6d4dc-160">INPUTS</span></span>

### <span data-ttu-id="6d4dc-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6d4dc-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6d4dc-162">System.String</span><span class="sxs-lookup"><span data-stu-id="6d4dc-162">System.String</span></span>

### <span data-ttu-id="6d4dc-163">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6d4dc-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6d4dc-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="6d4dc-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="6d4dc-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="6d4dc-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="6d4dc-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6d4dc-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="6d4dc-167">출력</span><span class="sxs-lookup"><span data-stu-id="6d4dc-167">OUTPUTS</span></span>

### <span data-ttu-id="6d4dc-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6d4dc-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="6d4dc-169">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6d4dc-169">NOTES</span></span>

## <span data-ttu-id="6d4dc-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d4dc-170">RELATED LINKS</span></span>

[<span data-ttu-id="6d4dc-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6d4dc-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="6d4dc-172">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="6d4dc-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="6d4dc-173">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="6d4dc-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="6d4dc-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6d4dc-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="6d4dc-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6d4dc-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

