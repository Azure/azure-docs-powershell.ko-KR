---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: fe4d94bb438d3180ed0a77bb7129b46c65d5edbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205685"
---
# <span data-ttu-id="0625a-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="0625a-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="0625a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0625a-102">SYNOPSIS</span></span>
<span data-ttu-id="0625a-103">새 백end 프록시 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0625a-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="0625a-104">구문</span><span class="sxs-lookup"><span data-stu-id="0625a-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0625a-105">설명</span><span class="sxs-lookup"><span data-stu-id="0625a-105">DESCRIPTION</span></span>
<span data-ttu-id="0625a-106">새 백end 엔터티를 만들 때 파이프할 수 있는 새 백 엔드 프록시 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0625a-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="0625a-107">예제</span><span class="sxs-lookup"><span data-stu-id="0625a-107">EXAMPLES</span></span>

### <span data-ttu-id="0625a-108">예제 1: 개체에 백 In-Memory 만들기</span><span class="sxs-lookup"><span data-stu-id="0625a-108">Example 1: Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="0625a-109">백end 프록시 개체를 만들고 백end를 설정</span><span class="sxs-lookup"><span data-stu-id="0625a-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="0625a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0625a-110">PARAMETERS</span></span>

### <span data-ttu-id="0625a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0625a-111">-DefaultProfile</span></span>
<span data-ttu-id="0625a-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0625a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0625a-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="0625a-113">-ProxyCredential</span></span>
<span data-ttu-id="0625a-114">백end 프록시에 연결하는 데 사용되는 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="0625a-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="0625a-115">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="0625a-115">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0625a-116">-Url</span><span class="sxs-lookup"><span data-stu-id="0625a-116">-Url</span></span>
<span data-ttu-id="0625a-117">백end에 호출을 전달할 때 사용할 프록시 서버의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="0625a-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="0625a-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="0625a-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0625a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0625a-119">CommonParameters</span></span>
<span data-ttu-id="0625a-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0625a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0625a-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0625a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0625a-122">입력</span><span class="sxs-lookup"><span data-stu-id="0625a-122">INPUTS</span></span>

### <span data-ttu-id="0625a-123">없음</span><span class="sxs-lookup"><span data-stu-id="0625a-123">None</span></span>

## <span data-ttu-id="0625a-124">출력</span><span class="sxs-lookup"><span data-stu-id="0625a-124">OUTPUTS</span></span>

### <span data-ttu-id="0625a-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="0625a-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="0625a-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0625a-126">NOTES</span></span>

## <span data-ttu-id="0625a-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0625a-127">RELATED LINKS</span></span>

[<span data-ttu-id="0625a-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0625a-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="0625a-129">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0625a-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="0625a-130">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="0625a-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="0625a-131">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0625a-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="0625a-132">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0625a-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
