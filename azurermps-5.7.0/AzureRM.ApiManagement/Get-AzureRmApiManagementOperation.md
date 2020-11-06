---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: 1b1547485a4758764cf02eaca4fd7bc26d4ef990
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533808"
---
# <span data-ttu-id="40309-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="40309-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="40309-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40309-102">SYNOPSIS</span></span>
<span data-ttu-id="40309-103">목록 또는 지정 된 API 연산을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="40309-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40309-104">구문과</span><span class="sxs-lookup"><span data-stu-id="40309-104">SYNTAX</span></span>

### <span data-ttu-id="40309-105">GetAllApiOperations (기본값)</span><span class="sxs-lookup"><span data-stu-id="40309-105">GetAllApiOperations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40309-106">GetById</span><span class="sxs-lookup"><span data-stu-id="40309-106">GetById</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40309-107">설명은</span><span class="sxs-lookup"><span data-stu-id="40309-107">DESCRIPTION</span></span>
<span data-ttu-id="40309-108">**Get-AzureRmApiManagementOperation** 는 목록 또는 지정 된 API 연산을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="40309-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="40309-109">예제의</span><span class="sxs-lookup"><span data-stu-id="40309-109">EXAMPLES</span></span>

### <span data-ttu-id="40309-110">예제 1: 모든 API 관리 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="40309-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="40309-111">이 명령은 모든 API 관리 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="40309-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="40309-112">예제 2: 작업 ID를 기준으로 API 관리 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="40309-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="40309-113">이 명령은 Operation0003 이라는 작업 ID에 따라 API 관리 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="40309-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="40309-114">변수</span><span class="sxs-lookup"><span data-stu-id="40309-114">PARAMETERS</span></span>

### <span data-ttu-id="40309-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="40309-115">-ApiId</span></span>
<span data-ttu-id="40309-116">API 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40309-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="40309-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="40309-117">-Context</span></span>
<span data-ttu-id="40309-118">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40309-118">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="40309-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40309-119">-DefaultProfile</span></span>
<span data-ttu-id="40309-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40309-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="40309-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="40309-121">-OperationId</span></span>
<span data-ttu-id="40309-122">작업 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40309-122">Specifies the operation identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40309-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40309-123">CommonParameters</span></span>
<span data-ttu-id="40309-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="40309-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40309-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40309-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40309-126">입력</span><span class="sxs-lookup"><span data-stu-id="40309-126">INPUTS</span></span>

### <span data-ttu-id="40309-127">않아야</span><span class="sxs-lookup"><span data-stu-id="40309-127">None</span></span>
<span data-ttu-id="40309-128">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40309-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="40309-129">출력</span><span class="sxs-lookup"><span data-stu-id="40309-129">OUTPUTS</span></span>

### <span data-ttu-id="40309-130">ApiManagement. ServiceManagement. \ PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="40309-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>
<span data-ttu-id="40309-131">Api Management 서비스의 API 작업에 대 한 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="40309-131">The details of the API Operation in Api Management service.</span></span>

### <span data-ttu-id="40309-132">IList를<ApiManagement> ServiceManagement. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="40309-132">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation></span></span>
<span data-ttu-id="40309-133">Api Management 서비스의 API 작업 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="40309-133">The list of API Operation in Api Management service.</span></span>

## <span data-ttu-id="40309-134">상속자</span><span class="sxs-lookup"><span data-stu-id="40309-134">NOTES</span></span>

## <span data-ttu-id="40309-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40309-135">RELATED LINKS</span></span>

[<span data-ttu-id="40309-136">새로운 AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="40309-136">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="40309-137">제거-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="40309-137">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="40309-138">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="40309-138">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


