---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 10c84654bb5d074ee9f668062d1fa7a18d92f8b0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216938"
---
# <span data-ttu-id="273ca-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="273ca-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="273ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="273ca-102">SYNOPSIS</span></span>
<span data-ttu-id="273ca-103">진단의 Http 메시지 진단 설정인 **PsApiManagementHttpMessageDiagnostic** 의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="273ca-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="273ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="273ca-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="273ca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="273ca-105">DESCRIPTION</span></span>
<span data-ttu-id="273ca-106">Cmdlet **AzApiManagementHttpMessageDiagnostic** 는 Http 메시지 진단 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="273ca-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="273ca-107">예제의</span><span class="sxs-lookup"><span data-stu-id="273ca-107">EXAMPLES</span></span>

### <span data-ttu-id="273ca-108">예제 1: 기본 Http 메시지 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="273ca-108">Example 1: Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="273ca-109">`Content-Type`100 바이트와 함께 로그 및 머리글 하는 데 사용 되는 http 메시지 진단 설정 만들기 `User-Agent``body`</span><span class="sxs-lookup"><span data-stu-id="273ca-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="273ca-110">변수</span><span class="sxs-lookup"><span data-stu-id="273ca-110">PARAMETERS</span></span>

### <span data-ttu-id="273ca-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="273ca-111">-BodyBytesToLog</span></span>
<span data-ttu-id="273ca-112">로깅할 요청 본문 바이트의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="273ca-112">Number of request body bytes to log.</span></span> <span data-ttu-id="273ca-113">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="273ca-113">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="273ca-114">-DefaultProfile</span></span>
<span data-ttu-id="273ca-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="273ca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="273ca-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="273ca-116">-HeadersToLog</span></span>
<span data-ttu-id="273ca-117">로깅할 헤더의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="273ca-117">The array of headers to log.</span></span> <span data-ttu-id="273ca-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="273ca-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="273ca-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="273ca-119">CommonParameters</span></span>
<span data-ttu-id="273ca-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="273ca-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="273ca-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="273ca-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="273ca-122">입력</span><span class="sxs-lookup"><span data-stu-id="273ca-122">INPUTS</span></span>

### <span data-ttu-id="273ca-123">않아야</span><span class="sxs-lookup"><span data-stu-id="273ca-123">None</span></span>

## <span data-ttu-id="273ca-124">출력</span><span class="sxs-lookup"><span data-stu-id="273ca-124">OUTPUTS</span></span>

### <span data-ttu-id="273ca-125">ApiManagement. ServiceManagement. \ PsApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="273ca-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="273ca-126">상속자</span><span class="sxs-lookup"><span data-stu-id="273ca-126">NOTES</span></span>

## <span data-ttu-id="273ca-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="273ca-127">RELATED LINKS</span></span>

[<span data-ttu-id="273ca-128">새로운 AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="273ca-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="273ca-129">새로운 AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="273ca-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)