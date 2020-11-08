---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: 4ed63d0e3b801572698b123038a2022e89672a88
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056611"
---
# <span data-ttu-id="aee6b-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="aee6b-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="aee6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aee6b-102">SYNOPSIS</span></span>
<span data-ttu-id="aee6b-103">새 백엔드 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="aee6b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aee6b-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aee6b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aee6b-105">DESCRIPTION</span></span>
<span data-ttu-id="aee6b-106">Api Management에 새 백엔드 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="aee6b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="aee6b-107">EXAMPLES</span></span>

### <span data-ttu-id="aee6b-108">예제 1: 기본 권한 부여 스키마를 사용 하 여 백엔드 123 만들기</span><span class="sxs-lookup"><span data-stu-id="aee6b-108">Example 1: Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="aee6b-109">새 백 엔드 만들기</span><span class="sxs-lookup"><span data-stu-id="aee6b-109">Creates a new Backend</span></span>

## <span data-ttu-id="aee6b-110">변수</span><span class="sxs-lookup"><span data-stu-id="aee6b-110">PARAMETERS</span></span>

### <span data-ttu-id="aee6b-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="aee6b-111">-BackendId</span></span>
<span data-ttu-id="aee6b-112">새 백 엔드의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-112">Identifier of new backend.</span></span>
<span data-ttu-id="aee6b-113">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-113">This parameter is optional.</span></span>
<span data-ttu-id="aee6b-114">지정 하지 않으면가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="aee6b-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="aee6b-115">-Context</span></span>
<span data-ttu-id="aee6b-116">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="aee6b-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-117">This parameter is required.</span></span>

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

### <span data-ttu-id="aee6b-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="aee6b-118">-Credential</span></span>
<span data-ttu-id="aee6b-119">백 엔드로 대화할 때 사용 해야 하는 자격 증명 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="aee6b-120">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="aee6b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aee6b-121">-DefaultProfile</span></span>
<span data-ttu-id="aee6b-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aee6b-123">-설명</span><span class="sxs-lookup"><span data-stu-id="aee6b-123">-Description</span></span>
<span data-ttu-id="aee6b-124">백 엔드 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-124">Backend Description.</span></span>
<span data-ttu-id="aee6b-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="aee6b-126">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="aee6b-126">-Protocol</span></span>
<span data-ttu-id="aee6b-127">백 엔드 통신 프로토콜.</span><span class="sxs-lookup"><span data-stu-id="aee6b-127">Backend Communication protocol.</span></span>
<span data-ttu-id="aee6b-128">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-128">This parameter is required.</span></span>
<span data-ttu-id="aee6b-129">유효한 값은 ' http ' 및 ' soap '입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="aee6b-130">-프록시</span><span class="sxs-lookup"><span data-stu-id="aee6b-130">-Proxy</span></span>
<span data-ttu-id="aee6b-131">백 엔드에 요청을 보내는 동안 사용할 프록시 서버 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="aee6b-132">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="aee6b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aee6b-133">-ResourceId</span></span>
<span data-ttu-id="aee6b-134">외부 시스템 리소스의 관리 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="aee6b-135">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-135">This parameter is optional.</span></span>
<span data-ttu-id="aee6b-136">이 url은 논리 앱, 함수 앱 또는 Api 앱의 Arm 리소스 Id 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="aee6b-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="aee6b-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="aee6b-138">Service Fabric 클러스터 백 엔드 정보.</span><span class="sxs-lookup"><span data-stu-id="aee6b-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="aee6b-139">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="aee6b-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="aee6b-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="aee6b-141">백 엔드로 대화 하는 경우 인증서 체인 유효성 검사를 건너뛸지 여부</span><span class="sxs-lookup"><span data-stu-id="aee6b-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="aee6b-142">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="aee6b-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="aee6b-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="aee6b-144">백 엔드로 대화 하는 경우 인증서 이름 유효성 검사를 건너뛸지 여부</span><span class="sxs-lookup"><span data-stu-id="aee6b-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="aee6b-145">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="aee6b-146">-Title</span><span class="sxs-lookup"><span data-stu-id="aee6b-146">-Title</span></span>
<span data-ttu-id="aee6b-147">백 엔드 제목.</span><span class="sxs-lookup"><span data-stu-id="aee6b-147">Backend Title.</span></span>
<span data-ttu-id="aee6b-148">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="aee6b-149">-Url</span><span class="sxs-lookup"><span data-stu-id="aee6b-149">-Url</span></span>
<span data-ttu-id="aee6b-150">백 엔드의 런타임 Url입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="aee6b-151">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-151">This parameter is required.</span></span>

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

### <span data-ttu-id="aee6b-152">-확인</span><span class="sxs-lookup"><span data-stu-id="aee6b-152">-Confirm</span></span>
<span data-ttu-id="aee6b-153">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aee6b-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aee6b-154">-WhatIf</span></span>
<span data-ttu-id="aee6b-155">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aee6b-156">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aee6b-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aee6b-157">CommonParameters</span></span>
<span data-ttu-id="aee6b-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aee6b-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aee6b-159">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aee6b-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aee6b-160">입력</span><span class="sxs-lookup"><span data-stu-id="aee6b-160">INPUTS</span></span>

### <span data-ttu-id="aee6b-161">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aee6b-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aee6b-162">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aee6b-162">System.String</span></span>

### <span data-ttu-id="aee6b-163">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="aee6b-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="aee6b-164">ApiManagement. ServiceManagement. \ PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="aee6b-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="aee6b-165">ApiManagement. ServiceManagement. \ PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="aee6b-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="aee6b-166">ApiManagement. ServiceManagement. \ PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aee6b-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="aee6b-167">출력</span><span class="sxs-lookup"><span data-stu-id="aee6b-167">OUTPUTS</span></span>

### <span data-ttu-id="aee6b-168">ApiManagement. ServiceManagement. \ PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="aee6b-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="aee6b-169">상속자</span><span class="sxs-lookup"><span data-stu-id="aee6b-169">NOTES</span></span>

## <span data-ttu-id="aee6b-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aee6b-170">RELATED LINKS</span></span>

[<span data-ttu-id="aee6b-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="aee6b-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="aee6b-172">새로운 AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="aee6b-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="aee6b-173">새로운 AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="aee6b-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="aee6b-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="aee6b-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="aee6b-175">제거-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="aee6b-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

