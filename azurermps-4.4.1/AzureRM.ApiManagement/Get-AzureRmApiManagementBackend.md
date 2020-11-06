---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 4f54b361482bad24826d7120e53f96ce8d3b9eef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531884"
---
# <span data-ttu-id="7bc6a-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7bc6a-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="7bc6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bc6a-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc6a-103">백 엔드의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bc6a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7bc6a-104">SYNTAX</span></span>

### <span data-ttu-id="7bc6a-105">모든 백 엔드 가져오기 (기본값)</span><span class="sxs-lookup"><span data-stu-id="7bc6a-105">Get all backends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7bc6a-106">백엔드 ID로 가져오기</span><span class="sxs-lookup"><span data-stu-id="7bc6a-106">Get by backend ID</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bc6a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7bc6a-107">DESCRIPTION</span></span>
<span data-ttu-id="7bc6a-108">백 엔드의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="7bc6a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7bc6a-109">EXAMPLES</span></span>

### <span data-ttu-id="7bc6a-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7bc6a-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="7bc6a-111">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="7bc6a-111">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="7bc6a-112">Api Management 서비스에 구성 된 모든 Backends의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-112">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="7bc6a-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="7bc6a-113">--------------------------  Example 2  --------------------------</span></span>
<span data-ttu-id="7bc6a-114">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="7bc6a-114">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="7bc6a-115">식별자 ' 123 ' (으)로 식별 되는 지정 된 백엔드의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-115">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="7bc6a-116">변수</span><span class="sxs-lookup"><span data-stu-id="7bc6a-116">PARAMETERS</span></span>

### <span data-ttu-id="7bc6a-117">-BackendId</span><span class="sxs-lookup"><span data-stu-id="7bc6a-117">-BackendId</span></span>
<span data-ttu-id="7bc6a-118">백 엔드의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-118">Identifier of a backend.</span></span>
<span data-ttu-id="7bc6a-119">지정 된 경우 식별자를 사용 하 여 백 엔드를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-119">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="7bc6a-120">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-120">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by backend ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc6a-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="7bc6a-121">-Context</span></span>
<span data-ttu-id="7bc6a-122">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7bc6a-123">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-123">This parameter is required.</span></span>

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

### <span data-ttu-id="7bc6a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bc6a-124">-DefaultProfile</span></span>
<span data-ttu-id="7bc6a-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bc6a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc6a-126">CommonParameters</span></span>
<span data-ttu-id="7bc6a-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc6a-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bc6a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc6a-129">입력</span><span class="sxs-lookup"><span data-stu-id="7bc6a-129">INPUTS</span></span>

## <span data-ttu-id="7bc6a-130">출력</span><span class="sxs-lookup"><span data-stu-id="7bc6a-130">OUTPUTS</span></span>

### <span data-ttu-id="7bc6a-131">IList를<ApiManagement> ServiceManagement. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7bc6a-131">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend></span></span>

### <span data-ttu-id="7bc6a-132">ApiManagement. ServiceManagement. PsApiManagementLogger. PsApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="7bc6a-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger.PsApiManagementBackend</span></span>

## <span data-ttu-id="7bc6a-133">상속자</span><span class="sxs-lookup"><span data-stu-id="7bc6a-133">NOTES</span></span>

## <span data-ttu-id="7bc6a-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7bc6a-134">RELATED LINKS</span></span>

[<span data-ttu-id="7bc6a-135">새로운 AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7bc6a-135">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="7bc6a-136">새로운 AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="7bc6a-136">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="7bc6a-137">새로운 AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="7bc6a-137">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="7bc6a-138">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7bc6a-138">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="7bc6a-139">제거-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7bc6a-139">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
