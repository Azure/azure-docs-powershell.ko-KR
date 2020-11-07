---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: ce27a151ebb6d778ed647fb81909c44c11edbf8e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869354"
---
# <span data-ttu-id="1fbf8-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1fbf8-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="1fbf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fbf8-102">SYNOPSIS</span></span>
<span data-ttu-id="1fbf8-103">백 엔드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-103">Updates a Backend.</span></span>

## <span data-ttu-id="1fbf8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1fbf8-104">SYNTAX</span></span>

```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fbf8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1fbf8-105">DESCRIPTION</span></span>
<span data-ttu-id="1fbf8-106">Api Management에서 기존 백 엔드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="1fbf8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1fbf8-107">EXAMPLES</span></span>

### <span data-ttu-id="1fbf8-108">백 엔드 123에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="1fbf8-109">변수</span><span class="sxs-lookup"><span data-stu-id="1fbf8-109">PARAMETERS</span></span>

### <span data-ttu-id="1fbf8-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="1fbf8-110">-BackendId</span></span>
<span data-ttu-id="1fbf8-111">새 백 엔드의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-111">Identifier of new backend.</span></span>
<span data-ttu-id="1fbf8-112">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-112">This parameter is required.</span></span>

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

### <span data-ttu-id="1fbf8-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="1fbf8-113">-Context</span></span>
<span data-ttu-id="1fbf8-114">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1fbf8-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-115">This parameter is required.</span></span>

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

### <span data-ttu-id="1fbf8-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="1fbf8-116">-Credential</span></span>
<span data-ttu-id="1fbf8-117">백 엔드로 대화할 때 사용 해야 하는 자격 증명 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="1fbf8-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="1fbf8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fbf8-119">-DefaultProfile</span></span>
<span data-ttu-id="1fbf8-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fbf8-121">-설명</span><span class="sxs-lookup"><span data-stu-id="1fbf8-121">-Description</span></span>
<span data-ttu-id="1fbf8-122">백 엔드 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-122">Backend Description.</span></span>
<span data-ttu-id="1fbf8-123">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="1fbf8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fbf8-124">-PassThru</span></span>
<span data-ttu-id="1fbf8-125">이 cmdlet이이 cmdlet이 수정 하는  **PsApiManagementBackend** 를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1fbf8-126">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="1fbf8-126">-Protocol</span></span>
<span data-ttu-id="1fbf8-127">백 엔드 통신 프로토콜 (http 또는 soap).</span><span class="sxs-lookup"><span data-stu-id="1fbf8-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="1fbf8-128">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-128">This parameter is optional</span></span>

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

### <span data-ttu-id="1fbf8-129">-프록시</span><span class="sxs-lookup"><span data-stu-id="1fbf8-129">-Proxy</span></span>
<span data-ttu-id="1fbf8-130">백 엔드에 요청을 보내는 동안 사용할 프록시 서버 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="1fbf8-131">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="1fbf8-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fbf8-132">-ResourceId</span></span>
<span data-ttu-id="1fbf8-133">외부 시스템 리소스의 관리 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="1fbf8-134">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-134">This parameter is optional.</span></span>
<span data-ttu-id="1fbf8-135">이 url은 논리 앱, 함수 앱 또는 Api 앱의 Arm 리소스 Id 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="1fbf8-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="1fbf8-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="1fbf8-137">Service Fabric 클러스터 백 엔드 정보.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="1fbf8-138">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="1fbf8-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="1fbf8-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="1fbf8-140">백 엔드로 대화 하는 경우 인증서 체인 유효성 검사를 건너뛸지 여부</span><span class="sxs-lookup"><span data-stu-id="1fbf8-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="1fbf8-141">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="1fbf8-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="1fbf8-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="1fbf8-143">백 엔드로 대화 하는 경우 인증서 이름 유효성 검사를 건너뛸지 여부</span><span class="sxs-lookup"><span data-stu-id="1fbf8-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="1fbf8-144">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="1fbf8-145">-Title</span><span class="sxs-lookup"><span data-stu-id="1fbf8-145">-Title</span></span>
<span data-ttu-id="1fbf8-146">백 엔드 제목.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-146">Backend Title.</span></span>
<span data-ttu-id="1fbf8-147">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="1fbf8-148">-Url</span><span class="sxs-lookup"><span data-stu-id="1fbf8-148">-Url</span></span>
<span data-ttu-id="1fbf8-149">백 엔드의 런타임 Url입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="1fbf8-150">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="1fbf8-151">-확인</span><span class="sxs-lookup"><span data-stu-id="1fbf8-151">-Confirm</span></span>
<span data-ttu-id="1fbf8-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fbf8-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fbf8-153">-WhatIf</span></span>
<span data-ttu-id="1fbf8-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1fbf8-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fbf8-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fbf8-156">CommonParameters</span></span>
<span data-ttu-id="1fbf8-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fbf8-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fbf8-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fbf8-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fbf8-159">입력</span><span class="sxs-lookup"><span data-stu-id="1fbf8-159">INPUTS</span></span>

### <span data-ttu-id="1fbf8-160">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1fbf8-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1fbf8-161">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1fbf8-161">System.String</span></span>

### <span data-ttu-id="1fbf8-162">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1fbf8-162">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1fbf8-163">ApiManagement. ServiceManagement. \ PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="1fbf8-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="1fbf8-164">ApiManagement. ServiceManagement. \ PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="1fbf8-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="1fbf8-165">ApiManagement. ServiceManagement. \ PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1fbf8-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="1fbf8-166">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1fbf8-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1fbf8-167">출력</span><span class="sxs-lookup"><span data-stu-id="1fbf8-167">OUTPUTS</span></span>

### <span data-ttu-id="1fbf8-168">ApiManagement. ServiceManagement. \ PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1fbf8-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="1fbf8-169">상속자</span><span class="sxs-lookup"><span data-stu-id="1fbf8-169">NOTES</span></span>

## <span data-ttu-id="1fbf8-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1fbf8-170">RELATED LINKS</span></span>

[<span data-ttu-id="1fbf8-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1fbf8-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="1fbf8-172">새로운 AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1fbf8-172">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="1fbf8-173">새로운 AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="1fbf8-173">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="1fbf8-174">새로운 AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="1fbf8-174">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="1fbf8-175">제거-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1fbf8-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
