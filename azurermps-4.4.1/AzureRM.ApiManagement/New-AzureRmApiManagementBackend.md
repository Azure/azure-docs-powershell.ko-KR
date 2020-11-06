---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: 144830c2155379683c8568eda6e0d1bc021b38fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531279"
---
# <span data-ttu-id="942cf-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="942cf-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="942cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="942cf-102">SYNOPSIS</span></span>
<span data-ttu-id="942cf-103">새 백엔드 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="942cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="942cf-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="942cf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="942cf-105">DESCRIPTION</span></span>
<span data-ttu-id="942cf-106">Api Management에 새 백엔드 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="942cf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="942cf-107">EXAMPLES</span></span>

### <span data-ttu-id="942cf-108">기본 권한 부여 스키마를 사용 하 여 백엔드 123 만들기</span><span class="sxs-lookup"><span data-stu-id="942cf-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```
$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="942cf-109">새 백 엔드 만들기</span><span class="sxs-lookup"><span data-stu-id="942cf-109">Creates a new Backend</span></span>

## <span data-ttu-id="942cf-110">변수</span><span class="sxs-lookup"><span data-stu-id="942cf-110">PARAMETERS</span></span>

### <span data-ttu-id="942cf-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="942cf-111">-BackendId</span></span>
<span data-ttu-id="942cf-112">새 백 엔드의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-112">Identifier of new backend.</span></span>
<span data-ttu-id="942cf-113">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-113">This parameter is optional.</span></span>
<span data-ttu-id="942cf-114">지정 하지 않으면가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="942cf-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="942cf-115">-Context</span></span>
<span data-ttu-id="942cf-116">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="942cf-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-117">This parameter is required.</span></span>

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

### <span data-ttu-id="942cf-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="942cf-118">-Credential</span></span>
<span data-ttu-id="942cf-119">백 엔드로 대화할 때 사용 해야 하는 자격 증명 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="942cf-120">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="942cf-121">-설명</span><span class="sxs-lookup"><span data-stu-id="942cf-121">-Description</span></span>
<span data-ttu-id="942cf-122">백 엔드 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-122">Backend Description.</span></span>
<span data-ttu-id="942cf-123">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="942cf-124">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="942cf-124">-Protocol</span></span>
<span data-ttu-id="942cf-125">백 엔드 통신 프로토콜.</span><span class="sxs-lookup"><span data-stu-id="942cf-125">Backend Communication protocol.</span></span>
<span data-ttu-id="942cf-126">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-126">This parameter is required.</span></span>
<span data-ttu-id="942cf-127">유효한 값은 ' http ' 및 ' soap '입니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-127">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="942cf-128">-프록시</span><span class="sxs-lookup"><span data-stu-id="942cf-128">-Proxy</span></span>
<span data-ttu-id="942cf-129">백 엔드에 요청을 보내는 동안 사용할 프록시 서버 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-129">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="942cf-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="942cf-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="942cf-131">-ResourceId</span></span>
<span data-ttu-id="942cf-132">외부 시스템 리소스의 관리 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-132">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="942cf-133">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-133">This parameter is optional.</span></span>
<span data-ttu-id="942cf-134">이 url은 논리 앱, 함수 앱 또는 Api 앱의 Arm 리소스 Id 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-134">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="942cf-135">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="942cf-135">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="942cf-136">백 엔드로 대화 하는 경우 인증서 체인 유효성 검사를 건너뛸지 여부</span><span class="sxs-lookup"><span data-stu-id="942cf-136">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="942cf-137">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="942cf-138">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="942cf-138">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="942cf-139">백 엔드로 대화 하는 경우 인증서 이름 유효성 검사를 건너뛸지 여부</span><span class="sxs-lookup"><span data-stu-id="942cf-139">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="942cf-140">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="942cf-141">-Title</span><span class="sxs-lookup"><span data-stu-id="942cf-141">-Title</span></span>
<span data-ttu-id="942cf-142">백 엔드 제목.</span><span class="sxs-lookup"><span data-stu-id="942cf-142">Backend Title.</span></span>
<span data-ttu-id="942cf-143">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="942cf-144">-Url</span><span class="sxs-lookup"><span data-stu-id="942cf-144">-Url</span></span>
<span data-ttu-id="942cf-145">백 엔드의 런타임 Url입니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-145">Runtime Url for the Backend.</span></span>
<span data-ttu-id="942cf-146">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-146">This parameter is required.</span></span>

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

### <span data-ttu-id="942cf-147">-확인</span><span class="sxs-lookup"><span data-stu-id="942cf-147">-Confirm</span></span>
<span data-ttu-id="942cf-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="942cf-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="942cf-149">-WhatIf</span></span>
<span data-ttu-id="942cf-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="942cf-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="942cf-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="942cf-152">-DefaultProfile</span></span>
<span data-ttu-id="942cf-153">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="942cf-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="942cf-154">CommonParameters</span></span>
<span data-ttu-id="942cf-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="942cf-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="942cf-156">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="942cf-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="942cf-157">입력</span><span class="sxs-lookup"><span data-stu-id="942cf-157">INPUTS</span></span>

## <span data-ttu-id="942cf-158">출력</span><span class="sxs-lookup"><span data-stu-id="942cf-158">OUTPUTS</span></span>

### <span data-ttu-id="942cf-159">ApiManagement. ServiceManagement. \ PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="942cf-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="942cf-160">상속자</span><span class="sxs-lookup"><span data-stu-id="942cf-160">NOTES</span></span>

## <span data-ttu-id="942cf-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="942cf-161">RELATED LINKS</span></span>

[<span data-ttu-id="942cf-162">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="942cf-162">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="942cf-163">새로운 AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="942cf-163">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="942cf-164">새로운 AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="942cf-164">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="942cf-165">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="942cf-165">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="942cf-166">제거-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="942cf-166">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

