---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: b2c623d46dcc2d84e2c90ae5f3d94cfb54f7224a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531295"
---
# <span data-ttu-id="560ff-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="560ff-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="560ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="560ff-102">SYNOPSIS</span></span>
<span data-ttu-id="560ff-103">목록 또는 지정 된 API 연산을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="560ff-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="560ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="560ff-104">SYNTAX</span></span>

### <span data-ttu-id="560ff-105">모든 API 작업 (기본값)</span><span class="sxs-lookup"><span data-stu-id="560ff-105">All API Operations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="560ff-106">ID로 찾기</span><span class="sxs-lookup"><span data-stu-id="560ff-106">Find by ID</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="560ff-107">설명은</span><span class="sxs-lookup"><span data-stu-id="560ff-107">DESCRIPTION</span></span>
<span data-ttu-id="560ff-108">**Get-AzureRmApiManagementOperation** 는 목록 또는 지정 된 API 연산을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="560ff-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="560ff-109">예제의</span><span class="sxs-lookup"><span data-stu-id="560ff-109">EXAMPLES</span></span>

### <span data-ttu-id="560ff-110">예제 1: 모든 API 관리 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="560ff-110">Example 1: Get all API management operations</span></span>
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId
```

<span data-ttu-id="560ff-111">이 명령은 모든 API 관리 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="560ff-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="560ff-112">예제 2: 작업 ID를 기준으로 API 관리 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="560ff-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="560ff-113">이 명령은 Operation0003 이라는 작업 ID에 따라 API 관리 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="560ff-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="560ff-114">변수</span><span class="sxs-lookup"><span data-stu-id="560ff-114">PARAMETERS</span></span>

### <span data-ttu-id="560ff-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="560ff-115">-ApiId</span></span>
<span data-ttu-id="560ff-116">API 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="560ff-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="560ff-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="560ff-117">-Context</span></span>
<span data-ttu-id="560ff-118">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="560ff-118">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="560ff-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="560ff-119">-OperationId</span></span>
<span data-ttu-id="560ff-120">작업 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="560ff-120">Specifies the operation identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="560ff-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="560ff-121">-DefaultProfile</span></span>
<span data-ttu-id="560ff-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="560ff-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="560ff-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="560ff-123">CommonParameters</span></span>
<span data-ttu-id="560ff-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="560ff-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="560ff-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="560ff-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="560ff-126">입력</span><span class="sxs-lookup"><span data-stu-id="560ff-126">INPUTS</span></span>

## <span data-ttu-id="560ff-127">출력</span><span class="sxs-lookup"><span data-stu-id="560ff-127">OUTPUTS</span></span>

### <span data-ttu-id="560ff-128">IList를<ApiManagement> ServiceManagement. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="560ff-128">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation></span></span>

## <span data-ttu-id="560ff-129">상속자</span><span class="sxs-lookup"><span data-stu-id="560ff-129">NOTES</span></span>

## <span data-ttu-id="560ff-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="560ff-130">RELATED LINKS</span></span>

[<span data-ttu-id="560ff-131">새로운 AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="560ff-131">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="560ff-132">제거-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="560ff-132">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="560ff-133">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="560ff-133">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


