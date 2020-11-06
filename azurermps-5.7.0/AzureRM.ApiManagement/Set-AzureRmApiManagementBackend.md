---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: b5e51891f82b2a12f42fac3a1535f974912ca1dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530583"
---
# <span data-ttu-id="eef2b-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="eef2b-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="eef2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eef2b-102">SYNOPSIS</span></span>
<span data-ttu-id="eef2b-103">백 엔드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eef2b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eef2b-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eef2b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eef2b-105">DESCRIPTION</span></span>
<span data-ttu-id="eef2b-106">Api Management에서 기존 백 엔드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="eef2b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="eef2b-107">EXAMPLES</span></span>

### <span data-ttu-id="eef2b-108">백 엔드 123에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-108">Updates the Description of the Backend 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="eef2b-109">변수</span><span class="sxs-lookup"><span data-stu-id="eef2b-109">PARAMETERS</span></span>

### <span data-ttu-id="eef2b-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="eef2b-110">-BackendId</span></span>
<span data-ttu-id="eef2b-111">새 백 엔드의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-111">Identifier of new backend.</span></span>
<span data-ttu-id="eef2b-112">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-112">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef2b-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="eef2b-113">-Context</span></span>
<span data-ttu-id="eef2b-114">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="eef2b-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-115">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef2b-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="eef2b-116">-Credential</span></span>
<span data-ttu-id="eef2b-117">백 엔드로 대화할 때 사용 해야 하는 자격 증명 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="eef2b-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-118">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef2b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eef2b-119">-DefaultProfile</span></span>
<span data-ttu-id="eef2b-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eef2b-121">-설명</span><span class="sxs-lookup"><span data-stu-id="eef2b-121">-Description</span></span>
<span data-ttu-id="eef2b-122">백 엔드 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-122">Backend Description.</span></span>
<span data-ttu-id="eef2b-123">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-123">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef2b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eef2b-124">-PassThru</span></span>
<span data-ttu-id="eef2b-125">이 cmdlet이이 cmdlet이 수정 하는  **PsApiManagementBackend** 를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eef2b-126">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="eef2b-126">-Protocol</span></span>
<span data-ttu-id="eef2b-127">백 엔드 통신 프로토콜 (http 또는 soap).</span><span class="sxs-lookup"><span data-stu-id="eef2b-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="eef2b-128">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-128">This parameter is optional</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef2b-129">-프록시</span><span class="sxs-lookup"><span data-stu-id="eef2b-129">-Proxy</span></span>
<span data-ttu-id="eef2b-130">백 엔드에 요청을 보내는 동안 사용할 프록시 서버 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="eef2b-131">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-131">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef2b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eef2b-132">-ResourceId</span></span>
<span data-ttu-id="eef2b-133">외부 시스템 리소스의 관리 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="eef2b-134">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-134">This parameter is optional.</span></span>
<span data-ttu-id="eef2b-135">이 url은 논리 앱, 함수 앱 또는 Api 앱의 Arm 리소스 Id 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef2b-136">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="eef2b-136">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="eef2b-137">백 엔드로 대화 하는 경우 인증서 체인 유효성 검사를 건너뛸지 여부</span><span class="sxs-lookup"><span data-stu-id="eef2b-137">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="eef2b-138">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-138">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef2b-139">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="eef2b-139">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="eef2b-140">백 엔드로 대화 하는 경우 인증서 이름 유효성 검사를 건너뛸지 여부</span><span class="sxs-lookup"><span data-stu-id="eef2b-140">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="eef2b-141">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-141">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef2b-142">-Title</span><span class="sxs-lookup"><span data-stu-id="eef2b-142">-Title</span></span>
<span data-ttu-id="eef2b-143">백 엔드 제목.</span><span class="sxs-lookup"><span data-stu-id="eef2b-143">Backend Title.</span></span>
<span data-ttu-id="eef2b-144">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-144">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef2b-145">-Url</span><span class="sxs-lookup"><span data-stu-id="eef2b-145">-Url</span></span>
<span data-ttu-id="eef2b-146">백 엔드의 런타임 Url입니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-146">Runtime Url for the Backend.</span></span>
<span data-ttu-id="eef2b-147">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-147">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef2b-148">-확인</span><span class="sxs-lookup"><span data-stu-id="eef2b-148">-Confirm</span></span>
<span data-ttu-id="eef2b-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eef2b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eef2b-150">-WhatIf</span></span>
<span data-ttu-id="eef2b-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eef2b-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eef2b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eef2b-153">CommonParameters</span></span>
<span data-ttu-id="eef2b-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eef2b-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eef2b-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eef2b-156">입력</span><span class="sxs-lookup"><span data-stu-id="eef2b-156">INPUTS</span></span>

### <span data-ttu-id="eef2b-157">않아야</span><span class="sxs-lookup"><span data-stu-id="eef2b-157">None</span></span>
<span data-ttu-id="eef2b-158">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eef2b-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eef2b-159">출력</span><span class="sxs-lookup"><span data-stu-id="eef2b-159">OUTPUTS</span></span>

### <span data-ttu-id="eef2b-160">ApiManagement. ServiceManagement. \ PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="eef2b-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="eef2b-161">상속자</span><span class="sxs-lookup"><span data-stu-id="eef2b-161">NOTES</span></span>

## <span data-ttu-id="eef2b-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eef2b-162">RELATED LINKS</span></span>

[<span data-ttu-id="eef2b-163">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="eef2b-163">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="eef2b-164">새로운 AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="eef2b-164">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="eef2b-165">새로운 AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="eef2b-165">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="eef2b-166">새로운 AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="eef2b-166">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="eef2b-167">제거-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="eef2b-167">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
