---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: 890f169c3fd497f7045522133e1e9e1f1d509aca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536867"
---
# <span data-ttu-id="1eefa-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="1eefa-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="1eefa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1eefa-102">SYNOPSIS</span></span>
<span data-ttu-id="1eefa-103">새 백 엔드 프록시 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1eefa-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1eefa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1eefa-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1eefa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1eefa-105">DESCRIPTION</span></span>
<span data-ttu-id="1eefa-106">새 백엔드 엔터티를 만들 때 파이프 될 수 있는 새 백 엔드 프록시 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1eefa-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="1eefa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1eefa-107">EXAMPLES</span></span>

### <span data-ttu-id="1eefa-108">백 엔드 프록시 In-Memory 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="1eefa-108">Create a Backend Proxy In-Memory Object</span></span>
```
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzureRmApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds
```

<span data-ttu-id="1eefa-109">백 엔드 프록시 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1eefa-109">Creates a Backend Proxy Object</span></span>

## <span data-ttu-id="1eefa-110">변수</span><span class="sxs-lookup"><span data-stu-id="1eefa-110">PARAMETERS</span></span>

### <span data-ttu-id="1eefa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eefa-111">-DefaultProfile</span></span>
<span data-ttu-id="1eefa-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1eefa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="1eefa-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="1eefa-113">-ProxyCredential</span></span>
<span data-ttu-id="1eefa-114">백엔드 프록시에 연결 하는 데 사용 되는 자격 증명</span><span class="sxs-lookup"><span data-stu-id="1eefa-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="1eefa-115">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1eefa-115">This parameter is optional.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eefa-116">-Url</span><span class="sxs-lookup"><span data-stu-id="1eefa-116">-Url</span></span>
<span data-ttu-id="1eefa-117">전화를 백 엔드로 착신 이동할 때 사용할 프록시 서버의 Url입니다.</span><span class="sxs-lookup"><span data-stu-id="1eefa-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="1eefa-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="1eefa-118">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eefa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eefa-119">CommonParameters</span></span>
<span data-ttu-id="1eefa-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1eefa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eefa-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1eefa-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eefa-122">입력</span><span class="sxs-lookup"><span data-stu-id="1eefa-122">INPUTS</span></span>

### <span data-ttu-id="1eefa-123">않아야</span><span class="sxs-lookup"><span data-stu-id="1eefa-123">None</span></span>
<span data-ttu-id="1eefa-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1eefa-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1eefa-125">출력</span><span class="sxs-lookup"><span data-stu-id="1eefa-125">OUTPUTS</span></span>

### <span data-ttu-id="1eefa-126">ApiManagement. ServiceManagement. \ PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="1eefa-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="1eefa-127">상속자</span><span class="sxs-lookup"><span data-stu-id="1eefa-127">NOTES</span></span>

## <span data-ttu-id="1eefa-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1eefa-128">RELATED LINKS</span></span>

[<span data-ttu-id="1eefa-129">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1eefa-129">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="1eefa-130">새로운 AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1eefa-130">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="1eefa-131">새로운 AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="1eefa-131">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="1eefa-132">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1eefa-132">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="1eefa-133">제거-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1eefa-133">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
