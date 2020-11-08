---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: fe4d94bb438d3180ed0a77bb7129b46c65d5edbc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217879"
---
# <span data-ttu-id="31d06-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="31d06-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="31d06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31d06-102">SYNOPSIS</span></span>
<span data-ttu-id="31d06-103">새 백 엔드 프록시 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31d06-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="31d06-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31d06-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31d06-105">설명은</span><span class="sxs-lookup"><span data-stu-id="31d06-105">DESCRIPTION</span></span>
<span data-ttu-id="31d06-106">새 백엔드 엔터티를 만들 때 파이프 될 수 있는 새 백 엔드 프록시 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31d06-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="31d06-107">예제의</span><span class="sxs-lookup"><span data-stu-id="31d06-107">EXAMPLES</span></span>

### <span data-ttu-id="31d06-108">예제 1: 백 엔드 프록시 In-Memory 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="31d06-108">Example 1: Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="31d06-109">백 엔드 프록시 개체를 만들고 백 엔드를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d06-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="31d06-110">변수</span><span class="sxs-lookup"><span data-stu-id="31d06-110">PARAMETERS</span></span>

### <span data-ttu-id="31d06-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31d06-111">-DefaultProfile</span></span>
<span data-ttu-id="31d06-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31d06-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31d06-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="31d06-113">-ProxyCredential</span></span>
<span data-ttu-id="31d06-114">백엔드 프록시에 연결 하는 데 사용 되는 자격 증명</span><span class="sxs-lookup"><span data-stu-id="31d06-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="31d06-115">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="31d06-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="31d06-116">-Url</span><span class="sxs-lookup"><span data-stu-id="31d06-116">-Url</span></span>
<span data-ttu-id="31d06-117">전화를 백 엔드로 착신 이동할 때 사용할 프록시 서버의 Url입니다.</span><span class="sxs-lookup"><span data-stu-id="31d06-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="31d06-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="31d06-118">This parameter is required.</span></span>

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

### <span data-ttu-id="31d06-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31d06-119">CommonParameters</span></span>
<span data-ttu-id="31d06-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31d06-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31d06-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="31d06-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31d06-122">입력</span><span class="sxs-lookup"><span data-stu-id="31d06-122">INPUTS</span></span>

### <span data-ttu-id="31d06-123">않아야</span><span class="sxs-lookup"><span data-stu-id="31d06-123">None</span></span>

## <span data-ttu-id="31d06-124">출력</span><span class="sxs-lookup"><span data-stu-id="31d06-124">OUTPUTS</span></span>

### <span data-ttu-id="31d06-125">ApiManagement. ServiceManagement. \ PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="31d06-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="31d06-126">상속자</span><span class="sxs-lookup"><span data-stu-id="31d06-126">NOTES</span></span>

## <span data-ttu-id="31d06-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31d06-127">RELATED LINKS</span></span>

[<span data-ttu-id="31d06-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="31d06-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="31d06-129">새로운 AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="31d06-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="31d06-130">새로운 AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="31d06-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="31d06-131">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="31d06-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="31d06-132">제거-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="31d06-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
