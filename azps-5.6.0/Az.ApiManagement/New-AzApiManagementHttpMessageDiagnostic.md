---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 3475778104655e6b27061edf08ced376f192ea34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988540"
---
# <span data-ttu-id="59659-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="59659-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="59659-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59659-102">SYNOPSIS</span></span>
<span data-ttu-id="59659-103">진단의 Http 메시지 진단 설정인 **PsApiManagementHttpMessageDiagnostic의** 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="59659-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="59659-104">구문</span><span class="sxs-lookup"><span data-stu-id="59659-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59659-105">설명</span><span class="sxs-lookup"><span data-stu-id="59659-105">DESCRIPTION</span></span>
<span data-ttu-id="59659-106">cmdlet **New-AzApiManagementHttpMessageDiagnostic는** Http 메시지 진단 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="59659-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="59659-107">예제</span><span class="sxs-lookup"><span data-stu-id="59659-107">EXAMPLES</span></span>

### <span data-ttu-id="59659-108">예제 1: 기본 Http 메시지 진단 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="59659-108">Example 1: Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="59659-109">100비트와 함께 로그 및 헤더에 http 메시지 진단 `Content-Type` `User-Agent` 설정 만들기 `body`</span><span class="sxs-lookup"><span data-stu-id="59659-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="59659-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="59659-110">PARAMETERS</span></span>

### <span data-ttu-id="59659-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="59659-111">-BodyBytesToLog</span></span>
<span data-ttu-id="59659-112">로그할 요청 본문의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="59659-112">Number of request body bytes to log.</span></span> <span data-ttu-id="59659-113">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="59659-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="59659-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59659-114">-DefaultProfile</span></span>
<span data-ttu-id="59659-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59659-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59659-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="59659-116">-HeadersToLog</span></span>
<span data-ttu-id="59659-117">로그할 헤더의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="59659-117">The array of headers to log.</span></span> <span data-ttu-id="59659-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="59659-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="59659-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59659-119">CommonParameters</span></span>
<span data-ttu-id="59659-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="59659-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59659-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59659-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59659-122">입력</span><span class="sxs-lookup"><span data-stu-id="59659-122">INPUTS</span></span>

### <span data-ttu-id="59659-123">없음</span><span class="sxs-lookup"><span data-stu-id="59659-123">None</span></span>

## <span data-ttu-id="59659-124">출력</span><span class="sxs-lookup"><span data-stu-id="59659-124">OUTPUTS</span></span>

### <span data-ttu-id="59659-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="59659-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="59659-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="59659-126">NOTES</span></span>

## <span data-ttu-id="59659-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59659-127">RELATED LINKS</span></span>

[<span data-ttu-id="59659-128">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="59659-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="59659-129">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="59659-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)