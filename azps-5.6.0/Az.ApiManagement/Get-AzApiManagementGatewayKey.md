---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: 08931af2c5d4f4747bd02a759e374d8fccd247c0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981323"
---
# <span data-ttu-id="1642b-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="1642b-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="1642b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1642b-102">SYNOPSIS</span></span>
<span data-ttu-id="1642b-103">기존 게이트웨이의 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1642b-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="1642b-104">구문</span><span class="sxs-lookup"><span data-stu-id="1642b-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1642b-105">설명</span><span class="sxs-lookup"><span data-stu-id="1642b-105">DESCRIPTION</span></span>
<span data-ttu-id="1642b-106">**Get-AzApiManagementGatewayKey** cmdlet은 기존 게이트웨이의 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1642b-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="1642b-107">예제</span><span class="sxs-lookup"><span data-stu-id="1642b-107">EXAMPLES</span></span>

### <span data-ttu-id="1642b-108">예제 2: ID로 게이트웨이를 얻다</span><span class="sxs-lookup"><span data-stu-id="1642b-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="1642b-109">이 명령은 "0123456789" 게이트웨이에 대한 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1642b-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="1642b-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1642b-110">PARAMETERS</span></span>

### <span data-ttu-id="1642b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1642b-111">-Context</span></span>
<span data-ttu-id="1642b-112">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="1642b-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1642b-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="1642b-113">This parameter is required.</span></span>

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

### <span data-ttu-id="1642b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1642b-114">-DefaultProfile</span></span>
<span data-ttu-id="1642b-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1642b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1642b-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="1642b-116">-GatewayId</span></span>
<span data-ttu-id="1642b-117">게이트웨이 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="1642b-117">Gateway identifier.</span></span>
<span data-ttu-id="1642b-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="1642b-118">This parameter is required.</span></span>

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

### <span data-ttu-id="1642b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1642b-119">CommonParameters</span></span>
<span data-ttu-id="1642b-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1642b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1642b-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1642b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1642b-122">입력</span><span class="sxs-lookup"><span data-stu-id="1642b-122">INPUTS</span></span>

### <span data-ttu-id="1642b-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1642b-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1642b-124">System.String</span><span class="sxs-lookup"><span data-stu-id="1642b-124">System.String</span></span>

## <span data-ttu-id="1642b-125">출력</span><span class="sxs-lookup"><span data-stu-id="1642b-125">OUTPUTS</span></span>

### <span data-ttu-id="1642b-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="1642b-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="1642b-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1642b-127">NOTES</span></span>

## <span data-ttu-id="1642b-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1642b-128">RELATED LINKS</span></span>
