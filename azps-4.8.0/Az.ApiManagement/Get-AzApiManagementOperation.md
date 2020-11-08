---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 568e3562a199a3fc247de41a30a4383bdb37adac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213401"
---
# <span data-ttu-id="a1e3f-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="a1e3f-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="a1e3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1e3f-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e3f-103">목록 또는 지정 된 API 연산을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1e3f-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="a1e3f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a1e3f-104">SYNTAX</span></span>

### <span data-ttu-id="a1e3f-105">GetAllApiOperations (기본값)</span><span class="sxs-lookup"><span data-stu-id="a1e3f-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1e3f-106">GetById</span><span class="sxs-lookup"><span data-stu-id="a1e3f-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1e3f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a1e3f-107">DESCRIPTION</span></span>
<span data-ttu-id="a1e3f-108">**Get-AzApiManagementOperation** 는 목록 또는 지정 된 API 연산을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1e3f-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="a1e3f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a1e3f-109">EXAMPLES</span></span>

### <span data-ttu-id="a1e3f-110">예제 1: 모든 API 관리 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="a1e3f-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="a1e3f-111">이 명령은 모든 API 관리 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1e3f-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="a1e3f-112">예제 2: 작업 ID를 기준으로 API 관리 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="a1e3f-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="a1e3f-113">이 명령은 Operation0003 이라는 작업 ID에 따라 API 관리 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1e3f-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="a1e3f-114">변수</span><span class="sxs-lookup"><span data-stu-id="a1e3f-114">PARAMETERS</span></span>

### <span data-ttu-id="a1e3f-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a1e3f-115">-ApiId</span></span>
<span data-ttu-id="a1e3f-116">API 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1e3f-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="a1e3f-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="a1e3f-117">-ApiRevision</span></span>
<span data-ttu-id="a1e3f-118">API 개정판의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a1e3f-118">Identifier of API Revision.</span></span> <span data-ttu-id="a1e3f-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a1e3f-119">This parameter is optional.</span></span> <span data-ttu-id="a1e3f-120">지정 하지 않으면 현재 활성 api 개정판에서 작업이 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1e3f-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1e3f-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="a1e3f-121">-Context</span></span>
<span data-ttu-id="a1e3f-122">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1e3f-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1e3f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1e3f-123">-DefaultProfile</span></span>
<span data-ttu-id="a1e3f-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a1e3f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1e3f-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="a1e3f-125">-OperationId</span></span>
<span data-ttu-id="a1e3f-126">작업 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1e3f-126">Specifies the operation identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1e3f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e3f-127">CommonParameters</span></span>
<span data-ttu-id="a1e3f-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1e3f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e3f-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a1e3f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e3f-130">입력</span><span class="sxs-lookup"><span data-stu-id="a1e3f-130">INPUTS</span></span>

### <span data-ttu-id="a1e3f-131">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a1e3f-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a1e3f-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a1e3f-132">System.String</span></span>

## <span data-ttu-id="a1e3f-133">출력</span><span class="sxs-lookup"><span data-stu-id="a1e3f-133">OUTPUTS</span></span>

### <span data-ttu-id="a1e3f-134">ApiManagement. ServiceManagement. \ PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="a1e3f-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="a1e3f-135">상속자</span><span class="sxs-lookup"><span data-stu-id="a1e3f-135">NOTES</span></span>

## <span data-ttu-id="a1e3f-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1e3f-136">RELATED LINKS</span></span>

[<span data-ttu-id="a1e3f-137">새로운 AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="a1e3f-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="a1e3f-138">제거-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="a1e3f-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="a1e3f-139">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="a1e3f-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


