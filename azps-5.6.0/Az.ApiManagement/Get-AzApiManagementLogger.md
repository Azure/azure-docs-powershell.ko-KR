---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: aafe70a476dbf983e8ae68b0f1fadf021b2990f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973008"
---
# <span data-ttu-id="68d59-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="68d59-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="68d59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68d59-102">SYNOPSIS</span></span>
<span data-ttu-id="68d59-103">API Management 로거 개체를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68d59-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="68d59-104">구문</span><span class="sxs-lookup"><span data-stu-id="68d59-104">SYNTAX</span></span>

### <span data-ttu-id="68d59-105">GetAllLoggers(기본값)</span><span class="sxs-lookup"><span data-stu-id="68d59-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68d59-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="68d59-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68d59-107">설명</span><span class="sxs-lookup"><span data-stu-id="68d59-107">DESCRIPTION</span></span>
<span data-ttu-id="68d59-108">**Get-AzApiManagementLogger** cmdlet은 Azure API Management **Logger** 또는 모든 로거를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68d59-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="68d59-109">예제</span><span class="sxs-lookup"><span data-stu-id="68d59-109">EXAMPLES</span></span>

### <span data-ttu-id="68d59-110">예제 1: 모든 로거 사용</span><span class="sxs-lookup"><span data-stu-id="68d59-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="68d59-111">이 명령은 지정된 컨텍스트에 대한 모든 로거를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68d59-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="68d59-112">예제 2: 특정 로거를 구합니다.</span><span class="sxs-lookup"><span data-stu-id="68d59-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="68d59-113">이 명령은 ID Logger123이 있는 로거를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="68d59-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="68d59-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="68d59-114">PARAMETERS</span></span>

### <span data-ttu-id="68d59-115">-Context</span><span class="sxs-lookup"><span data-stu-id="68d59-115">-Context</span></span>
<span data-ttu-id="68d59-116">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="68d59-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="68d59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68d59-117">-DefaultProfile</span></span>
<span data-ttu-id="68d59-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68d59-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68d59-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="68d59-119">-LoggerId</span></span>
<span data-ttu-id="68d59-120">얻을 특정 로거의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="68d59-120">Specifies the ID of the specific logger to get.</span></span>

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

### <span data-ttu-id="68d59-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68d59-121">CommonParameters</span></span>
<span data-ttu-id="68d59-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="68d59-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68d59-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68d59-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68d59-124">입력</span><span class="sxs-lookup"><span data-stu-id="68d59-124">INPUTS</span></span>

### <span data-ttu-id="68d59-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="68d59-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="68d59-126">System.String</span><span class="sxs-lookup"><span data-stu-id="68d59-126">System.String</span></span>

## <span data-ttu-id="68d59-127">출력</span><span class="sxs-lookup"><span data-stu-id="68d59-127">OUTPUTS</span></span>

### <span data-ttu-id="68d59-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="68d59-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="68d59-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="68d59-129">NOTES</span></span>

## <span data-ttu-id="68d59-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68d59-130">RELATED LINKS</span></span>

[<span data-ttu-id="68d59-131">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="68d59-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="68d59-132">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="68d59-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="68d59-133">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="68d59-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


