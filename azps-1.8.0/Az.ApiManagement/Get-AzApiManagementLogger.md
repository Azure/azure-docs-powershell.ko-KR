---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: 633b76e60ef47ef871033ca55e7595c6eacd68f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689143"
---
# <span data-ttu-id="c378a-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c378a-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="c378a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c378a-102">SYNOPSIS</span></span>
<span data-ttu-id="c378a-103">API Management로 거 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c378a-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="c378a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c378a-104">SYNTAX</span></span>

### <span data-ttu-id="c378a-105">GetAllLoggers (기본값)</span><span class="sxs-lookup"><span data-stu-id="c378a-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c378a-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="c378a-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c378a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c378a-107">DESCRIPTION</span></span>
<span data-ttu-id="c378a-108">**AzApiManagementLogger** Cmdlet은 Azure API Management **로 거** 또는 모든로 거를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c378a-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="c378a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c378a-109">EXAMPLES</span></span>

### <span data-ttu-id="c378a-110">예제 1: 모든로 거 가져오기</span><span class="sxs-lookup"><span data-stu-id="c378a-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="c378a-111">이 명령은 지정 된 컨텍스트에 대 한 모든로 거를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c378a-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="c378a-112">예제 2: 특정로 거 가져오기</span><span class="sxs-lookup"><span data-stu-id="c378a-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="c378a-113">이 명령은 ID Logger123를 가진로 거를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c378a-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="c378a-114">변수</span><span class="sxs-lookup"><span data-stu-id="c378a-114">PARAMETERS</span></span>

### <span data-ttu-id="c378a-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="c378a-115">-Context</span></span>
<span data-ttu-id="c378a-116">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c378a-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c378a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c378a-117">-DefaultProfile</span></span>
<span data-ttu-id="c378a-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c378a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c378a-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="c378a-119">-LoggerId</span></span>
<span data-ttu-id="c378a-120">가져올 특정 로거에서 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c378a-120">Specifies the ID of the specific logger to get.</span></span>

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

### <span data-ttu-id="c378a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c378a-121">CommonParameters</span></span>
<span data-ttu-id="c378a-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c378a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c378a-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c378a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c378a-124">입력</span><span class="sxs-lookup"><span data-stu-id="c378a-124">INPUTS</span></span>

### <span data-ttu-id="c378a-125">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c378a-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c378a-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c378a-126">System.String</span></span>

## <span data-ttu-id="c378a-127">출력</span><span class="sxs-lookup"><span data-stu-id="c378a-127">OUTPUTS</span></span>

### <span data-ttu-id="c378a-128">ApiManagement. ServiceManagement. \ PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c378a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="c378a-129">상속자</span><span class="sxs-lookup"><span data-stu-id="c378a-129">NOTES</span></span>

## <span data-ttu-id="c378a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c378a-130">RELATED LINKS</span></span>

[<span data-ttu-id="c378a-131">새로운 AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c378a-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="c378a-132">제거-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c378a-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="c378a-133">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c378a-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


