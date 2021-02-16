---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 069bf57b62d6834a1509adb551d15ce5082b2dc3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205693"
---
# <span data-ttu-id="ad97c-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="ad97c-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="ad97c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad97c-102">SYNOPSIS</span></span>
<span data-ttu-id="ad97c-103">새 백end 자격 증명 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad97c-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="ad97c-104">구문</span><span class="sxs-lookup"><span data-stu-id="ad97c-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad97c-105">설명</span><span class="sxs-lookup"><span data-stu-id="ad97c-105">DESCRIPTION</span></span>
<span data-ttu-id="ad97c-106">새 백end 자격 증명 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad97c-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="ad97c-107">예제</span><span class="sxs-lookup"><span data-stu-id="ad97c-107">EXAMPLES</span></span>

### <span data-ttu-id="ad97c-108">예제 1: 개체에 대한 백 In-Memory 만들기</span><span class="sxs-lookup"><span data-stu-id="ad97c-108">Example 1: Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="ad97c-109">백end 자격 증명 계약을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad97c-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="ad97c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad97c-110">PARAMETERS</span></span>

### <span data-ttu-id="ad97c-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="ad97c-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="ad97c-112">백end에 사용되는 권한 부여 헤더입니다.</span><span class="sxs-lookup"><span data-stu-id="ad97c-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="ad97c-113">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ad97c-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="ad97c-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="ad97c-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="ad97c-115">백end에 사용되는 권한 부여 체계입니다.</span><span class="sxs-lookup"><span data-stu-id="ad97c-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="ad97c-116">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ad97c-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="ad97c-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ad97c-117">-CertificateThumbprint</span></span>
<span data-ttu-id="ad97c-118">클라이언트 인증서 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="ad97c-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="ad97c-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ad97c-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="ad97c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad97c-120">-DefaultProfile</span></span>
<span data-ttu-id="ad97c-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad97c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad97c-122">-Header</span><span class="sxs-lookup"><span data-stu-id="ad97c-122">-Header</span></span>
<span data-ttu-id="ad97c-123">백end에서 허용하는 헤더 매개 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ad97c-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="ad97c-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ad97c-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="ad97c-125">-Query</span><span class="sxs-lookup"><span data-stu-id="ad97c-125">-Query</span></span>
<span data-ttu-id="ad97c-126">백end에서 허용하는 쿼리 매개 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ad97c-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="ad97c-127">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ad97c-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="ad97c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad97c-128">CommonParameters</span></span>
<span data-ttu-id="ad97c-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ad97c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad97c-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ad97c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad97c-131">입력</span><span class="sxs-lookup"><span data-stu-id="ad97c-131">INPUTS</span></span>

### <span data-ttu-id="ad97c-132">없음</span><span class="sxs-lookup"><span data-stu-id="ad97c-132">None</span></span>

## <span data-ttu-id="ad97c-133">출력</span><span class="sxs-lookup"><span data-stu-id="ad97c-133">OUTPUTS</span></span>

### <span data-ttu-id="ad97c-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="ad97c-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="ad97c-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ad97c-135">NOTES</span></span>

## <span data-ttu-id="ad97c-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad97c-136">RELATED LINKS</span></span>

[<span data-ttu-id="ad97c-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ad97c-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="ad97c-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ad97c-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="ad97c-139">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ad97c-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="ad97c-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ad97c-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="ad97c-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ad97c-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
