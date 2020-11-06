---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
ms.openlocfilehash: bcfcd052d2278fa39bc310a5c1927457a1b0fcd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532860"
---
# <span data-ttu-id="3e6fd-101">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3e6fd-101">Get-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="3e6fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e6fd-102">SYNOPSIS</span></span>
<span data-ttu-id="3e6fd-103">API Management로 거 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3e6fd-103">Gets API Management Logger objects.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e6fd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3e6fd-104">SYNTAX</span></span>

### <span data-ttu-id="3e6fd-105">GetAllLoggers (기본값)</span><span class="sxs-lookup"><span data-stu-id="3e6fd-105">GetAllLoggers (Default)</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e6fd-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="3e6fd-106">GetByLoggerId</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e6fd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3e6fd-107">DESCRIPTION</span></span>
<span data-ttu-id="3e6fd-108">**AzureRmApiManagementLogger** Cmdlet은 Azure API Management **로 거** 또는 모든로 거를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3e6fd-108">The **Get-AzureRmApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="3e6fd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3e6fd-109">EXAMPLES</span></span>

### <span data-ttu-id="3e6fd-110">예제 1: 모든로 거 가져오기</span><span class="sxs-lookup"><span data-stu-id="3e6fd-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementLogger -Context $apimContext
```

<span data-ttu-id="3e6fd-111">이 명령은 지정 된 컨텍스트에 대 한 모든로 거를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3e6fd-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="3e6fd-112">예제 2: 특정로 거 가져오기</span><span class="sxs-lookup"><span data-stu-id="3e6fd-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="3e6fd-113">이 명령은 ID Logger123를 가진로 거를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e6fd-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="3e6fd-114">변수</span><span class="sxs-lookup"><span data-stu-id="3e6fd-114">PARAMETERS</span></span>

### <span data-ttu-id="3e6fd-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="3e6fd-115">-Context</span></span>
<span data-ttu-id="3e6fd-116">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e6fd-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3e6fd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e6fd-117">-DefaultProfile</span></span>
<span data-ttu-id="3e6fd-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3e6fd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="3e6fd-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="3e6fd-119">-LoggerId</span></span>
<span data-ttu-id="3e6fd-120">가져올 특정 로거에서 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e6fd-120">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByLoggerId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e6fd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e6fd-121">CommonParameters</span></span>
<span data-ttu-id="3e6fd-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e6fd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e6fd-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e6fd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e6fd-124">입력</span><span class="sxs-lookup"><span data-stu-id="3e6fd-124">INPUTS</span></span>

### <span data-ttu-id="3e6fd-125">않아야</span><span class="sxs-lookup"><span data-stu-id="3e6fd-125">None</span></span>
<span data-ttu-id="3e6fd-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e6fd-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3e6fd-127">출력</span><span class="sxs-lookup"><span data-stu-id="3e6fd-127">OUTPUTS</span></span>

### <span data-ttu-id="3e6fd-128">ApiManagement. ServiceManagement. \ PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3e6fd-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>
<span data-ttu-id="3e6fd-129">API Management 서비스에 구성 된로 거에 대 한 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="3e6fd-129">The detail of the Logger configured in API Management service.</span></span>

### <span data-ttu-id="3e6fd-130">IList를<ApiManagement> ServiceManagement. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3e6fd-130">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger></span></span>
<span data-ttu-id="3e6fd-131">API Management 서비스에 구성 된로 거 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3e6fd-131">The list of Loggers configured in API Management service.</span></span>

## <span data-ttu-id="3e6fd-132">상속자</span><span class="sxs-lookup"><span data-stu-id="3e6fd-132">NOTES</span></span>

## <span data-ttu-id="3e6fd-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e6fd-133">RELATED LINKS</span></span>

[<span data-ttu-id="3e6fd-134">새로운 AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3e6fd-134">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="3e6fd-135">제거-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3e6fd-135">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="3e6fd-136">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3e6fd-136">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


