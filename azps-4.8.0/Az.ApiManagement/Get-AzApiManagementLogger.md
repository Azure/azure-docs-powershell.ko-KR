---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: c4b7246a2b600c1ed0d9f8a01ea3fd69cd4af33d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211989"
---
# <span data-ttu-id="35b75-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="35b75-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="35b75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35b75-102">SYNOPSIS</span></span>
<span data-ttu-id="35b75-103">API Management로 거 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35b75-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="35b75-104">구문과</span><span class="sxs-lookup"><span data-stu-id="35b75-104">SYNTAX</span></span>

### <span data-ttu-id="35b75-105">GetAllLoggers (기본값)</span><span class="sxs-lookup"><span data-stu-id="35b75-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35b75-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="35b75-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35b75-107">설명은</span><span class="sxs-lookup"><span data-stu-id="35b75-107">DESCRIPTION</span></span>
<span data-ttu-id="35b75-108">**AzApiManagementLogger** Cmdlet은 Azure API Management **로 거** 또는 모든로 거를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35b75-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="35b75-109">예제의</span><span class="sxs-lookup"><span data-stu-id="35b75-109">EXAMPLES</span></span>

### <span data-ttu-id="35b75-110">예제 1: 모든로 거 가져오기</span><span class="sxs-lookup"><span data-stu-id="35b75-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="35b75-111">이 명령은 지정 된 컨텍스트에 대 한 모든로 거를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35b75-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="35b75-112">예제 2: 특정로 거 가져오기</span><span class="sxs-lookup"><span data-stu-id="35b75-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="35b75-113">이 명령은 ID Logger123를 가진로 거를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="35b75-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="35b75-114">변수</span><span class="sxs-lookup"><span data-stu-id="35b75-114">PARAMETERS</span></span>

### <span data-ttu-id="35b75-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="35b75-115">-Context</span></span>
<span data-ttu-id="35b75-116">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35b75-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="35b75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35b75-117">-DefaultProfile</span></span>
<span data-ttu-id="35b75-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35b75-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35b75-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="35b75-119">-LoggerId</span></span>
<span data-ttu-id="35b75-120">가져올 특정 로거에서 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35b75-120">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByLoggerId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35b75-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35b75-121">CommonParameters</span></span>
<span data-ttu-id="35b75-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35b75-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35b75-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35b75-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35b75-124">입력</span><span class="sxs-lookup"><span data-stu-id="35b75-124">INPUTS</span></span>

### <span data-ttu-id="35b75-125">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="35b75-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="35b75-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="35b75-126">System.String</span></span>

## <span data-ttu-id="35b75-127">출력</span><span class="sxs-lookup"><span data-stu-id="35b75-127">OUTPUTS</span></span>

### <span data-ttu-id="35b75-128">ApiManagement. ServiceManagement. \ PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="35b75-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="35b75-129">상속자</span><span class="sxs-lookup"><span data-stu-id="35b75-129">NOTES</span></span>

## <span data-ttu-id="35b75-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35b75-130">RELATED LINKS</span></span>

[<span data-ttu-id="35b75-131">새로운 AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="35b75-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="35b75-132">제거-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="35b75-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="35b75-133">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="35b75-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


