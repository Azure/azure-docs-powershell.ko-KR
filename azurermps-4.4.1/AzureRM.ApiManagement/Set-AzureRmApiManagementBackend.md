---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: 85545777f5a76f3f75e81648a009ffcdcad8ab30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710997"
---
# <span data-ttu-id="efc0a-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="efc0a-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="efc0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efc0a-102">SYNOPSIS</span></span>
<span data-ttu-id="efc0a-103">백 엔드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efc0a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="efc0a-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efc0a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="efc0a-105">DESCRIPTION</span></span>
<span data-ttu-id="efc0a-106">Api Management에서 기존 백 엔드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="efc0a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="efc0a-107">EXAMPLES</span></span>

### <span data-ttu-id="efc0a-108">백 엔드 123에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-108">Updates the Description of the Backend 123</span></span>
```
Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="efc0a-109">변수</span><span class="sxs-lookup"><span data-stu-id="efc0a-109">PARAMETERS</span></span>

### <span data-ttu-id="efc0a-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="efc0a-110">-BackendId</span></span>
<span data-ttu-id="efc0a-111">새 백 엔드의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-111">Identifier of new backend.</span></span>
<span data-ttu-id="efc0a-112">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-112">This parameter is required.</span></span>

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

### <span data-ttu-id="efc0a-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="efc0a-113">-Context</span></span>
<span data-ttu-id="efc0a-114">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="efc0a-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-115">This parameter is required.</span></span>

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

### <span data-ttu-id="efc0a-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="efc0a-116">-Credential</span></span>
<span data-ttu-id="efc0a-117">백 엔드로 대화할 때 사용 해야 하는 자격 증명 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="efc0a-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="efc0a-119">-설명</span><span class="sxs-lookup"><span data-stu-id="efc0a-119">-Description</span></span>
<span data-ttu-id="efc0a-120">백 엔드 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-120">Backend Description.</span></span>
<span data-ttu-id="efc0a-121">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="efc0a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efc0a-122">-PassThru</span></span>
<span data-ttu-id="efc0a-123">이 cmdlet이이 cmdlet이 수정 하는  **PsApiManagementBackend** 를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-123">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc0a-124">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="efc0a-124">-Protocol</span></span>
<span data-ttu-id="efc0a-125">백 엔드 통신 프로토콜 (http 또는 soap).</span><span class="sxs-lookup"><span data-stu-id="efc0a-125">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="efc0a-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-126">This parameter is optional</span></span>

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

### <span data-ttu-id="efc0a-127">-프록시</span><span class="sxs-lookup"><span data-stu-id="efc0a-127">-Proxy</span></span>
<span data-ttu-id="efc0a-128">백 엔드에 요청을 보내는 동안 사용할 프록시 서버 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-128">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="efc0a-129">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="efc0a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efc0a-130">-ResourceId</span></span>
<span data-ttu-id="efc0a-131">외부 시스템 리소스의 관리 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-131">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="efc0a-132">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-132">This parameter is optional.</span></span>
<span data-ttu-id="efc0a-133">이 url은 논리 앱, 함수 앱 또는 Api 앱의 Arm 리소스 Id 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-133">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="efc0a-134">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="efc0a-134">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="efc0a-135">백 엔드로 대화 하는 경우 인증서 체인 유효성 검사를 건너뛸지 여부</span><span class="sxs-lookup"><span data-stu-id="efc0a-135">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="efc0a-136">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="efc0a-137">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="efc0a-137">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="efc0a-138">백 엔드로 대화 하는 경우 인증서 이름 유효성 검사를 건너뛸지 여부</span><span class="sxs-lookup"><span data-stu-id="efc0a-138">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="efc0a-139">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="efc0a-140">-Title</span><span class="sxs-lookup"><span data-stu-id="efc0a-140">-Title</span></span>
<span data-ttu-id="efc0a-141">백 엔드 제목.</span><span class="sxs-lookup"><span data-stu-id="efc0a-141">Backend Title.</span></span>
<span data-ttu-id="efc0a-142">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="efc0a-143">-Url</span><span class="sxs-lookup"><span data-stu-id="efc0a-143">-Url</span></span>
<span data-ttu-id="efc0a-144">백 엔드의 런타임 Url입니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-144">Runtime Url for the Backend.</span></span>
<span data-ttu-id="efc0a-145">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="efc0a-146">-확인</span><span class="sxs-lookup"><span data-stu-id="efc0a-146">-Confirm</span></span>
<span data-ttu-id="efc0a-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efc0a-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efc0a-148">-WhatIf</span></span>
<span data-ttu-id="efc0a-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efc0a-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efc0a-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc0a-151">-DefaultProfile</span></span>
<span data-ttu-id="efc0a-152">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efc0a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc0a-153">CommonParameters</span></span>
<span data-ttu-id="efc0a-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="efc0a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc0a-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efc0a-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc0a-156">입력</span><span class="sxs-lookup"><span data-stu-id="efc0a-156">INPUTS</span></span>

## <span data-ttu-id="efc0a-157">출력</span><span class="sxs-lookup"><span data-stu-id="efc0a-157">OUTPUTS</span></span>

### <span data-ttu-id="efc0a-158">ApiManagement. ServiceManagement. \ PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="efc0a-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="efc0a-159">상속자</span><span class="sxs-lookup"><span data-stu-id="efc0a-159">NOTES</span></span>

## <span data-ttu-id="efc0a-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efc0a-160">RELATED LINKS</span></span>

[<span data-ttu-id="efc0a-161">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="efc0a-161">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="efc0a-162">새로운 AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="efc0a-162">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="efc0a-163">새로운 AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="efc0a-163">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="efc0a-164">새로운 AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="efc0a-164">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="efc0a-165">제거-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="efc0a-165">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
