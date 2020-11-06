---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 11d832bc74aca4ac274ee17ff0b38de06b77e377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528697"
---
# <span data-ttu-id="6030e-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6030e-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="6030e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6030e-102">SYNOPSIS</span></span>
<span data-ttu-id="6030e-103">백 엔드의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6030e-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6030e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6030e-104">SYNTAX</span></span>

### <span data-ttu-id="6030e-105">GetAllBackends (기본값)</span><span class="sxs-lookup"><span data-stu-id="6030e-105">GetAllBackends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6030e-106">GetByBackendId</span><span class="sxs-lookup"><span data-stu-id="6030e-106">GetByBackendId</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6030e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6030e-107">DESCRIPTION</span></span>
<span data-ttu-id="6030e-108">백 엔드의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6030e-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="6030e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6030e-109">EXAMPLES</span></span>

### <span data-ttu-id="6030e-110">예제 1: 모든 백 엔드 가져오기</span><span class="sxs-lookup"><span data-stu-id="6030e-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="6030e-111">Api Management 서비스에 구성 된 모든 Backends의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6030e-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="6030e-112">예제 2: 식별자 123으로 지정 된 백 엔드 가져오기</span><span class="sxs-lookup"><span data-stu-id="6030e-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="6030e-113">식별자 ' 123 ' (으)로 식별 되는 지정 된 백엔드의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6030e-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="6030e-114">변수</span><span class="sxs-lookup"><span data-stu-id="6030e-114">PARAMETERS</span></span>

### <span data-ttu-id="6030e-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="6030e-115">-BackendId</span></span>
<span data-ttu-id="6030e-116">백 엔드의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6030e-116">Identifier of a backend.</span></span>
<span data-ttu-id="6030e-117">지정 된 경우 식별자를 사용 하 여 백 엔드를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="6030e-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="6030e-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="6030e-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByBackendId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6030e-119">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="6030e-119">-Context</span></span>
<span data-ttu-id="6030e-120">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="6030e-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6030e-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="6030e-121">This parameter is required.</span></span>

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

### <span data-ttu-id="6030e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6030e-122">-DefaultProfile</span></span>
<span data-ttu-id="6030e-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6030e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6030e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6030e-124">CommonParameters</span></span>
<span data-ttu-id="6030e-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6030e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6030e-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6030e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6030e-127">입력</span><span class="sxs-lookup"><span data-stu-id="6030e-127">INPUTS</span></span>

### <span data-ttu-id="6030e-128">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6030e-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6030e-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6030e-129">System.String</span></span>

## <span data-ttu-id="6030e-130">출력</span><span class="sxs-lookup"><span data-stu-id="6030e-130">OUTPUTS</span></span>

### <span data-ttu-id="6030e-131">ApiManagement. ServiceManagement. \ PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6030e-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="6030e-132">상속자</span><span class="sxs-lookup"><span data-stu-id="6030e-132">NOTES</span></span>

## <span data-ttu-id="6030e-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6030e-133">RELATED LINKS</span></span>

[<span data-ttu-id="6030e-134">새로운 AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6030e-134">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="6030e-135">새로운 AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="6030e-135">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="6030e-136">새로운 AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="6030e-136">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="6030e-137">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6030e-137">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="6030e-138">제거-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6030e-138">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
