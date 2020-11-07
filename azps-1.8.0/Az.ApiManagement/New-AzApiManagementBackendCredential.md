---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 246b465c64242913fb0d05981b0f221605c6a0d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689105"
---
# <span data-ttu-id="b25de-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b25de-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="b25de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b25de-102">SYNOPSIS</span></span>
<span data-ttu-id="b25de-103">새 백엔드 자격 증명 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b25de-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="b25de-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b25de-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b25de-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b25de-105">DESCRIPTION</span></span>
<span data-ttu-id="b25de-106">새 백엔드 자격 증명 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b25de-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="b25de-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b25de-107">EXAMPLES</span></span>

### <span data-ttu-id="b25de-108">백 엔드 자격 증명 In-Memory 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="b25de-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="b25de-109">백 엔드 자격 증명 계약 만들기</span><span class="sxs-lookup"><span data-stu-id="b25de-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="b25de-110">변수</span><span class="sxs-lookup"><span data-stu-id="b25de-110">PARAMETERS</span></span>

### <span data-ttu-id="b25de-111">-AuthorizationHeaderParameter 변수</span><span class="sxs-lookup"><span data-stu-id="b25de-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="b25de-112">백 엔드에 사용 되는 권한 부여 헤더입니다.</span><span class="sxs-lookup"><span data-stu-id="b25de-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="b25de-113">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="b25de-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25de-114">-Authorization헤더 구성표</span><span class="sxs-lookup"><span data-stu-id="b25de-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="b25de-115">백 엔드에 사용 되는 권한 부여 체계입니다.</span><span class="sxs-lookup"><span data-stu-id="b25de-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="b25de-116">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="b25de-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25de-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="b25de-117">-CertificateThumbprint</span></span>
<span data-ttu-id="b25de-118">클라이언트 인증서 지문.</span><span class="sxs-lookup"><span data-stu-id="b25de-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="b25de-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="b25de-119">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25de-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b25de-120">-DefaultProfile</span></span>
<span data-ttu-id="b25de-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b25de-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b25de-122">-헤더</span><span class="sxs-lookup"><span data-stu-id="b25de-122">-Header</span></span>
<span data-ttu-id="b25de-123">백 엔드가 허용 하는 헤더 매개 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b25de-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="b25de-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="b25de-124">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25de-125">-쿼리</span><span class="sxs-lookup"><span data-stu-id="b25de-125">-Query</span></span>
<span data-ttu-id="b25de-126">백 엔드에 의해 허용 된 쿼리 매개 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b25de-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="b25de-127">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="b25de-127">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25de-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b25de-128">CommonParameters</span></span>
<span data-ttu-id="b25de-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b25de-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b25de-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b25de-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b25de-131">입력</span><span class="sxs-lookup"><span data-stu-id="b25de-131">INPUTS</span></span>

### <span data-ttu-id="b25de-132">않아야</span><span class="sxs-lookup"><span data-stu-id="b25de-132">None</span></span>

## <span data-ttu-id="b25de-133">출력</span><span class="sxs-lookup"><span data-stu-id="b25de-133">OUTPUTS</span></span>

### <span data-ttu-id="b25de-134">ApiManagement. ServiceManagement. \ PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b25de-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="b25de-135">상속자</span><span class="sxs-lookup"><span data-stu-id="b25de-135">NOTES</span></span>

## <span data-ttu-id="b25de-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b25de-136">RELATED LINKS</span></span>

[<span data-ttu-id="b25de-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b25de-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="b25de-138">새로운 AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b25de-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="b25de-139">새로운 AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b25de-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="b25de-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b25de-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="b25de-141">제거-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b25de-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
