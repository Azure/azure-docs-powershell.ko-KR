---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: f5cf0d9f80b15f178cb701b4474fa5dc13d957eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697944"
---
# <span data-ttu-id="0757f-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0757f-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="0757f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0757f-102">SYNOPSIS</span></span>
<span data-ttu-id="0757f-103">백 엔드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-103">Updates a Backend.</span></span>

## <span data-ttu-id="0757f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0757f-104">SYNTAX</span></span>

### <span data-ttu-id="0757f-105">ContextParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0757f-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0757f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0757f-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0757f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0757f-107">DESCRIPTION</span></span>
<span data-ttu-id="0757f-108">Api Management에서 기존 백 엔드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="0757f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0757f-109">EXAMPLES</span></span>

### <span data-ttu-id="0757f-110">백 엔드 123에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="0757f-111">변수</span><span class="sxs-lookup"><span data-stu-id="0757f-111">PARAMETERS</span></span>

### <span data-ttu-id="0757f-112">-BackendId</span><span class="sxs-lookup"><span data-stu-id="0757f-112">-BackendId</span></span>
<span data-ttu-id="0757f-113">새 백 엔드의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-113">Identifier of new backend.</span></span>
<span data-ttu-id="0757f-114">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-114">This parameter is required.</span></span>

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

### <span data-ttu-id="0757f-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="0757f-115">-Context</span></span>
<span data-ttu-id="0757f-116">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0757f-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-117">This parameter is required.</span></span>

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

### <span data-ttu-id="0757f-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="0757f-118">-Credential</span></span>
<span data-ttu-id="0757f-119">백 엔드로 대화할 때 사용 해야 하는 자격 증명 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="0757f-120">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="0757f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0757f-121">-DefaultProfile</span></span>
<span data-ttu-id="0757f-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0757f-123">-설명</span><span class="sxs-lookup"><span data-stu-id="0757f-123">-Description</span></span>
<span data-ttu-id="0757f-124">백 엔드 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-124">Backend Description.</span></span>
<span data-ttu-id="0757f-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="0757f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0757f-126">-InputObject</span></span>
<span data-ttu-id="0757f-127">PsApiManagementBackend의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="0757f-128">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-128">This parameter is required.</span></span>

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

### <span data-ttu-id="0757f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0757f-129">-PassThru</span></span>
<span data-ttu-id="0757f-130">이 cmdlet이이 cmdlet이 수정 하는  **PsApiManagementBackend** 를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0757f-131">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="0757f-131">-Protocol</span></span>
<span data-ttu-id="0757f-132">백 엔드 통신 프로토콜 (http 또는 soap).</span><span class="sxs-lookup"><span data-stu-id="0757f-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="0757f-133">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-133">This parameter is optional</span></span>

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

### <span data-ttu-id="0757f-134">-프록시</span><span class="sxs-lookup"><span data-stu-id="0757f-134">-Proxy</span></span>
<span data-ttu-id="0757f-135">백 엔드에 요청을 보내는 동안 사용할 프록시 서버 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="0757f-136">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="0757f-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0757f-137">-ResourceId</span></span>
<span data-ttu-id="0757f-138">외부 시스템 리소스의 관리 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="0757f-139">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-139">This parameter is optional.</span></span>
<span data-ttu-id="0757f-140">이 url은 논리 앱, 함수 앱 또는 Api 앱의 Arm 리소스 Id 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="0757f-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="0757f-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="0757f-142">Service Fabric 클러스터 백 엔드 정보.</span><span class="sxs-lookup"><span data-stu-id="0757f-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="0757f-143">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="0757f-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="0757f-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="0757f-145">백 엔드로 대화 하는 경우 인증서 체인 유효성 검사를 건너뛸지 여부</span><span class="sxs-lookup"><span data-stu-id="0757f-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="0757f-146">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="0757f-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="0757f-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="0757f-148">백 엔드로 대화 하는 경우 인증서 이름 유효성 검사를 건너뛸지 여부</span><span class="sxs-lookup"><span data-stu-id="0757f-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="0757f-149">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="0757f-150">-Title</span><span class="sxs-lookup"><span data-stu-id="0757f-150">-Title</span></span>
<span data-ttu-id="0757f-151">백 엔드 제목.</span><span class="sxs-lookup"><span data-stu-id="0757f-151">Backend Title.</span></span>
<span data-ttu-id="0757f-152">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="0757f-153">-Url</span><span class="sxs-lookup"><span data-stu-id="0757f-153">-Url</span></span>
<span data-ttu-id="0757f-154">백 엔드의 런타임 Url입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="0757f-155">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="0757f-156">-확인</span><span class="sxs-lookup"><span data-stu-id="0757f-156">-Confirm</span></span>
<span data-ttu-id="0757f-157">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0757f-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0757f-158">-WhatIf</span></span>
<span data-ttu-id="0757f-159">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0757f-160">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0757f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0757f-161">CommonParameters</span></span>
<span data-ttu-id="0757f-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0757f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0757f-163">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0757f-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0757f-164">입력</span><span class="sxs-lookup"><span data-stu-id="0757f-164">INPUTS</span></span>

### <span data-ttu-id="0757f-165">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0757f-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0757f-166">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0757f-166">System.String</span></span>

### <span data-ttu-id="0757f-167">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0757f-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0757f-168">ApiManagement. ServiceManagement. \ PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="0757f-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="0757f-169">ApiManagement. ServiceManagement. \ PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="0757f-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="0757f-170">ApiManagement. ServiceManagement. \ PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0757f-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="0757f-171">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0757f-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0757f-172">출력</span><span class="sxs-lookup"><span data-stu-id="0757f-172">OUTPUTS</span></span>

### <span data-ttu-id="0757f-173">ApiManagement. ServiceManagement. \ PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0757f-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="0757f-174">상속자</span><span class="sxs-lookup"><span data-stu-id="0757f-174">NOTES</span></span>

## <span data-ttu-id="0757f-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0757f-175">RELATED LINKS</span></span>

[<span data-ttu-id="0757f-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0757f-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="0757f-177">새로운 AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0757f-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="0757f-178">새로운 AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="0757f-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="0757f-179">새로운 AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="0757f-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="0757f-180">제거-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0757f-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
