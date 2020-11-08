---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: fc6346bc87b5bc69fdcd06474227afec7de55dee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042267"
---
# <span data-ttu-id="04285-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="04285-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="04285-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04285-102">SYNOPSIS</span></span>
<span data-ttu-id="04285-103">새 백엔드 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04285-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="04285-104">구문과</span><span class="sxs-lookup"><span data-stu-id="04285-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04285-105">설명은</span><span class="sxs-lookup"><span data-stu-id="04285-105">DESCRIPTION</span></span>
<span data-ttu-id="04285-106">Api Management에 새 백엔드 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04285-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="04285-107">예제의</span><span class="sxs-lookup"><span data-stu-id="04285-107">EXAMPLES</span></span>

### <span data-ttu-id="04285-108">기본 권한 부여 스키마를 사용 하 여 백엔드 123 만들기</span><span class="sxs-lookup"><span data-stu-id="04285-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="04285-109">새 백 엔드 만들기</span><span class="sxs-lookup"><span data-stu-id="04285-109">Creates a new Backend</span></span>

## <span data-ttu-id="04285-110">변수</span><span class="sxs-lookup"><span data-stu-id="04285-110">PARAMETERS</span></span>

### <span data-ttu-id="04285-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="04285-111">-BackendId</span></span>
<span data-ttu-id="04285-112">새 백 엔드의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-112">Identifier of new backend.</span></span>
<span data-ttu-id="04285-113">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-113">This parameter is optional.</span></span>
<span data-ttu-id="04285-114">지정 하지 않으면가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04285-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="04285-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="04285-115">-Context</span></span>
<span data-ttu-id="04285-116">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="04285-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-117">This parameter is required.</span></span>

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

### <span data-ttu-id="04285-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="04285-118">-Credential</span></span>
<span data-ttu-id="04285-119">백 엔드로 대화할 때 사용 해야 하는 자격 증명 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="04285-120">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="04285-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04285-121">-DefaultProfile</span></span>
<span data-ttu-id="04285-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04285-123">-설명</span><span class="sxs-lookup"><span data-stu-id="04285-123">-Description</span></span>
<span data-ttu-id="04285-124">백 엔드 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-124">Backend Description.</span></span>
<span data-ttu-id="04285-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="04285-126">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="04285-126">-Protocol</span></span>
<span data-ttu-id="04285-127">백 엔드 통신 프로토콜.</span><span class="sxs-lookup"><span data-stu-id="04285-127">Backend Communication protocol.</span></span>
<span data-ttu-id="04285-128">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-128">This parameter is required.</span></span>
<span data-ttu-id="04285-129">유효한 값은 ' http ' 및 ' soap '입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="04285-130">-프록시</span><span class="sxs-lookup"><span data-stu-id="04285-130">-Proxy</span></span>
<span data-ttu-id="04285-131">백 엔드에 요청을 보내는 동안 사용할 프록시 서버 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="04285-132">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="04285-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04285-133">-ResourceId</span></span>
<span data-ttu-id="04285-134">외부 시스템 리소스의 관리 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="04285-135">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-135">This parameter is optional.</span></span>
<span data-ttu-id="04285-136">이 url은 논리 앱, 함수 앱 또는 Api 앱의 Arm 리소스 Id 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04285-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="04285-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="04285-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="04285-138">Service Fabric 클러스터 백 엔드 정보.</span><span class="sxs-lookup"><span data-stu-id="04285-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="04285-139">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="04285-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="04285-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="04285-141">백 엔드로 대화 하는 경우 인증서 체인 유효성 검사를 건너뛸지 여부</span><span class="sxs-lookup"><span data-stu-id="04285-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="04285-142">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="04285-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="04285-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="04285-144">백 엔드로 대화 하는 경우 인증서 이름 유효성 검사를 건너뛸지 여부</span><span class="sxs-lookup"><span data-stu-id="04285-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="04285-145">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="04285-146">-Title</span><span class="sxs-lookup"><span data-stu-id="04285-146">-Title</span></span>
<span data-ttu-id="04285-147">백 엔드 제목.</span><span class="sxs-lookup"><span data-stu-id="04285-147">Backend Title.</span></span>
<span data-ttu-id="04285-148">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="04285-149">-Url</span><span class="sxs-lookup"><span data-stu-id="04285-149">-Url</span></span>
<span data-ttu-id="04285-150">백 엔드의 런타임 Url입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="04285-151">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="04285-151">This parameter is required.</span></span>

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

### <span data-ttu-id="04285-152">-확인</span><span class="sxs-lookup"><span data-stu-id="04285-152">-Confirm</span></span>
<span data-ttu-id="04285-153">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="04285-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04285-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04285-154">-WhatIf</span></span>
<span data-ttu-id="04285-155">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="04285-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04285-156">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04285-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04285-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04285-157">CommonParameters</span></span>
<span data-ttu-id="04285-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04285-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04285-159">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="04285-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04285-160">입력</span><span class="sxs-lookup"><span data-stu-id="04285-160">INPUTS</span></span>

### <span data-ttu-id="04285-161">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="04285-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="04285-162">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="04285-162">System.String</span></span>

### <span data-ttu-id="04285-163">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="04285-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="04285-164">ApiManagement. ServiceManagement. \ PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="04285-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="04285-165">ApiManagement. ServiceManagement. \ PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="04285-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="04285-166">ApiManagement. ServiceManagement. \ PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="04285-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="04285-167">출력</span><span class="sxs-lookup"><span data-stu-id="04285-167">OUTPUTS</span></span>

### <span data-ttu-id="04285-168">ApiManagement. ServiceManagement. \ PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="04285-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="04285-169">상속자</span><span class="sxs-lookup"><span data-stu-id="04285-169">NOTES</span></span>

## <span data-ttu-id="04285-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04285-170">RELATED LINKS</span></span>

[<span data-ttu-id="04285-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="04285-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="04285-172">새로운 AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="04285-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="04285-173">새로운 AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="04285-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="04285-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="04285-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="04285-175">제거-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="04285-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

